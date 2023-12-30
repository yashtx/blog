---
layout: post
title:  "Value, object, types and classes in python"
date:   2021-10-17 15:20:31 +0530
permalink: /votc/
---

When i was learning Python, i used to get confused between value, type, object and classes. Understanding these concepts are important for learning Object Oriented programming. So, i hope this post helps.

### Value and objects

A value is one of the basic things a program works with, like a letter or a number.
Some value are `2`, `42.0` and `'hello'`. These values belongs to different types.

Objects are python's abstraction for data. All data in python program is represented by objects or relation between objects. An object has an `identity`, `value` and `type`.

Difference in value and object is that two different object may have the same value.

``` python
>>> a = 'hello'
>>> b = 'hello'
>>> a is b
    False
>>> a == b 
    True
```
In python, `==` Operator checks the identity of objects based on its value. When you use `is` operator you are checking object identity.

The value of some objects can change. Objects whose value can change are said to be `mutable`; objects whoses value is unchanged once they are created are called `immutable`.

``` python
>>> a = 1            # immutable
>>> b = 'two'        # immutable
>>> c = [a, b, c]    # mutable 
```
Three object assigned to the names `a, b and c`  names can be reassigned at any point.
Every object in python has a type. It types can be discovered by calling the `'type'` built in function. the type is an object too, so it has type of its own, which is called type.

``` python
>>> type(42)
    <class 'int'>
>>> type(type(42))
    <class 'type'>
```

### Classes
Classes is a mechanism python gives us to create new user defined types from python code.

``` python
>>> class hello: pass
>>> y = hello()
>>> type(y)
    <class '__main__.hello'>
```

Using class mechanism we've created `hello` a user defined type. `'y'` is instance of the class `'hello'` . In another word, it is an object and its type is `hello` .

As any other type `'hello'` is object itself and it has type too. this type is `'type'`.

``` python
>>> type(type(y))
    <class 'type'>
```

The term class and type are an example of two name referring to same concept.
To avoid this confusion, try to say 'type' when you mean a type, and `"user-defined class"` (user defined type) when referring to new type created using class construct.

### Instance 

Instance is synonymous to object. Think of it this way. object are instance of types, so `'42'` is an instance of `'type int'` is equivalent to `'42 is an int object'`.