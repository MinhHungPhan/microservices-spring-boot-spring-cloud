# Web Services Key Terminology

## Table of Contents

- [Introduction](#introduction)
- [Key Terminology](#key-terminology)
    - [Request and Response](#request-and-response)
    - [Message Exchange Format](#message-exchange-format)
    - [Service Provider and Consumer](#service-provider-and-consumer)
    - [Service Definition](#service-definition)
    - [Transport](#transport)
- [Conclusion](#conclusion)
- [References](#references)

## Introduction

Welcome to this concise guide on web services key terminology! Throughout our previous videos, we discussed the basic concepts of web services. In this guide, we revisit some crucial terms such as Request, Response, Message Exchange Format, Service Provider, Service Consumer, Service Definition, and Transport. We aim to eliminate any ambiguity surrounding these terms and ensure a solid understanding before proceeding to more complex aspects of the course.

## Key Terminology

### Request and Response

- **Request**: A Request is the input you send to a web service. 
- **Response**: A Response is the output you receive from a web service.

These are the fundamental building blocks of web service interactions. Essentially, you ask something from a web service (request), and it provides you with an answer (response).

### Message Exchange Format

This term refers to the structure of the Request and the Response. They could be in XML, JSON, or any other agreed-upon format. It is like the language used to communicate between the client and the web service.

For instance, you may send a JSON request to a web service and expect a JSON response.

### Service Provider and Consumer

- **Service Provider**: This is the web service that hosts and offers the service. It listens for requests, processes them, and responds accordingly.
- **Service Consumer**: This is the client (it could be an application or another service) that consumes or uses the web service.

Consider an example where a Java application wants to consume a service from a web service. Here, the Java application is the Service Consumer, and the Web Service is the Service Provider.

### Service Definition

The Service Definition is a contract between the Service Provider and the Service Consumer. It describes the structure of the request and response, and where the service is available (the Endpoint).

The Endpoint is the URL at which the service is exposed. It is like the address of the web service. The Service Definition tells the consumer how and where to call the service provided.

### Transport

Transport refers to how the service is accessed. This could be over the Internet (via HTTP) or a Queue (like MQ - Message Queuing). 

- With **HTTP**, the Service Consumer calls the web service using a URL, similar to typing a URL in the web browser. 
- With **MQ**, communication occurs over a Queue. The Service Consumer places a message in the Queue, and the Service Provider listens to the Queue. Upon receiving a request, the Provider processes it, creates a response, and puts it back in the Queue for the Consumer to retrieve.

```plaintex
                        ┌────────────────────┐                  ┌────────────────────┐ 
                        │                    │                  │                    │ 
                        │  Service Consumer  │                  │  Service Provider  │ 
                        │                    │                  │                    │ 
                        └────────────────────┘                  └────────────────────┘ 
                                   ▲                                       ▲           
                                   │                                       │           
                                   │                                       │           
                        ┌──────────│───────────────────────────────────────│──────────┐
                        │          │                                       │          │
                        │          │              SOAP Layer               │          │
                        │          │                                       │          │
                        └──────────│───────────────────┬───────────────────│──────────┘
                                   │                   │                   │           
                                   │                   │                   │           
                                   │            ┌──────────────┐           │           
                                   │            │ SOAP Message │           │           
                                   │            └──────┬───────┘           │           
                                   │                   │                   │           
                                   │                   │                   │           
                        ┌──────────▼───────────────────▼───────────────────▼──────────┐
                        │                                                             │
                        │                        WebSphere MQ                         │
                        │                                                             │
                        └─────────────────────────────────────────────────────────────┘

                                                © Minh Hung Phan
```

## Conclusion

This guide provides a brief recap of the key terminology associated with web services. We hope that these terms and their explanations help clear any misunderstandings, preparing you for the next stages of the course. 

## References

For further reading and understanding of these concepts, refer to:

- [Understanding Web Services- XML, WSDL, SOAP and UDDI](https://www.tutorialspoint.com/wsdl/wsdl_introduction.htm) by TutorialsPoint
- [What is a Web Service?](https://www.w3schools.com/whatis/whatis_webservice.asp) by W3Schools
- [Web services, SOA, and cloud: A guide to key concepts](https://www.infoworld.com/article/2074214/web-services--soa--and-cloud--a-guide-to-key-concepts.html) by InfoWorld

Until our next guide, happy learning!
