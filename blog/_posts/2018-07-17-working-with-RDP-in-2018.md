---
layout: post
title:  "Working with Remote Desktop Protocol in 2018"
date:   2018-07-17 09:09:13 -0400
categories: IT cmd networking
---

<h2>Introduction</h2>

"Remote desktop" is designed to allow remote control of a computer, with many capabilities rendered accessible in the same type of fashion as if you were physically at the workstation.
There are pros and cons to using Remote Desktop Protocol (Known as RDP, and also as RDC for Remote Desktop Connection). Much of it depends on which <b>form</b> of remote desktop software you chose to use.
In this blog post, I will detail the options we have right now in this time, and the different past configurations we used that lead up to what we currently use.


<h1>The beginning</h1>
From Windows XP and onwards, every version of Windows has included a form of RDP accessibility.
The first version, known as <b>"4.0 Terminal Services Client"</b> was released along with "terminal services" as part of <i>Microsoft Windows NT 4.0 Server, Terminal Server Edition</i>. The protocol was based on the <b>model ITU-T T.128</b> example from the <b>T.120</b> recommendation series.
The company Citrix had a <i>"MultiWin"</i> technology which was previously used in windows 3.1 to support multiple logins. Microsoft called upon Citrix to use this technology in the design of the 4.0 model.
The DLLs used in this were still branded with Citrix, rather than Microsoft. When 5.0 came around with the release of <b>Windows 2000 Server</b> it included many improvements to the design, including the functionality to support printing, and streamlined network bandwidth usage.

<h1>Evolution</h1>
With the release of Windows XP and RDC <b>version 5.1</b>, the name of the technology was officially re-branded from <i>Terminal Services Client</i> to <i>Remote Desktop Connection</i> as it would be known from there onwards.
This was the first time that audio was available to be streamed through remote services, as well as 24-bit color display. 

<b>Version 5.2</b> coincided with the release of <i>Windows Server 2003</i> and would be used in the future with <i>Windows XP Professional x64 Edition</i>.
This was the first version that offered local resource mapping, session directories, and console mode connections. 

<b>Version 6</b> was included with <i>Windows Vista</i>. Many new quality-of-life features were added, such as multi-monitor support, large desktop support, and the much needed Network Level Authentication. This version would be included also with the <i>Windows XP Service Pack 2</i>, as well as <i>Windows Server 2003 SP1/SP2</i>.

<b>Version 6.1</b> was released alongside Windows Server 2008, which focused on printing redirection, to allow clients to have print capabilities within remote applications without the hassle of needing to install printer drivers on the server.

<b>Version 7</b> came out with Windows 7 and Windows Server 2008 R2. This marked the formal change from <i>"Terminal Services"</i> to <i>"Remote Desktop Services</i>. This update included some major changes, such as the capability to support the <i>Aero glass</i> desktop subsystem, bidirectional audio, and multiple monitor support (at a much more reliable level than before).
However, most of these bells and whistles are only available on <i>Windows 7 Enterprise</i> or <i>Ultimate editions</i>.

<b>Version 8</b>: Released alongside <i>Windows 8</i> and <i>Windows Server 2012</i> a particular focus was placed on the graphics capabilities across the protocol. Functions such as Adaptive Graphics, vGPU support, a "quality-slider" and more were key focus points on this version release. The shadow feature, which allowed a user to previously monitor an RDP session without notice, had been stripped; The aero glass feature was also done away with, as it was no longer being utilized in Windows 8 (and onwards)

<b>Version 8.1</b>: You guessed it, this was released alongside <i>Windows 8.1</i> and <i>Windows Server 2012 R2</i>. Support for shadowing was <b>added back by popular demand</b> and many visual glitches on applications such as Microsoft Office 2013 running <i>RemoteApp</i> were resolved.

<b>Version 10</b>: This is the current version as of 2018, and was released along with Windows 10. H.264/AVC compression has been introduced to improve the graphic compression. AutoSize zoom functionality has also been added, to allow the user the resize the RDP window to any size.

<h1>Competition</h1>
Many different alternatives have popped up over the years. One of the most popular, known as TeamViewer, has been around nearly as long as the protocol itself. There are caveats to using any alternative in general, due to the fact that you'll need to download third party software. One of the inherent pros to using this software is that it is already bundled with Windows.
Another hugely popular protocol known as VNC, has many different applications (TightVNC, TigerVNC, VNCConnect, etc) Virtual Network Computing protocol is outside the scope of this article, but is a notible alternative to RDP/RDC <b>especially if you use Linux</b>.

<h1>Conclusion</h1>
Terminal Services have come a long way. Now known as Remote Desktop Services, it's one of the most used tools by IT professionals. The changes that have been made over the years have been somewhat broad, but the product we use today is very focused and useful for many different tasks.