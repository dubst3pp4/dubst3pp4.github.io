---
title: Why I use Object Pascal
date: 2017-09-29 12:07:41 +0200
draft: true

---


Pascal is one of the older programming languages that are used today. Older in this context means, that it was initially developed in 1969 by Dr. Niklaus Wirth on the ETH Zurich. Despite the fact, that it is older than 40(!) years, the language has greatly involved in the last decades. All of the features that are required by a modern programming language are supported by Pascal, too.<!--more-->

Pascal was standardized as an ISO standard in the early 90s. Unlike other languages, there were different Pascal dialects and compilers since the beginning.[^1] Today there are two major implementations: **Delphi™** and **Free Pascal**.

Delphi™ is a Rapid Application Development (RAD) environment, which consists of the Object Pascal language, a powerful and fast compiler, a large runtime-library (RTL) and a designer for Graphical User Interfaces (GUI). Delphi™ runs on Windows but can compile programs for GNU/Linux, MacOS, Windows, iOS and Android.

[Free Pascal](http://www.freepascal.org) is a free, Open Source implementation of the Object Pascal language. It consists of the language, the compiler and also a runtime-library - but does not include the RAD-tools which made Delphi™ famous. But thanks to some Free Pascal enthusiasts, the [Lazarus IDE](http://www.lazarus-ide.org) was developed as a powerful RAD environment for Free Pascal. Both, Free Pascal *and* Lazarus, are highly cross-platform and can run on different systems, among them are GNU/Linux, Windows, MacOS, BSD.

But beside this historical excursion, what are the reasons that I use Free Pascal in my personal projects?

## Full support of OOP

## Pascal is modular

Sourcecode can be organized in units, which are files with code inside, that has a common relation. You can define which parts of the unit are visible to others (`interface`), and which parts are not (`implementation`) and thus private to the unit. You can even define code, which gets executed when the unit is included into your program (`initialization`).

## Type-focused

Free Pascal is static-typed language, that means that you have to declare the types of all variables, parameters and functions in your source code. The compiler will raise an error if you're trying to pass incompatible types to a variable or parameter. The type-safety forces you to think about *how to structure your data*. With Free Pascal you can create your own types (which are `Enums`, `Sets`, `Arrays`, `Records` and `Classes`), sub-ranges of types and you can even rename existing types.

I don't want to start a debate about dynamically-types vs. static-typed languages – I use both of them. But what I really like about Pascal is that it is consequent and does't try to guess how to typecast a type into another one. In contrast, C and C++ for example are not that typesafe like Pascal is.

## It is fast

## It is verbose

## Good documentation

## Community

[^1]: You can read more about the history of Pascal [here](http://wiki.freepascal.org/Object_Pascal_History)