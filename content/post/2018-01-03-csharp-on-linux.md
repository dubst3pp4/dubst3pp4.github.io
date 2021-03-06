---
title: C# and .NET on Linux
date: 2018-03-01 20:46:56 +0100
categories:
- Programming
tags:
- Linux
- CSharp
- ".NET Core"
- Programming

---
C# on Linux exists for a long time, but many users are unaware of this. The languages that are used most today on Linux are still C, C++ and various scripting languages Python, Perl and Ruby. Miguel de Icaza, the founder of the _Gnome Desktop_, was the one who aimed to develop an open, crossplatform C# compiler and Common Language Runtime for Linux, Unix and macOS in 2001. The results suceeded in 2004 in the _Mono_ Project[^1], which is an open implementation of ECMA-334 Standard[^2] which defines the C# language itself and the ECMA-335 Standard[^3] which defines a Common Language Infrastructure for different languages, such as C#.<!--more-->

## The situation on Linux

You may have used or heard of applications like _Banshee_ music player, _F-Spot_, a software for organizing photos or _Tomboy_, a Wiki-like tool for desktop notes. All these applications were developed with Mono and had some remarkable success, but the critics were harsh, Mono at this time somewhat slow and the fear to use something that had to do with Microsoft, the company that has called Linux and the Free Software Movement as "cancer"[^4], was huge.

14 years later, the IT world has changed. Microsoft is not only a member of the Linux Foundation[^5] and a sponsor of the Open Source Initiative[^6], but also open-sourced various of its technologies and tools. The Mono Project still exists and since that time has produced some well known projects like the _Unity Game Engine_[^7], _MonoDevelop_[^8], an IDE to develop C# applications on Linux and _Visual Studio for Mac_[^9]. Nevertheless all of the Mono-based Linux applications like Banshee, F-Spot and Tomboy have died or aren't actively maintained anymore. Unfortunately I'm not aware of a single Linux Desktop application that was made with C# beside MonoDevelop (edit: now I am, the password manager [KeePass2](https://keepass.info) was build with Mono). It seems that the reputation of C# development in the Open Source community is still very bad.

## The licensing question

One of the major critics is the fear, that Microsoft could start a lawsuit against the Mono project. Although the .NET Standard is an open ECMA-Standard, Microsoft holds patents for its own .NET implementation, which is the Microsoft .NET Framework. Mono itself is mainly licensed under the MIT license, with parts being licensed under the BSD and the Apache license[^10]. Microsoft has given a Patent Promise[^11] - not license - that the company will not assert any patents against the project or software written with Mono, as long as the runtime used still implements the full ECMA-335 Standard. And until today Microsoft did not take any legal actions against Mono, but to the surprise of everyone purchased Xamarin Inc.[^12] in 2016, the company of Miguel de Icaza, which is the main developer of the Mono project. Microsoft even affirmed that they are interested to support and to continue the Open Source .NET implementation[^13].

In the same year Microsoft released its own open and crossplatform .NET implementation, called _.NET Core_[^14]. .NET Core runs on Linux, macOS and Windows. .NET Core itself is also licensed under the MIT-License[^15] with an similar additional "Patent Promise for .NET Libraries and Runtime Components"[^16]. Again Microsoft assures, not to "assert any .NET patents" against developers for "making, using, selling, offering for sale, importing, or distributing Covered Code" as long as the code is part of any compliant .NET runtime implementation (that follows the ECMA-335 standard) or is designed to run on such an implementation. In other words, as long as your code which is using the .NET libraries or code that you modified runs under .NET, .NET Core or Mono, everything is fine. When you try to reimplement patented code on any other runtime (like Java, Ruby etc.) or when you try to strip down a .NET runtime to a subset of the ECMA standard, then you could get in trouble.

Of course this promise is discussed very controversal in the Open Source community. You don't have the full freedom to do what you want with the software, as you would perhaps expect from a license such as the MIT license. But from my point of view, this is an similar situation with Oracle, which holds patents on parts of the Java language and its JRE/JDK. Even Google owns patents regarding the Go programming language. At least each user has to decide for his self if he/her can live with these restrictions. But as Microsoft is highly interested in attrating developers and - unlike 20 years ago - not a platform but the ecosystem is the most important value of an IT company, it is very unlikely that Microsoft will drop its Open Source initiatives or will chase developers by starting lawsuits.

Do you already use or plan to use C# / .NET Core on Linux?

[^1]: http://www.mono-project.com
[^2]: https://www.ecma-international.org/publications/standards/Ecma-334.htm
[^3]: https://www.ecma-international.org/publications/standards/Ecma-335.htm
[^4]: https://www.theregister.co.uk/2001/06/02/ballmer_linux_is_a_cancer
[^5]: https://www.linuxfoundation.org/press-release/microsoft-fortifies-commitment-to-open-source-becomes-linux-foundation-platinum-member
[^6]: https://opensource.org/node/901
[^7]: https://unity3d.com
[^8]: http://www.monodevelop.com
[^9]: https://www.visualstudio.com/vs/visual-studio-mac
[^10]: https://github.com/mono/mono/blob/master/LICENSE
[^11]: https://github.com/mono/mono/blob/master/PATENTS.TXT
[^12]: https://www.xamarin.com
[^13]: https://blogs.microsoft.com/blog/2016/02/24/microsoft-to-acquire-xamarin-and-empower-more-developers-to-build-apps-on-any-device
[^14]: https://dotnet.github.io
[^15]: https://github.com/dotnet/core/blob/master/LICENSE.TXT
[^16]: https://github.com/dotnet/coreclr/blob/master/PATENTS.TXT

