# java_note
Spring Initializr হলো একটি ওয়েবসাইট এবং সার্ভিস, যার মাধ্যমে আপনি কমান্ড লাইন (Command Line) ব্যবহার করেই নতুন একটি স্প্রিং বুট প্রজেক্ট খুব সহজে তৈরি করে নিতে পারেন।
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
