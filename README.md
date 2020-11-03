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
