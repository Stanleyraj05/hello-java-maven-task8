# Hello Java Maven with Jenkins

This project demonstrates how to set up a **Java HelloWorld application** using **Maven**, and build it using **Jenkins**. This is a basic CI/CD pipeline introduction task.

---

## 📁 Project Structure

hello-java-maven/
├── pom.xml  
├── README.md  
└── src/  
  └── main/  
    └── java/  
      └── HelloWorld.java

---

## 📌 What You’ll Learn

- How to write a basic Java + Maven app  
- How to set up Jenkins and configure Maven  
- How to create a Freestyle Jenkins job  
- How to trigger builds and view console output  
- How to run the compiled Java program via Jenkins  

---

## 💻 Step-by-Step Instructions

###  Create the Java App

File: `src/main/java/HelloWorld.java`

 java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, Jenkins + Maven!");
    }
}

### Run It Locally

- docker run -p 8080:8080 jenkins/jenkins:lts

###  Set up Maven in Jenkins
- Go to: Manage Jenkins → Global Tool Configuration

- Under Maven, click Add Maven

- Name it: Maven 3.8.6

- Let Jenkins install it automatically

###  Create Jenkins Freestyle Job
- Go to Dashboard → New Item → Freestyle project

- Name: hello-java-maven

- In Build Section:
  Add build step → Invoke top-level Maven targets
  Set Goals to: clean package

###  Upload or Pull Java Code
- Clone from GitHub 

###  Run Java Program in Jenkins
- Execute shell
  cd $WORKSPACE
java -cp target/hello-1.0.jar HelloWorld

- Expected output:
  
Hello, Jenkins + Maven!



<img width="1440" alt="Screenshot 2025-04-18 at 20 20 13" src="https://github.com/user-attachments/assets/c050dead-171f-42d0-bf31-2e61e5353941" />
<img width="1440" alt="Screenshot 2025-04-18 at 20 22 55" src="https://github.com/user-attachments/assets/591f739b-ee57-4137-9a82-9d5c3c4b9b41" />



