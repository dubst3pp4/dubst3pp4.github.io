---
title: 2018 01 03 Csharp on Linux
date: 2018-03-01 20:46:56 +0100
draft: true

---
C# on Linux exists for a long time, but many users are unaware of this. The languages that are still used mostly today on our OS are C, C++ and various scripting languages Python, Perl and Ruby. Miguel de Icaza, the founder of the Gnome Desktop, was the one who aimed to develop an open, crossplatform C# compiler and Common Language Runtime for Linux, Unix and macOS in 2001. The results suceeded in the Mono Project, which is an open implementation of the .NET ECMA-335 Standard and provides a compiler for the C# ECMA-334 Standard and was released in its first version in 2004.<!--more-->

You may have used or heard of applications like Banshee, a music player, F-Spot, a software for organizing photos or Tomboy, a Wiki-like desktop notes tool. All these tools were developed with Mono and had some success, but the critics were harsh, Mono at this time somewhat slow and the fear to use something that had to do with Microsoft, the company that has called Linux and the Free Software Movement as "cancer", was huge. 

14 years later, the world has changed. Microsoft is not only a member of the Linux foundation, it also open-sourced various technologies and tools. The Mono Project still exists and has produced well known projects like the Unity Game Engine, MonoDevelop, an IDE to develop C# applications on Linux and Visual Studio for Mac. Nevertheless the Banshee, F-Spot and Tomboy died and aren't activly maintained. And I'm not aware of a single Linux Desktop application that was made with C# beside MonoDevelop. It seems that the reputation of C# development in the Open Source community is still very bad.

One of the major critics is the fear, that Microsoft could start a lawsuit against the Mono project. Although the .NET Standard is an open ECMA-Standard, Microsoft holds patents for its own .NET implementation, which is the Microsoft .NET Framework. But until today, Microsoft didn't start a battle against Mono, but in 2016 purchased the company of Miguel de Icaza, Xamarin, which is the main developer of the Mono project. Microsoft even confirmed, that they are interested to support and to continue the Open Source .NET implementation.

In the same year, Microsoft released its own open and crossplatform .NET implementation, called .NET Core. .NET Core runs on Linux, macOS and Windows. To my surprise, it doesn't feel like an alien on Linux, but provides a very comfortable CLI to build and scaffold applications or to manage dependencies. .NET Core itself is licensed under the MIT-License with an additional "Patent Promise for .NET Libraries and Runtime Components". With this promise, Microsoft assures, not to "assert any .NET patents" against developers for "making, using, selling, offering for sale, importing, or distributing Covered Code" as long as the code is part of any compliant .NET runtime implementation (that follows the ECMA-335 standard) or is designed to run on such an implementation. In other words, as long as your code runs under .NET, .NET Core or Mono, everything is fine. When you try to reimplement code on any other runtime (like Java, Ruby etc.) or when you try to strip down a .NET runtime, things look bad. This promise is discussed very controversal in the Open Source movement. From my point of view, this is the same situation as with the Java language and runtime and Oracle or the Go programming language and Google. All those companies own patents for the language and runtime implementations and grant the users to modify and redistribute those implementations under certain circumstances.




