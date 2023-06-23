# Web Services Overview

## Table of Contents

- [Introduction](#Introduction)
- [What is a Web Service?](#What-is-a-Web-Service)
- [Web Application vs Web Service](#Web-Application-vs-Web-Service)
- [Why HTML is Not Enough](#Why-HTML-is-Not-Enough)
- [The Role of JARs in Web Services](#The-Role-of-JARs-in-Web-Services)
- [Defining a Web Service: The W3C Criteria](#Defining-a-Web-Service-The-W3C-Criteria)
- [Conclusion](#Conclusion)
- [References](#References)

## Introduction

Welcome, new coder! If you're just starting your journey in web development, you might have heard the term "web service" thrown around. But what exactly is a web service? How does it differ from a typical web application? And how can you create one? This guide is designed to help you understand all of this and more. Let's jump in!

## What is a Web Service?

Imagine you're ordering a pizza online. You choose the size, the toppings, and the crust. Once you're done, you click on 'Order'. In a few moments, the pizza place gets your order and starts preparing your pizza. Here, the pizza place's online ordering system is acting as a web service. It takes your order (input), processes it, and sends it to the pizza place (output).

Now, let's define it in technical terms. A web service is a service that's delivered over the internet and allows applications to communicate with each other over a network. Sounds simple, right? But there's a bit more to it, which we'll explore next.

## Web Application vs Web Service

Let's illustrate this with an example. Suppose I've created a simple 'to-do' application using Java and the Spring MVC framework. This application allows you to login, logout, and manage your tasks. Now, is this a web service? 

Not really. You see, this is a web application designed for human interaction. It delivers its output in HTML, which is great for us humans to read in a browser but not so good for application-to-application interaction. For it to be a web service, it should be designed to interact with other applications, not just humans.

## Why HTML is Not Enough

HTML (HyperText Markup Language) is the standard markup language for documents designed to be displayed in a web browser. It's perfect for designing user interfaces, but it falls short when we want to have application-to-application interaction. Imagine if our pizza ordering system sent its responses in HTML. The other application (say, the pizza place's kitchen display system) would have a hard time deciphering that HTML to understand the order details. 

## The Role of JARs in Web Services

Continuing our 'to-do' application example, one might think we can simply package the business logic into a Java ARchive (JAR) file and let the other application use it. However, it's not that straightforward. The other application would need to install a database, satisfy other dependencies, and handle updates to the business logic. It can get pretty complicated!

## Defining a Web Service: The W3C Criteria

So, how do we define a web service? The World Wide Web Consortium (W3C) provides us with a good definition. According to W3C, a web service is a software system designed to support interoperable machine-to-machine interaction over a network. There are three key components here:

- **Interoperability**: The service should facilitate interaction among different applications, regardless of their underlying technology. This means whether an application is built on Java, .NET, PHP, or any other technology, it should be able to interact with the web service.
- **Machine-to-Machine Interaction**: The service is not designed for human interaction, but for application-to-application communication.
- **Network Communication**: The service should enable communication over a network, not just within a single system.

## Conclusion

And there you have it! We've explored what a web service is, how it differs from a web application, why HTML is not sufficient for application-to-application interaction, and how a web service is defined according to W3C criteria. As you embark on your journey to build your first web service, remember these principles, and you'll be on the right path.

## References

- [Web Services Architecture - World Wide Web Consortium (W3C)](https://www.w3.org/TR/ws-arch/)
- [Web MVC framework - Spring MVC](https://docs.spring.io/spring-framework/docs/current/reference/html/web.html)
- [The Java™ Tutorials - Oracle](https://docs.oracle.com/javase/tutorial/)
