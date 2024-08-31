package ecommerce;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

import io.github.bonigarcia.wdm.WebDriverManager;

public class Ecommerce {
    WebDriver driver;

    // Method to set up the WebDriver and navigate to the e-commerce website
    public void launchBrowser() {
        WebDriverManager.chromedriver().setup();
        driver = new ChromeDriver();
        driver.manage().window().maximize();
        driver.get("https://www.saucedemo.com/");
    }

    // Method to perform login
    public void login() throws InterruptedException {
        // Wait for 2 seconds (consider using WebDriverWait for better synchronization)
        Thread.sleep(2000);
        // Find the username field and enter a username
        driver.findElement(By.id("user-name")).sendKeys("standard_user");
        // Wait for 2 seconds
        Thread.sleep(2000);
        // Find the password field and enter a password
        driver.findElement(By.id("password")).sendKeys("secret_sauce");
        // Wait for 2 seconds
        Thread.sleep(2000);
        // Click the login button
        driver.findElement(By.id("login-button")).click();
        // Wait for 2 seconds
        Thread.sleep(2000);
    }

    // Method to navigate through the e-commerce site and add items to the cart
    public void navigateEcommerce() throws InterruptedException {
        // Click on the "Add to Cart" button for a fleece jacket
        driver.findElement(By.name("add-to-cart-sauce-labs-fleece-jacket")).click();
        // Wait for 2 seconds
        Thread.sleep(2000);
        // Click on the "Add to Cart" button for a red T-shirt
        driver.findElement(By.xpath("//*[@id=\"add-to-cart-test.allthethings()-t-shirt-(red)\"]")).click();
        // Wait for 2 seconds
        Thread.sleep(2000);
        // Click on the shopping cart icon to view the cart
        driver.findElement(By.xpath("//*[@id=\"shopping_cart_container\"]/a")).click();
        // Wait for 2 seconds
        Thread.sleep(2000);
    }

    // Method to proceed to checkout, enter user information, and complete the checkout process
    public void checkOut() throws InterruptedException {
        // Click on the "Checkout" button
        driver.findElement(By.name("checkout")).click();
        // Wait for 2 seconds
        Thread.sleep(2000);
        // Enter the first name
        driver.findElement(By.id("first-name")).sendKeys("JAMES");
        // Wait for 2 seconds
        Thread.sleep(2000);
        // Enter the last name
        driver.findElement(By.id("last-name")).sendKeys("BOND");
        // Wait for 2 seconds
        Thread.sleep(2000);
        // Enter the postal code
        driver.findElement(By.xpath("//*[@id=\"postal-code\"]")).sendKeys("007");
        // Wait for 2 seconds
        Thread.sleep(2000);
        // Click on the "Continue" button
        driver.findElement(By.xpath("//*[@id=\"continue\"]")).click();
        // Wait for 2 seconds
        Thread.sleep(2000);
        // Click on the "Finish" button to complete the checkout
        driver.findElement(By.id("finish")).click();
        // Wait for 2 seconds
        Thread.sleep(2000);
        // Click on the "Back to Products" button
        driver.findElement(By.name("back-to-products")).click();
        // Wait for 2 seconds
        Thread.sleep(2000);
    }

    // Method to log out from the e-commerce site
    public void logOut() throws InterruptedException {
        // Open the burger menu
        driver.findElement(By.xpath("//*[@id=\"react-burger-menu-btn\"]")).click();
        // Wait for 2 seconds
        Thread.sleep(2000);
        // Click on the "Logout" link
        driver.findElement(By.xpath("//*[@id=\"logout_sidebar_link\"]")).click();
        // Wait for 2 seconds
        Thread.sleep(2000);
    }

    // Method to close the browser
    public void closeBrowser() {
        // Quit the WebDriver, closing the browser
        driver.quit();
    }

    public static void main(String[] args) throws InterruptedException {
        // Create an instance of the Ecommerce class
        Ecommerce obj = new Ecommerce();
        // Launch the browser and navigate to the e-commerce site
        obj.launchBrowser();
        // Perform login
        obj.login();
        // Navigate through the e-commerce site and add items to the cart
        obj.navigateEcommerce();
        // Proceed to checkout, enter user information, and complete the checkout process
        obj.checkOut();
        // Log out from the e-commerce site
        obj.logOut();
        // Close the browser
        obj.closeBrowser();
    }
}
