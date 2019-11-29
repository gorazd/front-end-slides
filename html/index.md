class: center, middle

##INTERNET

---

##The internet
The Internet is the backbone of the Web, the technical infrastructure that makes the Web possible. 

At its most basic, the Internet is a large network of computers which communicate all together.

---

##History
The history of the Internet is somewhat obscure. It began in the 1960s as a US-army-funded research project, then evolved into a public infrastructure in the 1980s with the support of many public universities and private companies. The various technologies that support the Internet have evolved over time, but the way it works hasn't changed that much: Internet is a way to connect computers all together and ensure that, whatever happens, they find a way to stay connected.

---

##Network
A network is a group of two or more computer systems linked together. There are many types of computer networks. 

The one we are using in the school is called LAN, local-area network. 

WAN, wide-area network is a network where the computers are farther apart and are connected by telephone lines or radio waves.
]


---

layout: false
.left-column[
]
.right-column[
##Network


.responsive[![Network](internet-schema-1.png)]

---

##Router
A router is a device that forwards data packets along networks. A router is connected to at least two networks, commonly two LANs or WANs or a LAN and its ISP's network. Routers are located at gateways, the places where two or more networks connect.

Routers use headers and forwarding tables to determine the best path for forwarding the packets, and they use protocols such as **ICMP** to communicate with each other and configure the best route between any two hosts.

---

layout: false
.left-column[
]
.right-column[
##Router
Router has only one job: it makes sure that a message sent from a given computer arrives at the right destination computer.

.responsive[![Network](internet-schema-3.png)]

---

layout: false
.left-column[
]
.right-column[
##Router
By connecting computers to routers, then routers to routers, we are able to scale infinitely.

.responsive[![Network](internet-schema-5.png)]

---

##ICMP
The Internet Control Message Protocol (ICMP) is one of the main protocols of the Internet Protocol Suite. It is used by network devices, like routers, to send error messages indicating, for example, that a requested service is not available or that a host or router could not be reached.

The PING command, for example, uses ICMP to test an Internet connection.

* Ping is a computer network administration software utility used to test the reachability of a host on an Internet Protocol (IP) network and to measure the round-trip time for messages sent from the originating host to a destination computer and back.

---

##IP Address
An IP address is an identifier for a computer or device on a TCP/IP network. Networks using the TCP/IP protocol route messages based on the IP address of the destination.

If you want to send a message to a computer, you have to specify which one. Thus any computer linked to a network has a unique address to identify it, called an "IP address" (where IP stands for Internet Protocol). It's an address made of a series of four numbers separated by dots, for example: 192.168.2.10.

Within an isolated network, you can assign IP addresses at random as long as each one is unique. However, connecting a private network to the Internet requires using registered IP addresses (called Internet addresses) to avoid duplicates.

---

##IPv6
IPv6 (Internet Protocol Version 6) is also called IPng (Internet Protocol next generation) and it is the newest version of the Internet Protocol (IP) reviewed in the IETF standards committees to replace the current version of IPv4 (Internet Protocol Version 4).

- In IPv6 the IP address size is increased from 32 bits to 128 bits.
- IPv6 supports a greater number of addressable nodes
- IPv6 provides more levels of addressing hierarchy
- IPv6 offers simpler auto-configuration of addresses
- IPv6 also supports simplified header format 

---

##What this means

- IPv4 : 16.8 million unique addresses

- IPv6 : 340 trillion, trillion, trillion unique addresses

---

##Domain names
IP adresses are perfectly fine for computers, but we human beings have a hard time remembering that sort of address. 

To make things easier, we can alias an IP address with a human readable name called a domain name. 

For example, google.com is the domain name used on top of the IP address 216.58.209.142. So using the domain name is the easiest way for us to reach a computer over the Internet.

---

##Packets
Basically, when data is sent across the Web, it is sent as thousands of small chunks, so that many different web users can download the same website at the same time. 

If web sites were sent as single big chunks, only one user could download one at a time, which obviously would make the Web very inefficient and not much fun to use.

---

##TCP/IP
Transmission Control Protocol/Internet Protocol, TCP/IP is the suite of communications protocols used to connect hosts on the Internet. TCP/IP uses several protocols, the two main ones being TCP and IP. 

TCP/IP is built into the UNIX operating system and is used by the Internet, making it the de facto standard for transmitting data over networks. Even network operating systems that have their own protocols, such as Netware, also supportTCP/IP.

---


##Conclusion
The Internet is a technical infrastructure which allows billions of computers to be connected all together. Among those computers, some computers (called Web servers) can send messages intelligible to web browsers.

The Internet is an infrastructure, whereas the Web is a service built on top of the infrastructure. It is worth noting there are several other services built on top of the Internet, such as email and IRC.

---
class: center, middle

#THE WEB

---

##The Web
Computers connected to the Web are called clients and servers.

---

##Server 
Servers are computers that store webpages, sites, or apps. When a client device wants to access a webpage, a copy of the webpage is downloaded from the server onto the client machine to be displayed in the user's web browser.

---

##Client
Clients are the typical Web user's Internet-connected devices (for example, your computer connected to your Wi-Fi, or your phone connected to your mobile network) and Web-accessing software available on those devices (usually a web browser like Firefox or Chrome).

---

##Web browser
Short for Web browser, a browser is a software application used to locate, retrieve and display content on the World Wide Web, including Web pages, images, video and other files. 

As a client/server model, the browser is the client run on a computer that contacts the Web server and requests information. 

The Web server sends the information back to the Web browser which displays the results on the computer or other Internet-enabled device that supports a browser.

---


##HTTP
Short for HyperText Transfer Protocol, HTTP is the underlying protocol used by the World Wide Web. HTTP defines how messages are formatted and transmitted, and what actions Web servers and browsers should take in response to various commands. 

For example, when you enter a URL in your browser, this actually sends an HTTP command to the Web server directing it to fetch and transmit the requested Web page.

---


##HTTP Status codes
Errors on the Internet can be quite frustrating — especially if you do not know the difference between a 404 error and a 502 error. These error messages, also called HTTP status codes are response codes given by Web servers and help identify the cause of the problem.

For example, "404 File Not Found" is a common HTTP status code. It means the Web server cannot find the file you requested. The file -- the webpage or other document you try to load in your Web browser --  has either been moved or deleted, or you entered the wrong URL or document name.

"502 Service Temporarily Overloaded" means server congestion; too many connections; high traffic. Keep trying until the page loads.

---
class: center, middle

#THE PROCESS OF NAVIGATING

---

##Internet connection
Allows you to send and receive data on the Web. It's basically like the street between your house and another house.

---

##TCP/IP
Transmission Control Protocol and Internet Protocol are communication protocols that define how data should travel across the Web.

---

##DNS
Domain Name System Servers are like an address book for websites. When you type a web address in your browser, the browser looks at the DNS before retrieving the website. The browser needs to find out which server the website lives on, so it can send HTTP messages to the right place.

---

##HTTP
Hypertext Transfer Protocol is an application protocol that defines a language for clients and servers to speak to each other.

---

##Component files
A website is made up of many different files. These files come in two main types:

- **Code files**:
HTML, CSS, and JavaScript files (and others).

- **Assets**:
This is a collective name for all the other stuff that makes up a website, such as images, music, video, Word documents, and PDFs.

---

##When you type google.com into your browser

- The browser goes to the DNS server and finds the real address of the server that the website lives on.
- The browser sends an HTTP request message to the server asking it to send a copy of the website to the client (you go to the shop and order your goods). This message, and all other data sent between the client and the server, is sent across your internet connection using TCP/IP.
- Provided the server approves the client's request, the server sends the client a "200 OK" message, which means "Of course you can look at that website! Here it is", and then starts sending the website's files to the browser as a series of small chunks called data packets.
- The browser assembles the small chunks into a complete website and displays it to you.

---
class: center, middle

#Working on your Project

---

##The folder
When you are working on a website locally on your own computer, you should keep all the related files in a single folder that mirrors the published website's file structure on the server. 

This folder can live anywhere you like, but you should put it somewhere where you can easily find it, maybe on your Desktop, in your Home folder, or at the root of your hard drive.

- Choose a place to store your website projects. Here, create a new folder called web-projects (or similar). This is where all your website projects will live.

- Inside this first folder, create another folder to store your first website in. Call it with the name of your project.

---

##The naming
Many computers, particularly web servers, are case-sensitive. So for example, if you put an image on your website at **test-site/MyImage.jpg**, and then in a different file you try to invoke the image as **test-site/myimage.jpg**, it may not work.

Browsers, web servers, and programming languages do not handle spaces consistently. For example, if you use spaces in your filename, some systems may treat the filename as two filenames. 

Some servers will replace the spaces in your filenames with "%20" (the character code for spaces in URIs), breaking all your links. It's better to separate words with dashes or underscores: my-file.html or my_file.html.

---

#The structure 

The most common things you'll have on any website project you create are an index HTML file and folders to contain images, style and script files.

---

#The structure 

- index.html: This file will generally contain your homepage content, that is, the text and images that people see when they first go to your site.

---

#The structure 
- images folder: This folder will contain all the images that you use on your site. You should create the folder called images, inside your website folder.

---

#The structure 
- styles folder: This folder will contain the CSS code used to style your content (for example, setting text and background colors).

---

#The structure 
- scripts folder: This folder will contain all the JavaScript code used to add interactive functionality to your site (e.g. buttons that load data when clicked).

---
class: center, middle

#Back to HTML

---

##HTML elements
- doctype
- html
- head
- body
- meta
- title
- style
- script
- link

---

##HTML elements

- article
- section
- heading (h1,h2,...)
- paragraph (p)
- address
- hgroup
- nav
- a
- div
- span
- dl, dt, dd
- ul, ol, li
- pre
- br
- img
- audio
- video

---


##New Semantic Elements in HTML5
- article
- aside
- details
- figcaption
- figure
- footer
- header
- main
- mark
- nav
- section
- summary
- time

We already looked at article and section elements.
How do we nest them?

---

##Nesting
In the HTML5 standard, the ```<article>``` element defines a complete, self-contained block of related elements.

The ```<section>``` element is defined as a block of related elements.

Can we use the definitions to decide how to nest elements? No, we cannot!

On the Internet, you will find HTML pages with ```<section>``` elements containing ```<article>``` elements, and ```<article>``` elements containing ```<sections>``` elements.

You will also find pages with ```<section>``` elements containing ```<section>``` elements, and ```<article>``` elements containing ```<article>``` elements.

---

##HTML5 ```<header>``` Element
The ```<header>``` element specifies a header for a document or section.

The ```<header>``` element should be used as a container for introductory content.

You can have several ```<header>``` elements in one document.
```html
<article>
  <header>
    <h1>What Does WWF Do?</h1>
    <p>WWF's mission:</p>
  </header>
  <p>WWF's mission ...</p>
</article>
```
---

##HTML5 ```<footer>``` Element

The ```<footer>``` element specifies a footer for a document or section.

A ```<footer>``` element should contain information about its containing element.

A footer typically contains the author of the document, copyright information, links to terms of use, contact information, etc.

You can have several ```<footer>``` elements in one document.

```html
<footer>
  <p>Posted by: Hege Refsnes</p>
  <p>Contact information:<br>
    <a href="mailto:someone@example.com">
    someone@example.com</a>.</p>
</footer>
```

---

##HTML5 ```<aside>``` Element

The ```<aside>``` element defines some content aside from the content it is placed in (like a sidebar).

The aside content should be related to the surrounding content.
```html
<p>My family and I visited 
The Epcot center this summer.</p>

<aside>
  <h4>Epcot Center</h4>
  <p>The Epcot Center
    is a theme park in 
    Disney World, Florida.</p>
</aside>
```
---

##HTML5 ```<figure>``` and ```<figcaption>``` Elements

The purpose of a caption is to add a visual explanation to an image.

With HTML5, images and captions can be grouped together in ```<figure>``` elements:
```html
<figure>
  <img src="pic_mountain.jpg" alt="The Pulpit Rock" width="304" height="228">
  <figcaption>Fig1. - The Pulpit Rock, Norway.</figcaption>
</figure>
```
---

##HTML5 ```<main>``` Element

The ```<main>``` tag specifies the main content of a document.

The content inside the ```<main>``` element should be unique to the document. It should not contain any content that is repeated across documents such as sidebars, navigation links, copyright information, site logos, and search forms.

There must not be more than one ```<main>``` element in a document. The ```<main>``` element must NOT be a descendant of an ```<article>```, ```<aside>```, ```<footer>```, ```<header>```, or ```<nav>``` element.
```html
<main>
  <h1>Web Browsers</h1>
  <p>Google Chrome, Firefox, and Internet Explorer are the most used browsers today.</p>

  <article>
    <h1>Google Chrome</h1>
    <p>Google Chrome is a free, open-source web browser developed by Google,
      released in 2008.</p>
  </article>
</main>
```

---

##HTML ```<mark>``` Tag
The ```<mark>``` tag defines marked text.

Use the ```<mark>``` tag if you want to highlight parts of your text.
```html
<p>Do not forget to buy <mark>milk</mark> today.</p> 
```

---

##HTML ```<summary>``` Tag
The ```<summary>``` tag defines a visible heading for the ```<details>``` element. The heading can be clicked to view/hide the details.

---

##HTML ```<details>``` Tag
The ```<details>``` tag specifies additional details that the user can view or hide on demand.

The ```<details>``` tag can be used to create an interactive widget that the user can open and close. Any sort of content can be put inside the ```<details>``` tag.

The content of a ```<details>``` element should not be visible unless the open attribute is set.

```html
<details>
  <summary>Copyright 1999-2014.</summary>
  <p> - by Refsnes Data. All Rights Reserved.</p>
  <p>All content and graphics on this web site are the property of the company Refsnes Data.</p>
</details> 
```

---

##HTML ```<time>``` Tag
The ```<time>``` tag defines a human-readable date/time.

This element can also be used to encode dates and times in a machine-readable way so that user agents can offer to add birthday reminders or scheduled events to the user's calendar, and search engines can produce smarter search results.

```html
<p>We open at <time>10:00</time> every morning.</p>

<p>I have a date on <time datetime="2008-02-14 20:00">
Valentines day</time>.</p> 
```