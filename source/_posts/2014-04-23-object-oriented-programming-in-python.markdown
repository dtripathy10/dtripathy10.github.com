---
layout: post
title: "Object Oriented Programming in Python"
date: 2014-04-23 10:07:11 +0530
comments: true
categories: [Python, Object Oriented Programming Languages]
---

To Study any object oriented programming language, that may be dynamic type language like python, ruby or static
 type language like c++,java one has to learn/ask the following questions? If you are able to answer these 
 questions, then I think you can write object oriented programming in any programming language obviously that 
 should support the object oriented features. The questions are :-

* How to create a class with the specific properties
  * Constructor
  * Destructor
  * Public, Private or Protected accee speicifer using instance method and properties
  * Static instance or properties
* How to cretae a Object
* Inheritance
* Multiple Inheritance
* Method overloading and method overridding
* Special method of a class (Default base class and their inheritated method)
* Operator Overloading



### How to create a class with the specific properties

Let's see a example of a class in python - 

```python

'''
1. If the name of a Python function, class method, or attribute starts with 
(but doesn't end with) two underscores, It's private; everything else is public. 
Python has no concept of protected class methods (accessible only in their
own class and descendant classes). Class methods are either 
private (accessible only in their own class) or public (accessible from anywhere).

'''
class Employee:
   empCount = 0 ## public static variable
   __empC = 0   ## private static varibale

   ## constructor
   def __init__(self, name, salary):
      self.name = name
      self.salary = salary ## public state variable
      self.__privateField = 4 ##private state variable
      Employee.empCount += 1

   ## public instance method
   def displayCount(self):
     print "Total Employee %d" % Employee.empCount

   ## public instance method
   def displayEmployee(self):
      print "Name : ", self.name,  ", Salary: ", self.salary

   ## private instance method
   def __private():
   	  print "private method is called"

   ## private static method
   @staticmethod
   def __static_method():
   	  print "I am a private static mehtod"

   ## public static method
   @staticmethod
   def static_method():
   	  print "I am a public static mehtod"

   ## destructor
   def __del__(self):
      print "I am dieing"

```
###  How to cretae a Object

How to create the object and access the various properties and method
in python. we can undestand by using below example and I used the previous class
as base

```python

emp =  Employee("XYZ",321) ## creating object in python
print emp.salary ## accessing public instance variable
print Employee.empCount ## accessing public static variable
print Employee.static_method() ## accessing public static method
print emp.displayEmployee() ## accessing public instance method 
print emp.__private() ## Accessing private  method, we get AttributeError

```


### Inheritance

### Multiple Inheritance

###  Method overloading and method overridding

###  Special method of a class

###  Operator Overloading






