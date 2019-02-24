---
layout: single
title: "Microservices with Vapor"
date: 2019-02-23
categories: posts
classes: wide
tags: vapor server-side swift microservices
---

Vapor provides us with everything needed to create an API Gateway in a Microservices architecture.

## Microservices

A definition of Microservices from [Wikipedia](https://en.wikipedia.org/wiki/Microservices):

*Microservices are a software development technique—a variant of the service-oriented architecture (SOA) architectural style that structures an application as a collection of loosely coupled services.*

## Why?

The topic around monolith vs microservice architecture has already been debated in the software design and architecture community and is beyond the scope of this post. 

Microservices offers a number of benefits some of which includes:

* Clear separation of concerns
* Each service can be deployed independently
* Promotes continues integration and delivery
* Easier to test
* Works great with Docker and Kubernetes
* Scalable

## The API Gateway

As illustrated below, the API Gateway is the external interface and entry point to communicate with all the internal services. It is the API Gateway's responsibility to check and forward each request to the relevant internal services.

![image](/assets/images/microservices-api-gateway.png)

The Gateway Controller will check each request and forward it to the corresponding service:

```swift
func boot(router: Router) throws {
    router.post("users", use: handle)
    ...
}
```

```swift
func handle(_ req: Request) throws -> Future<Response> {
    if req.http.urlString.hasPrefix("/users") {
        guard let usersHost = Environment.get("USERS_HOST") else { throw Abort(.badRequest) }
        return try handle(req, host: usersHost)
    }
    throw Abort(.badRequest)
}
```