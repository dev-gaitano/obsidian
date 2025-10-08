09:16 Tue 31st December 2024

Tags: #django #youtube #frameworks #webdevelopment

---
https://youtu.be/rHux0gMZ3Eg?si=_z2s_QBh-U1pBEU_
Mosh Hamedani - Youtuber

What you should know to take this course:
[[Python programming language]]
	Basics
	Classes
	Inheritance

Relational Databases
	Tables
	Columns
	Keys
	Relationships

Tips for taking this course:
1. Watch this course from beginning to end
2. Take notes
3. After each lesson go through your notes and repeat the exercises
4. Complete all the exercises

**What is Django?**
Django is a free [[framework]] for building web apps with python.
Its the most popular python web app framework.

It is a 'Batteries included' framework. Which means it comes with a lot of features out of the box, e.g. 
	The admin site
	ORM
	Auth
	Caching

Don't pick a framework just based on performance, consider the following as well and pick what framework suites you best.
	Maturity
	Stability
	Difficulty
	Community

**How the web works**
In this course we are going to be building a Web store.

The frontend is the part that the user sees and interacts with
Runs on the clients machine

The backend is the part that manages the user data
Runs on a server

We use URLs (Uniform Resource Locators) to locate resources on the web.
Examples of resources are;
	Page
	Image
	PDF
	Video, etc.

What happens when the user types in the URL and presses enter:

![[Pasted image 20250102081741.png]]

![[Pasted image 20250102081719.png]]

*"This data exchange is defined by a protocol called HTTP (Hypertext Transfer Protocol)"*

*==A protocol is a set of rules, conventions, and standards that govern how data is transmitted and communicated between devices, systems, or applications. - ChatGPT ==*

The client sends a HTTP request.
The server serves a HTTP response.

How are we going to serve our clients?
1. Generate the requested page on the server and serve it to the client, as a HTML (Hypertext Markup Language) document.
	![[Pasted image 20250102085811.png]]

2. Serve only the data and have the client generate the website on their browser.
	![[Pasted image 20250102085910.png]]
	
	Serving just the data is the best practice, as it allows us to free up the server, allowing us to serve more clients.
	
	This method allows the server to become a gateway to the data. 
	
	We can then provide endpoints with which the client can communicate with to access or save data, e.g. /product, /orders.
	![[Pasted image 20250102091238.png]]
	
	All these endpoints together provide an **interface** that the client uses to talk to the server.
	
	This interface is called an API (Application Programming Interface)

In this course we are going to be using Django to create an API for a web app.

**Setting up the Development Environment**

### See also:
[[Django web application framework for python]]
[[IBM Technology - What is Django]]
[[Dennis Ivy - Python Django Explained in 8 Minutes]]
