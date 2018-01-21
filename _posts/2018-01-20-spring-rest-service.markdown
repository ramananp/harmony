---
layout: post
title:  "REST Service Using Spring Boot"
date:   2018-01-20 20:18:45
description: Creating a REST service using Spring Boot
categories:
- post
tags:
- spring
- spring-boot
- REST Service
---

## REST Service
How to create a REST service using Spring Boot?

### Introduction
In my last [Spring Boot post](http://ramanan.io/post/2018/01/07/spring-boot/), I showed you how to initialize a spring boot application from scratch. In this post, I will show you how to create a rest service using Spring Boot and Spring REST Controller.

### About This Post
This is the second post on the Spring Boot series. In this post I will explain how to create a simple rest service using spring boot and running it in the local machine.

### REST or RESTful Service
>_Representational state transfer (REST) or RESTful web services are a way of providing interoperability between computer systems on the Internet. REST-compliant Web services allow requesting systems to access and manipulate textual representations of Web resources using a uniform and predefined set of stateless operations._
-- [Wikipedia](https://en.wikipedia.org/wiki/Representational_state_transfer)

In my opinion the rest service is the simplest way of exposing the system functions for the external system to access or update.

If it is a [GET](https://www.w3.org/Protocols/rfc2616/rfc2616-sec9.html) service then the service can be easily accessed using web browsers. All the web pages including this post are rendered by the same mechanism. If the service expecting any HTTP Headers then it has to be manipulated, otherwise it is just invoking the url from the browser.

### Hello World!
I will use the same application created as part of the previous [post](http://ramanan.io/post/2018/01/07/spring-boot/) and add a new rest controller.

Let's create a service, which returns `Hello, world!` when you invoke a url. Follow the below steps:

1. Create a new package inside `src/java/` called `io.ramanan.demo.api`.
2. Create a new java class called HelloWorld.java
3. Annotate the class as `@RestController` and specify the path `/hello`. So the annotation will be `@RestController("/hello")`.
4. Create a public method and annotate the method as `@GetMapping`.
5. Return `Hello, world!` at the end of the method.
6. Run the application and access the url [`http://localhost:8080/hello`](http://localhost:8080/hello)

![hello-world](/assets/images/rest-service.gif)

<script src="https://gist.github.com/ramananp/576e191deb4ef26fc29d78b70c85e902.js"></script>

### Passing Values
The values can be passed as Path Variable like `/ramanan` or Request Param like `?name=ramanan`.

#### Path Variable
 Let's enhance our service to include the path variable.

 1. Update the `@GetMapping` annotation with the path value like `@GetMapping("/hello/{name}")`.
 2. Introduce the argument to the method `public String greet(@PathVariable("name") String name)`.
 3. Run the application and access the url [`http://localhost:8080/hello/ramanan`](http://localhost:8080/hello/ramanan)

![rest-service1](/assets/images/rest-service1.gif)

<script src="https://gist.github.com/ramananp/65676c2af5b23903d7f01c2b59cf0449.js"></script>

#### Request Param
In other way we can pass the value as query parameter or also called request parameter. Let's see how to do that.

1. Update the `@GetMapping` annotation with the path value like `@GetMapping("/hello")`.
2. Introduce the argument to the method `public String greet(@RequestParam("name") String name)`.
3. Run the application and access the url [`http://localhost:8080/hello?name=ramanan`](http://localhost:8080/hello?name=ramanan)

![rest-service2](/assets/images/rest-service2.gif)

<script src="https://gist.github.com/ramananp/7cbb27295043ffabfec3841cd029f260.js"></script>

### Conclusion
We have created a simple rest service, which accepts input value and returns response based on the input. In the next post, I will show you how to test this service using `@SpringBootTest`.

Please feel free to reach me out in twitter if you have any question.