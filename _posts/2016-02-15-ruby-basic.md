---
layout: post
title: Ruby Basics
excerpt: "Basics for ruby"
modified: 2016-02-15
tags: [intro, beginner, basics, ruby, tutorial]
comments: true
---

Ruby is...

> A **dynamic**, open source programming language with a focus on **simplicity** and **productivity**. It has an elegant syntax that is natural to read and easy to write.

{% highlight code %}
Ruby = Ruby programming language + Ruby virtual machine + core & standard API
{% endhighlight %}

## TL;DR
* Everything is an object.
* Objects are instances of class.
* 3 special classes: `Class` -> `Module` -> `Object`.
* Basic data types: Boolean, Symbol, Number, String, Array, Hash.



There only instance methods and singleton methods, class methods are just singleton methods of Class instances.

Class made of: constant, class method, instance method, class variable, instance variable, class instance variable.

class, instance, class instance variables are implicitly private.

All the classes in a class hierarchy actually share one class variable. Class instance variables should usually be preferred over class variables.

Everything is an object + classes are instances of class Class + object has class/instance method, class/instance variables, constants.

Module made of: constant, instance method, module method.
