---
layout: single
title: "Functional Programming in Swift"
date: 2019-03-23
categories: posts
classes: wide
tags: swift functional programming swiftlang ios
---

What is functional programming ...

A mindset, how you think about structuring your code.

Safer, easier to debug and maintain.

Everything is a function, you take an input and produce an output

## Imperative vs Functional

With imperative style you write code in a specific order, one line after the other mutating and maintaining state along the way.

Example of a none-function way of writing code using the imperative style:

...

Example of a functional way of writing code:

Expressing things as functions

...

## Immutability and Side Effects

The main goal of functional programming is to avoid side effects.

A side effect is anything a function might do which isn't computing the output from the input given and return that output.

Example of the above statement:

Example would be where the function mutate a variable in the global state. So it doesn't depend solely on the input given.

...

## First-Class and Higher-Order Functions

## Swift's Higher-Order Functions

Explain how in Swift you can have another function as input in another function and also return a function in turn.

Swift built in higher-order functions:

Avoid iterating where possible

Show examples of the typical iteration approach and then using the higher-order functions

### filter

### map

### reduce

## Pure Functions

A pure function is the opposite of side effects. It only depends on the input given, compute that and returns the output, nothing else.

Example of a pure function:

...

## Avoid mutating data

Avoid changing data in place. Mutable state is dangerous.

Explain how mutating in place can cause issue where you make assumption of what the data should be but somewhere in your code you mutated a value and forgot about it. This leads into unpredictable behavior and bugs which is hard to debug. This about of all data being immutable to make it predictable, make mutable copies of data and use that instead.

Example of mutating data in place:

...

## Persistent data structures for efficient immutability

Explain the issue (effiecency, more memory) with making mutable copies and how to avoid that using persistent data structures. Hash trees etc,

