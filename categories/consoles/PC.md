---
permalink: /pc/
layout: post
title: IBM-PC & Compatibles
recommend: pc
recommendTitle: All PC Posts
editlink: ../categories/consoles/PC.md
console: 'pc'
consoleimage: /public/consoles/Computer Old Design.png
breadcrumbs:
  - name: Home
    url: /
  - name: Consoles
    url: /
  - name: PC
    url: #
---

# Introduction
Welcome to our page dedicated to PC reverse engineering! PCs are some of the most versatile and widely-used computing platforms in the world, and there's no shortage of interesting and challenging reverse engineering topics to explore. If you're interested in learning more about the technical aspects of PCs and how they work, you've come to the right place. 

On this page, we've compiled a list of links to other pages that cover various topics related to PC reverse engineering. Whether you're interested in understanding the hardware architecture of retro CPUs and GPUs, analyzing software at the binary level, or exploring the many mods and hacks that have been created by enthusiasts over the years, you'll find a wealth of resources and information on the pages we've linked to. 

So grab your keyboard and mouse, and get ready to dive into the exciting world of PC reverse engineering!

---
# DOS

## DOS Gaming Aspect Ratio - 320x200
The Youtuber **Displaced Gamers** has an excellent video explaining the common DOS aspect ratio:
<iframe width="560" height="315" src="https://www.youtube.com/embed/YvckyWxHAIw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

---
## 32-bit DOS Applications
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/EDl9qBZ9Bb0?controls=0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
The video discusses the 640k memory limitation of DOS and why many DOS games require more than 1MB of memory. The 16-bit x86 architecture used a trick to address up to one megabyte of memory, which became a limitation as software became more complicated. DOS extenders were developed to allow 32-bit memory access with almost no performance penalty, enabling 32-bit games to run on 16-bit MS-DOS. DOS extenders were based on the DPMI specification, providing larger memory access and multitasking capabilities. Developers only needed to know how to use the correct DOS external functions when mode switching was necessary. The use of DOS extenders extended the lifespan of MS-DOS and its legacy is engraved into the memory of classic DOS games, which shaped the video game industry.

### Real Mode
Real mode is a processor mode in the x86 architecture where the CPU can directly access the first 1MB of memory. In real mode, the CPU uses 16-bit registers and addresses memory using 20-bit addresses that are formed by combining a 16-bit segment address with a 16-bit offset address. Real mode is the default mode of operation for the x86 CPU, and it was used in early versions of MS-DOS.

### Protected Mode
Protected mode is another processor mode in the x86 architecture that allows the CPU to access more than 1MB of memory, up to 4GB. Protected mode uses a different memory addressing scheme, called linear addressing, where memory is addressed using 32-bit addresses. Protected mode also provides hardware-based memory protection and multitasking capabilities, which make it suitable for modern operating systems like Windows and Linux. Protected mode is used by modern operating systems, and it requires a transition from real mode to enter this mode of operation.

### DOS Extenders
DOS extenders work by extending the 16-bit real mode of the x86 architecture to allow 32-bit applications to run on the platform. In real mode, applications can only access up to 1MB of memory. DOS extenders enable applications to access more memory by running in protected mode, which allows them to use up to 4GB of memory.

DOS extenders operate by adding an additional layer between the application and the operating system. This layer intercepts certain system calls made by the application and provides additional functionality. The extender provides a set of APIs that allow the application to access memory beyond the 1MB limit and other system services that are not available in real mode.

The DOS extender typically consists of a small loader program and a runtime library that is linked with the application. When the application is launched, the loader program loads the extender and initializes it. The extender then sets up a protected mode environment and transfers control back to the application, which can now use 32-bit instructions and access more memory.

The use of DOS extenders allows applications to take full advantage of the capabilities of the x86 architecture, and it played a crucial role in the development of early PC games. DOS extenders were particularly important for games that required a lot of memory and high-performance graphics, as they allowed developers to create games that pushed the limits of the platform.

#### DPMI - DOS Protected Mode Interface
DPMI stands for "DOS Protected Mode Interface" It is a specification that provides a way for DOS applications to run in protected mode, which allows them to access more memory and run more efficiently. DPMI was developed in the late 1980s and early 1990s, during a time when the transition from 16-bit to 32-bit computing was taking place. DPMI provides a set of services that allow DOS applications to run in a protected environment, including virtual memory management, task switching, and interrupt handling. It was used extensively in the development of DOS extenders, which allowed 32-bit applications to run on DOS systems. The DPMI specification was widely adopted and helped to extend the life of the DOS platform well into the 1990s.

DPMI was created by Microsoft in the late 1980s as part of their work on the Windows 3.0 operating system. It was developed to standardize the use of DOS extenders and allow applications using them to run under the protected mode environment of Windows 3.0.

#### Popular DOS Extenders
Some popular DOS extenders include:
* DOS4GW - bundled with the Watcom C/C++ compiler, and used by many popular games such as Doom and Duke Nukem 3D.
* CauseWay - an open-source extender that was designed to be small and fast.
* CWSDPMI - a DPMI implementation for use with the DJGPP compiler.
* DOS/32A - an extender designed for use with the Borland C/C++ compiler.
* DOS/4G - a commercial extender used by many games and applications.

---
## DOS Game Modding

### DOS Game Corruption
If You are using a browser-based DOSBox emulator to run your games you can add this bookmarklet to your browser for it to automatically corrupt random memory addresses inside the DOS game:
[jsRTC/jsRTC_for_js-dosbox.txt at master · redscientistlabs/jsRTC](https://github.com/redscientistlabs/jsRTC/blob/master/jsRTC_for_js-dosbox.txt)

---
## DOS Game Reverse Engineering

### Reverse Engineering Strike Commander
Fabien Sanglard has an excellent series of articles on how he reverse engineered the classic flight simuator **Strike Commander**:
[Reverse Engineering Strike Commander](https://fabiensanglard.net/reverse_engineering_strike_commander/index.php)

---
# MSX
The MSX was a standard introducted by **Microsoft Japan** to make sure no matter which manufacturer build the PC (e.g Sony, Panasonic, Philips) they would all be able to run the same software.
There were three different revisions of the MSX:
* MSX
* MSX2
* MSX Turbo R

## Introduction to the technology of the MSX
The best video I have found on the MSX is by the Youtuber **Displaced Gamers** where he goes through all the variations of the MSX (MSX2 etc) and explains the hardware limitations and the impressive feats developers managed to accomplish on the systems:
<iframe width="560" height="315" src="https://www.youtube.com/embed/AFRf87SqWrw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## MSX Games
While the MSX system is most famous for Konami games like Vampire Killer (Castlevania) and Metal Gear there are quite a few games worth playing for the system. What better video to show off the MSX games than the **Game Sack** episode on the topic:
<iframe width="560" height="315" src="https://www.youtube.com/embed/4R779hMGGC4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

---
# All Posts
<div>

{% include console.html %}
</div>
