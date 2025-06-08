# project3

OPEN IntelliJ IDEA
=
new
project
java      project3


          gradle


          groovy

                      create


Modify build.gradle and paste the below code:

plugins {
    id 'application'
}
repositories {
    mavenCentral()
}
dependencies {
    testImplementation 'org.junit.jupiter:junit-jupiter:5.8.1'
}
application {
    mainClass = 'com.example.Main'
}


src/main/java/
right click
new
package
com.example

copy below code:

package com.example;

public class Main {
 public static void main(String[] args) {

  System.out.println("Hello from Gradle!");
 }
}


right click on com.example
Main.java  open hoga 


click on upar |> [run]              
                                            
build successfull ayega


click on gradle on right
Click Tasks > application > run .                                              build successfull ayega
Or run in terminal:  gradle run                                                build successfull ayega


koi dusre project se docs folder copy karke paste kar de o n the project name p3 par right click karke        

OPTIONAL

Then create file index.html inside docs

<!DOCTYPE html>
<html lang="en">
<head>
 <meta charset="UTF-8">
 <meta name="viewport" content="width=device-width, initial-scale=1.0">
 <title>My Simple Website</title>
 <link rel="stylesheet" href="style.css">
</head>
<body>
<header>
 <img src="https://upload.wikimedia.org/wikipedia/commons/2/24/LEGO_logo.svg" 
alt="Logo">
</header>
<h1>Welcome To My Simple Website</h1>
</body>
</html>


Then create style.css inside docs

body {
 font-family: Arial, sans-serif;
 background-color: #f4f4f4;
 text-align: center;
}
header img {
 width: 100px;
}


OPTIONAL

IN TERMINAL TYPE TH EFOLLOWING ONE BY ONE

git init
git add .
git status
git commit -m "Added the docs folder with html, css, logo for deployement"
git status
git remote add origin https://github.com/Lavzgoyal999/project3.git
git push -u origin master

GO TO GITHUB WAHA REPOSITORY MEH SARI FILES AJANI CHAHIYA
DEFAULT KO MAIN SE MASTER KARNA 
SETTINGS 
PAGES
MASTER
DOCS
SAVE 
RELOAD 
LIVE URL AYEGA 
CLICK KARO THATS UR WEBSITE

 Update build.gradle

plugins {
    id 'application'
}
repositories {
    mavenCentral()
}

dependencies {
    testImplementation 'org.junit.jupiter:junit-jupiter:5.8.1'
    testImplementation 'org.seleniumhq.selenium:selenium-java:4.28.1' // use the latest stable version
    testImplementation 'org.testng:testng:7.4.0' // use the latest stable version
}
test {
    useTestNG()
}

application {
    mainClass = 'com.example.Main'
}


build successfull ayega


src/main/java/
right click
new
package
org.test


right click on org.test
new
java class
WebPageTest.java

IN WebPageTest.java PASTE THE BELOW CODE:

package org.test;

import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.testng.Assert;
import org.testng.annotations.AfterTest;
import org.testng.annotations.BeforeTest;
import org.testng.annotations.Test;

import static org.testng.Assert.assertTrue;

public class WebPageTest {
    private static WebDriver driver;
    
    @BeforeTest
    public void openBrowser() throws InterruptedException {
        driver = new ChromeDriver();
        driver.manage().window().maximize();
        Thread.sleep(2000);
        driver.get("https://sauravsarkar-codersarcade.github.io/CA-GRADLE/"); 
    }
    
    @Test
    public void titleValidationTest(){
        String actualTitle = driver.getTitle();
        String expectedTitle = "Tripillar Solutions";
        Assert.assertEquals(actualTitle, expectedTitle);
        assertTrue(true, "Title should contain 'Tripillar'");
    }
    
    @AfterTest
    public void closeBrowser() throws InterruptedException {
        Thread.sleep(1000);
        driver.quit();
    }
}




CLICK ON GRADLE ON RIGHT
Click Tasks > verification > test

Or run from terminal:      gradle test


BUILD SUCCESSFUL ayega

modify build.gradle   copy paste the below code:

plugins {
    id 'application'
    id 'java'
}

repositories {
    mavenCentral()
}

dependencies {
    testImplementation 'org.junit.jupiter:junit-jupiter:5.8.1'
    testImplementation 'org.seleniumhq.selenium:selenium-java:4.28.1' // use the latest stable version
    testImplementation 'org.testng:testng:7.4.0' // use the latest stable version
}

test {
    useTestNG()
}

application {
    mainClass = 'com.example.Main'
}

jar {
    manifest {
        attributes 'Main-Class': 'com.example.Main'  // This tells Java where to start execution
    }
}



in terminal run the following commands:

gradle jar 

build-libs-jar file is created

in terminal run the following commands:

java -jar .\build\libs\p3.jar    

DONE



