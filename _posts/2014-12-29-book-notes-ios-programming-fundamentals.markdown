---
layout: post
title:  "[Book] iOS 7 Programming Fundamentals"
date:   2014-12-29 15:38:28
categories: book
---

## Chapter 1: Overview of C
Skipped

## Chapter 2: Introduction to Obj-C
Skipped

## Chapter 3: Syntax

#### Blocks
A block retains the params it was executed with even after its variables have been dereferenced. Grand Central utilizes mean blocks.

    __block UIBackgroundTaskIdentifier bti = [[UIApplication sharedApplication] beginBackgroundTaskWithExpirationHandler: ^{ [[UIApplication sharedApplication] endBackgroundTask:bti];
    	}];

Notice how block is referenced in itself where beginBackgroundTaskWithExpirationHandler takes a block as a parameter.

## Chapter 4: Object Oriented Programming

#### Classes
A subclass inherits the methods of it's superclass. To write code for a class you need an `interface` and an `implementation`.

    @interface MyFirstClass : NSObject
    - (NSString*) helloJarvis;
    @end
    @implementation MyFirstClass
    - (NSString*) helloJarvis {
    	return @"Good Morning Sir..."
    }
    @end


