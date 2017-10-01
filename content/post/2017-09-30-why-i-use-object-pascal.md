---
title: Why I use Object Pascal
date: 2017-09-29 12:07:41 +0200
draft: true

---
Pascal is one of the older programming languages that are used today. Older in this context means, that it was initially developed in 1969 by Dr. Niklaus Wirth on the ETH of Zurich. Despite the fact, that it is now older than 40(!) years, the language has greatly involved in the last decades. All of the features that are required by a modern programming language are supported by Pascal, too.<!--more-->

Pascal was standardized as an ISO standard in the early 90s. Unlike other languages, there were different Pascal dialects and compilers since the beginning. One of the most favourite versions, which made Pascal one of the most well-known and widespread programming languages of the 80s and the early 90s, was Turbo Pascal.[^1] Today there are two major implementations: **Delphi™**, the official Turbo Pascal successor, and **Free Pascal**.

Delphi is a Rapid Application Development (RAD) environment, which consists of the Object Pascal language, a powerful and fast compiler, a large runtime-library (RTL) and a designer for Graphical User Interfaces (GUI). Delphi runs only on Windows, but can compile programs for GNU/Linux, MacOS, Windows, iOS and Android, too.

[Free Pascal](http://www.freepascal.org) is a free, Open Source implementation of the Object Pascal language. It consists of the language, the compiler and a runtime-library - but does not include the RAD-tools which made Delphi famous. But thanks to some Free Pascal enthusiasts, the [Lazarus IDE](http://www.lazarus-ide.org) was developed as a powerful RAD environment especially for Free Pascal. Both, Free Pascal *and* Lazarus, are highly cross-platform and can run on and compile for different systems, among them are GNU/Linux, Windows, MacOS, BSD.

But beside this historical excursion, what are the reasons that I use Free Pascal in my personal projects?

## Pascal focus on types

Pascal is a compiled, statically-typed language, which requires, that you define the types of all variables, parameters and functions in your code. The compiler will raise an error when you're trying to pass incompatible types to a variable or parameter. The type-safety has one big advantage: it forces you to think about *how to structure your data*. The language offers you many predefined types, but you can also create your own types (which are `Enums`, `Sets`, `Arrays`, `Records` and `Classes`), sub-ranges of existing types or rename existing ones. You even have to differ between subroutines that return values and thus have side-effects, *functions*, and subroutines that does not return something, *procedures*.  It is also possible to overload operators for your types, so you can define the result of the operation when you - for example - add two objects. To pass functions or procedures as data to your code, Free Pascal gives you the possibility to define *procedural types*.

## Object Pascal has full support for OOP

Object Pascal provides you all the tools you need for Object Oriented Programming (OOP). Although the language is not fully object oriented in that way like Smalltalk or Ruby, where even the most basic types like Integers or Booleans are instances of classes (objects), you will find all the concepts that define OOP: encapsulation, inheritance and polymorphism.

You can define you own classes as you would do with the basic types. A class can define *methods* (which are procedures or functions) and *data* (called fields in Object Pascal). It is also possible to define the way on how data is accessed by *properties*, which define which getter- or setter-methods are used to read or write a field. Classes can also inherit other classes, so you can build a hierarchical tree of the classes within your application. The base class of all these classes is `TObject`.

Contracts between your data types and the client code can be defined by the concept of *interfaces*. There are build-in standard *exceptions*, but you can define your own exceptions, too.

## Pascal is modular

Pascal supports programming in a modular way. What is called *packages* or *modules* in languages like Java or JavaScript, is called an `unit` in Pascal. An unit can contain all the code that has a common relation. You can define which data, types or functions of this unit are visible to other parts of your program, this is called the `interface`. And you can also define which parts are not visible to others and thus are private to the unit - this is called the `implementation` part. You can even define code, which gets executed once when the unit is included into your program, the `initialization` part of the unit, and code that gets executed when the program terminates, the `finalization` part.

Units have another advantage: they encapsulate the code in its own namespace. So you can have two or even more procedures with the same name in two different units without an name-collision.

## Pascal is fast

## Pascal is verbose

## Pascal has good documentation

## Pascal has a great community

[^1]: You can read more about the history of Pascal [here](http://wiki.freepascal.org/Object_Pascal_History)