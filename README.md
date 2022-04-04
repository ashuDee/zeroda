
	public static void main(String[] args) throws InterruptedException {
	System.setProperty("webdriver.chrome.driver",
			"C:\\Automation\\chromedriver.exe");
	WebDriver driver=new ChromeDriver();
	driver.get("https://www.facebook.com/signup");
	  WebElement day = driver.findElement(By.xpath("//select[@id='day']"));
	  
	  Select sel = new Select(day);
	  sel.selectByIndex(2);
	
	  Thread.sleep(1000);
	  
	 WebElement month = driver.findElement(By.xpath("//select[@id='month']"));
	 Select sel1=new Select(month);
	 sel1.selectByVisibleText("Feb");
	 
	 WebElement year = driver.findElement(By.xpath("//select[@id='year']"));
	   Select sel2=new Select(year);
	   sel2.deselectByValue("11");
	

	}

}
