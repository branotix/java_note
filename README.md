# java_note
* Spring Initializr হলো একটি ওয়েবসাইট এবং সার্ভিস, যার মাধ্যমে আপনি কমান্ড লাইন (Command Line) ব্যবহার করেই নতুন একটি স্প্রিং বুট প্রজেক্ট খুব সহজে তৈরি করার কমান্ড নিচে ঃ 
```
curl https://start.spring.io/starter.zip \
  -d dependencies=web,lombok \
  -d language=java \
  -d type=maven-project \
  -d groupId=com.example \
  -d artifactId=my-app \
  -d name=my-app \
  -o my-app.zip
```
* জিপ ফাইল Unzip করার পর যে my-app ফোল্ডারটি তৈরি হয়েছে, টার্মিনালে বা কমান্ড প্রম্পটে সেই ফোল্ডারের ভেতরে থাকুন (cd my-app) এবং নিচের
```
./mvnw spring-boot:run
```
* এই ফোল্ডার পাথে (File Location) যান:src ➔ main ➔ java ➔ com ➔ example ➔ myapp ফাইলটি ওপেন করে কোডটি ঠিক নিচের মতো বদলে দিন (Modify করুন): অবশ্যই ফাইলের নাম এই MyAppApplication নামের সাথে মিল করে দিন  
  ```
  package com.example.myapp;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RestController;

@SpringBootApplication
@RestController  // ১. স্প্রিং-কে বলছি এটি একটি ওয়েব কন্ট্রোলার
public class MyAppApplication {

    public static void main(String[] args) {
        SpringApplication.run(MyAppApplication.class, args);
    }

    // ২. নতুন একটি এন্ডপয়েন্ট বা রাউট তৈরি করছি
    @GetMapping("/")
    public String sayHello() {
        return "Hello, World! I am learning Spring Boot";
    }
}
```
*পুনরায় রান করার পর নিচের url এ যেয়ে চেক করুন যে সব কিছু ঠিকভবে কাজ করতেছে নাকি ঃ
```localhost:8080```
