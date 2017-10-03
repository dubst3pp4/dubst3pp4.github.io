---
title: Why I use Object Pascal
date: 2017-09-29 12:07:41 +0200
draft: true

---
Pascal is considered by many programmers as an old language from the past. And although it is in fact one of the older programming languages, it has greatly evolved into a modern, full featured language over the last decades.<!--more-->

Pascal was initially developed in 1969 by Dr. Niklaus Wirth on the ETH of Zurich. It was used as a teaching language as well as a language for business applications. With the appearance of the Classic Mac OS, Pascal was the language of choice propagated by Apple for serious application development. As an example, the first version of Photoshop was made with Pascal.[^1](http://www.computerhistory.org/atchm/adobe-photoshop-source-code)

Pascal was standardized as an ISO standard in the early 90s. But unlike other languages, there were different Pascal dialects and compilers since the very beginning. One of the most favourite versions, which made Pascal one of the most well-known and widespread programming languages of the 80s and the early 90s, was Borlands *Turbo Pascal*[^2](http://turbopascal.org). Over time some object-oriented additions were added to the language by Apple and later by Borland, which has evolved into what we now call **Object Pascal**.[^3]

Today there are two major implementations: **[Delphi](https://www.embarcadero.com/products/delphi)**, the official Turbo Pascal successor, and **[Free Pascal](http://www.freepascal.org)**.

Delphi is a commercial Rapid Application Development (RAD) environment, which consists of the Object Pascal language, a powerful and fast compiler, a large runtime-library (RTL) and a designer for crossplatform Graphical User Interfaces (GUI). Delphi runs only on Windows, but can compile programs for GNU/Linux, MacOS, Windows, iOS and Android, too.

Free Pascal in contrast is a free, Open Source implementation of the Object Pascal language. It consists of the language, the compiler and a runtime-library - but does not include the RAD-tools which made Delphi famous. But thanks to some Free Pascal enthusiasts, the **[Lazarus IDE](http://www.lazarus-ide.org)** was developed as a powerful RAD environment especially for Free Pascal. Both, Free Pascal *and* Lazarus, are highly cross-platform and can run on and compile for different systems, among them are GNU/Linux, Windows, MacOS, BSD.

But beside this historical excursion, what are the reasons that I use Free Pascal in my personal projects?

## Pascal focus on types

Pascal is a compiled, statically-typed language, which requires, that you define the types of all variables, parameters and functions in your code. The compiler will instantly raise an error when you're trying to pass incompatible types to a variable or parameter. The type-safety has one big advantage: it forces you to think about *how to structure your data*.

The language offers many predefined types, but you can also define your own types. For this task Pascal offers you *Enumerations*, *Sets*, *Arrays*, *Records* and *Classes*. It is even possible to create sub-ranges of types or to rename existing ones.

Pascal is very strict, so the programmer has to differ between subroutines that return values and thus have side-effects, in Pascal called *functions*, and subroutines that does not return something, called *procedures*. Functions and procedures can also be passed to variables or other functions thanks to *procedural types*.

It is possible to overload operators for specific types. With this feature, you have the power to define, let's say, the result of the addition operation of two or more instances of the same class.

## Object Pascal has full support for OOP

Object Pascal provides you all the tools you need for modern Object Oriented Programming (OOP). Although the language is not fully object oriented in that sense like Smalltalk or Ruby, where even the most basic data types are instances of classes, you will find all the concepts that define OOP in the Object Pascal language: *encapsulation*, *inheritance* and *polymorphism*.

You can define complex types with the help of classes. A class can define *methods*, which are procedures or functions, and *data*, called fields in Object Pascal. It is also possible to define the way of *how* data is accessed by a feature called *properties*. Properties define which getter- or setter-methods are used to read or write a field. Classes can also inherit other classes, so you can build a hierarchical tree of the data and behaviour you have modelled within your application. The base class of all classes is `TObject`.

*Interfaces* are also a part of Object Pascal as well as *Exceptions*. You can use the build-in standard exceptions, but you have of course the freedom to define your own exceptions. *Class helpers* are comparable with Smalltalks or PHPs traits (although not exactly the same) and let you add methods to existing classes without the need to derive a new class.

Further features are *Generics* to define classes that apply to a wide range of types, as well as many predefined classes for advanced data structures like lists, dictionaries, streams and many many more.

For an in-depth overview of all the modern OOP features, I recommend an excellent article written by Michalis Kamburelis, which is called *Modern Object Pascal Introduction for Programmers*[^4].

## Pascal is modular

Pascal supports programming in a modular way. What is called *packages* or *modules* in other languages like Java or JavaScript, is called an `unit` in Pascal.

An unit can contain all the code that has a common relation. You can define which data, types or functions of this unit are visible to other parts of your program - this is called the `interface`. And you can also define which parts are not visible to others and thus are private to the unit - this is called the `implementation` part. You can even define code, which gets executed once when the unit is included into your program, the `initialization` part of the unit, and code that gets executed when the program terminates, the `finalization` part.

Units have another advantage: they encapsulate the code in its own namespace. So you can have for example two or even more procedures with the same name in two different units without a name-collision.

## Pascal is fast

One of the reasons why the early Turbo Pascal was a huge success was the speed of the compiler. Even on older hardware code was compiled in a few seconds. In comparison to other compilers this is still true today.

But despite the fast compilation of code, the compiled code itself is very competitive to applications developed in plain C, C++ or Java due to the highly optimization for different processor architectures, allowing the program to run at a very high speed and with little memory consumption.[^5]

## Pascal is verbose

This is maybe the fact, that most developers are annoyed about: the absence of braces and the very verbose syntax of the language. As an example, instead of opening and closing braces, Pascal uses the `begin` and `end` keywords for blocks. The `if` keyword is complemented by the word `then`. As you can see, the whole syntax is readable like plain English. If you start to cry now, you should consider one important question by yourself: *What is more important?* The ability to have a short syntax to write code fast *or* the possibility to read and understand code that was written by other developers or even by you a year ago? I'm in favour of the second fact and I really enjoy that verboseness.

## Pascal has good documentation

A language without a good documentation is only half the value. The team behind Free Pascal has done a very good job. You can browse the whole language documentation as well as the documention about the compiler itself, the *Runtime Library (RTL)*, *Free Component Library (FCL)* and the *Lazarus Component Library (LCL)*[^6]. In addition to this you will find many examples in the *Free Pascal Wiki*[^7], but this takes us to the fact that...

## Pascal has a great community

Beside the official wiki, there is also an official forum[^8] where Free Pascal and Lazarus users will answer your questions. If you're active on Google+ you can have a look at the *Google+ Free Pascal / Lazarus IDE Community*[^9], too. There are several (althoug not many) Object Pascal related conferences as well as some local Free Pascal and Lazarus meetups. And with the *Blaise Pascal Magazine*[^10] you will find a regular publication which offers a broad selection of articles about Delphi, Free Pascal, Lazarus and Object Pascal in general.

## Conclusion

Object Pascal is really worth a look. Don't let you discourage by people that tell you that Pascal is out of date. It is definetly not! There are many great projects out there that prove how strong the language is: from the Lazarus IDE itself to high performance 3D-Game engines like the *Castle Game Engine*[^11], which compiles your games for Android and iOS, too. If you're interested in the path aside of the mainstream languages, have a look at some of the resources I mentioned. Or simply install Free Pascal and Lazarus and try out the language for yourself!

[^3]: You can read more about the history of Pascal at http://wiki.freepascal.org/Object_Pascal_History
[^4]: http://castle-engine.io/modern_pascal_introduction.html
[^5]: You can see a performance benchmark at http://benchmarksgame.alioth.debian.org/u64q/pascal.html
[^6]: http://www.freepascal.org/docs.var
[^7]: http://wiki.freepascal.org
[^8]: https://forum.lazarus.freepascal.org
[^9]: https://plus.google.com/communities/114860965042324270757
[^10]: http://www.blaisepascal.eu
[^11]: http://castle-engine.io