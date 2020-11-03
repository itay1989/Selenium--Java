# testcase
public class SWE {

	public static void main(String[] args) throws InterruptedException {
		System.setProperty("webdriver.chrome.driver", "C:\\Selenium\\chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.get("https://www.amazon.in/");
		driver.manage().window().maximize();
		Thread.sleep(2000);
		driver.findElement(By.id("twotabsearchtextbox")).sendKeys("Poco F1");
		Thread.sleep(2000);
		driver.findElement(By.className("nav-input")).click();
		driver.navigate().to("https://www.edureka.co/blog");
		Thread.sleep(4000);
		driver.navigate().back();
		Thread.sleep(4000);
		driver.quit();

	}

}

# same code only with WebManager!

## note that more packages are imported since u use multiple browsers

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.ie.InternetExplorerDriver;

import io.github.bonigarcia.wdm.WebDriverManager;

public class SWE {

	public static void main(String[] args) throws InterruptedException {
		
		//System.setProperty("webdriver.chrome.driver", "C:\\Selenium\\chromedriver.exe");
		//WebDriver driver = new ChromeDriver();
		
		WebDriverManager.firefoxdriver().setup();
		WebDriver driver = new FirefoxDriver();

		
		driver.get("https://www.amazon.in/");
		driver.manage().window().maximize();
		Thread.sleep(2000);
		driver.findElement(By.id("twotabsearchtextbox")).sendKeys("Poco F1");
		Thread.sleep(2000);
		driver.findElement(By.className("nav-search-submit")).click();
		Thread.sleep(8000);
		driver.navigate().to("https://www.edureka.co/blog");
		Thread.sleep(4000);
		driver.navigate().back();
		Thread.sleep(4000);
		driver.quit();

	}

}
