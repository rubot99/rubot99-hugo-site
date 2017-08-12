+++
tags = ["book-review","development"]
categories = ["books"]
date = "2017-08-12T21:00:00Z"
title = "Review - Refactoring - Improving the design of existing code - Part 3"
keywords = ["refactoring", "development", "software", "book"]

+++

### Chapter 3

This chapter is all about various code smells and how we can try to identify them. 
The first code smell is duplicated code. Duplicated code means more places to make code changes and higher risks of bugs being added. The best way to fix this issue is to either extract the code into a new method or into a different class.

<!--more-->

Switch statements are another code smell. Switch statements often have a lot of duplicated code. Use polymorphism to replace switch statements. 
Long methods are another code smell. Long methods make it difficult to understand the purpose of the code. Long methods always end up doing more than one thing, methods should have one responsibility (SRP). This makes it easier to understand the code and modify in the future. Good naming of methods helps a reader understand the purpose of the method. Modern languages have eliminated the overhead of in process calls, allowing smaller methods without effecting performance. Another good rule of thumb is that blocks of code that need comments are ideal candidates for decomposing into smaller methods. Large classes should also be decomposed into sub classes or extracted into other classes. Methods with long parameter lists should be reduced for readability by using objects instead.
So far we have mentioned splitting classes and methods, but sometimes you will need to merge classes and methods. This will help to bring methods that have similar purposes to be together, making it easier to modify and understand. 
If there are classes that only pass information from one class to a client, then it might be worth removing the middleman class. Remove unwanted abstraction that is not required. Temporary fields are also another form of code smell and make code to be difficult to debug and modify. Data model class might be considered also as code smells. Poor inheritance is a code smell this is where class inherits behaviours from a super class that it does not require. Classes that overly use another classes private methods and variable is a break of the encapsulation rule. Finally comments can be a code smell, instead of simplifying complex code the use of comments is a way to allow the reader to understand it better. Often code is modified but the comments aren’t which will causes further complications for the reader.  
