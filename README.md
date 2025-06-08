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




