---
layout: single
title: "Building containerized microservices using Go (Part 1/5)"
date: 2021-05-26
header:
    image: /assets/images/containerized-microservices-go.png
    teaser: /assets/images/containerized-microservices-go.png
classes: wide
categories: posts
tags: go golang go-gin gorm webservices microservices docker dockerfile container containerize devops
---

Today I'm kicking of part 1 of a 5-part series taking a closer look at how to build, test, and deploy scalable containerized microservices using Go. We'll take a deep dive into topics like Docker, Kubernetes, Terraform, and AWS.

**Containerization** provides a clean separation of concerns, as developers focus on their application logic and dependencies, while IT operations teams (DevOps) can focus on deployment and management without bothering with application details such as specific software versions and configurations specific to the app.

**Microservices** are a specialization of an implementation approach for service-oriented architectures (SOA) used to build flexible, independently deployable software applications. Services in a microservice architecture are processes that communicate with each other over a network (typically HTTP) in order to fulfill a goal.

**Go** is a statically typed, compiled programming language specifically engineered with simplicity and ease of use in mind.

## Why Go?

GoLang (Go) was first created by Google back in 2007 to improve programming productivity in an era of multicore, networked machines and large codebases. Go is still a relatively new programming language compared to Java and C# but has already seen widespread adoption in the software development community. Go was explicitly engineered with simplicity in mind, making life easier for “the everyday programmer” and is considered by many as their general-purpose backend language.

According to a [survey done by JetBrains](https://blog.jetbrains.com/go/2021/02/03/the-state-of-go/), Go is among the top 10 primary languages of professional developers. Some tech giants like Gooogle, Uber, Dropbox, and Twitch are all using Go in large scale production systems.

**A few advantages when choosing Go for your next project:**

- Easy to learn and to get started
- Being a compiled language, Go is extremly fast
- Statically typed
- Automatic garbage collection
- Simple concurrency primitives for multi-core processing
- Native binaries
- Fast compile times
- Great tooling
- Very active and supportive community

## Prerequisites

- A working [Go environment](https://golang.org/doc/install)
- A basic level of understanding of the [Go programming language](https://golang.org/doc/)
- A solid understanding of REST, API design, HTTP, and microservices architecture
- Having [Docker installed](https://docs.docker.com/get-docker/) in your environment
- A basic level of understanding [working with Docker](https://docs.docker.com/reference/)

## What we're going to build

Throughout this series we will focus on building a **single microservice** which you can assume is part of a bigger microservices architecture for an e-commerce platform.

**Functional requirements:**

- Build a service to manage the inventory of our an e-commerce platform
- Inventory data needs be stored in a PostgreSQL database
- The service needs to be accessible to other microservices in our architecture

**Non-functional requirements:**

- The service should be packaged and deployed independently
- Our service should be able to scale easily
- Downtime should be avoided at all costs

## Getting started

With all the boring stuff out of the way, it's time to get our hards dirty writing some code. Let's get started with building our microservice in Go.

### Project Structure

We will be splitting up our microservice application into logical layers to

### Models

Entities (objects) in our application

### Control


- models
- controllers
- 

## JWT

## Third-party libraries

- gogin
- gorm

## Containerize

- why containerize it

- creating a docker image (Dockerfile)
- building the image
- running the container


## Wrapping up