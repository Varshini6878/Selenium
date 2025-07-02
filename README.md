package org.example;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class Main {
    public static void main(String[] args) {
        WebDriver driver = new ChromeDriver();

        driver.get("https://app.fileright.com/registration/logincheck.do?next=/application-center/applicationcenter.do");

        driver.manage().window().maximize();


        WebElement emailField = driver.findElement(By.id("email"));
        emailField.sendKeys("john@gmail.com");


        try {
            Thread.sleep(9000);
        } catch (InterruptedException e) {
            e.printStackTrace();
        }

        driver.quit();
    }
}
