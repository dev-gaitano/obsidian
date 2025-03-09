22:00 Mon 13th January 2025

Status: teen

Tags: #html #css #javascript #cs50 #webdevelopment #youtube

------------------------------------
https://youtu.be/ciz2UaifaNM?si=6kMLblLC8KxY9_AQ
David J. Malan - Gordon McKay Professor of the Practice of Computer Science - Harvard University

**THE INTERNET**
Was Initially a project called ARPANET by the the US Department of defense to internetwork computers to enable them to exchange data in between the computers.

This data exchange is done through packets.

The internet uses routers during this exchange of data to move packets from point A to B.

Routers move data packets through the fastest path rather than the shortest path or a straight line.

**TCP/IP**
Routers implement this pair of protocols.

**1. IP - Internet Protocol**
Associated with IP addresses.

Every internet device has an IP address with the format #.#.#.# to uniquely identify them.

Each of these numbers in the IP address represent a number from 0 to 255.

```
 0                   1                   2                   3
 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|Version|  IHL  |Type of Service|          Total Length         |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|         Identification        |Flags|      Fragment Offset    |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|  Time to Live |    Protocol   |         Header Checksum       |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                       Source Address                          |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                    Destination Address                        |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                    Options                    |    Padding    |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+

Example Internet Datagram Header
```

The IP standardizes what you put on the outside of an envelope (data packet).

The IP mandates / enforces that computers at least provide a source and destination address, so that the packet can go from its source to its destination.

IP alone does not guarantee packet delivery, due to multiple reasons, e.g. Packet overload, memory overload.

**2. TCP - Transmission Control Protocol**
TCP guarantees delivery by adding sequence numbers to the packets.

TCP also adds port numbers to allow router to know what type of data is inside the packets. This helps the router know what program should open the packet.

Two of the most common port numbers today are:
	80 - HTTP
	443 - HTTPS

```
 0                   1                   2                   3
 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|          Source Port          |       Destination Port        |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                        Sequence Number                        |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                    Acknowledgment Number                      |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|  Data |           |U|A|P|R|S|F|                               |
| Offset| Reserved  |R|C|S|S|Y|I|            Window             |
|       |           |G|K|H|T|N|N|                               |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|           Checksum            |         Urgent Pointer        |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                    Options                    |    Padding    |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                             data                              |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+

TCP Header Format
```

**DNS**
When we visit websites we don't type any of the numbers from TCP/IP, we instead type the domain name, e.g. harvard.edu.

The machine still has to know the TCP/IP numbers, but how will it know what IP address to associate with what domain name?

A Domain Name System (DNS) Sever's job is to tell the computer, "This is the IP address of this specific domain name."

A DNS server acts as a dictionary for matching IP addresses and domain names.

| IP Address | Domain Name |
| ---------- | ----------- |
| 1.2.3.4    | example.com |
DNS Servers operate using a hierarchical system. 

When you search for a domain name, your device asks the nearest DNS server for the IP Address, if it doesn't have that IP information it will ask the DNS server above that one then the next one and the next one, until at some point one DNS Server will have that domain name's IP Address.

**DHCP**
A DHCP server tells the network what your computer's DNS server and router should be.

They also tell your device what your IP Address should be.

**HTTP**
HTTP governs how web servers and web browsers communicate with each other.

Standardizes what goes into the envelope (data packet).

HTTPS is the secure version of HTTP, the data in HTTPS is encrypted.

URL - "https://www.example.com/"

"/" - Give the root/default folder
"/path" - Opens a path on the site
"/file.html" - Opens a file on the site
"/folder/" - Opens a folder on the site

"www.example.com" - This is the fully qualified domain name.
"example.com" - This is the domain name.
"www." - This is the host name.
".com" - This is the top level domain.
"https" - This is the protocol.

There are two request information from a server:
	1. GET
	2. POST

POST is you are sending/submitting information to the server.
GET is used when you are getting information from the server.

1. GET

This is an example of what we put inside an envelope (data packet).
```
# This is a GET request

GET / HTTP/2
Host: www.harvad.edu
...
```

"GET" - This is the verb, so we are getting information from the server.
"/" - The root/default folder.

"HTTP/2" - This is the version of HTTP that we are using in this case we are using HTTP version 2

"Host: www.harvad.edu" - This is the HTTP header. It tells the server what fully qualified domain name we are looking for. 
	This is because on a server we might have multiple domains being hosted.

"..." - There are other HTTP headers.

```
# This is what the server sends back after a GET request

HTTP/2 200
Content-Type: text/html
...
```

"200" - A status Code

"Content-Type: text/html" - What type of content is in this envelope, in this case it is "text/html".

To see what an envelope looks like you can run
```
curl -I https://www.harvard.edu/
```
on Unix based systems.

This is what one of these envelopes might look like, after running the command above.
```
HTTP/2 200
server: nginx
date: Thu, 16 Jan 2025 07:34:05 GMT
content-type: text/html; charset=UTF-8
vary: Accept-Encoding
host-header: a9130478a60e5f9135f765b23f26593b
link: <https://www.harvard.edu/>; rel=shortlink
x-rq: jnb1 111 253 443
accept-ranges: bytes
x-cache: MISS
cache-control: max-age=300, must-revalidate
```

List of status codes and their meanings
```
200 OK
301 Moved Permanently
302 Found
305 Not Modified
307 Temporary Redirect
401 Unauthorized
403 Forbidden
404 Not Found
418 I'm a Teapot
500 Internal Server Error
503 Service Unavailable
...
```

**HTML**

This is not a programming language but a markup language.
HTML being a markup language, means you can not write logic or call functions.

There are two concepts
	1. Tags
	2. Attributes

```
<!DOCTYPE html>

<html lang="en">
	<head>
		<title>
			Hello, title
		</title>
	</head>
	<body>
		hello, body
	</body>
</html>

# This is an example HTML code
```

Everything contained in the angled brackets "<>" is referred to as a tag.

"`<!DOCTYPE html>`" - This tag tells the browser the HTML version that we are using. This is the only tag that contains an exclamation sign in it. 

"`<html lang="en">`" - This tag tells the browser where our HTML code begins.

Anything after the name of the tag is considered an attribute. For example in our "html" tag we have the attribute "`lang="en"`".
Attributes are structured in dictionary format, with "lang" being the key and "en" being the value.
Attributes are only typed in the opening tag.

"`</html>`" - This tell the browser where our HTML code ends. Any tag with a forward slash"/" after the first angled bracket is called closing/end tag.

Tags are structured in a family tree type manner, with children tags being inside parent tags.
Any tag inside placed inside another tag becomes its child.

The "html" tag always has two children:
	`<head></head>`
	`<body></body>`

The name of the tag tells the browser what the content inside the tag is, "head" - here comes the head of my website.

==Why isn't my video playing?==

**CSS**
In CSS attributes are called properties.

We use selectors in order to select specific HTML elements and tags and style them.
	type selector - the name of the tag "`p {}`".
	class selector - a dot plus the name of the class "`.centered`".
	ID selector - a "#" symbol plus the name of the ID "`#paragraph1`".
	attribute selector - ==How to select attributes?==
	...

To link our CSS and HTML code we can:
1. Add our CSS properties as attributes to individual elements or tags. 
	`<p style="text-align: center;> </P>"`

2. Add a style tag `<style></style>` to our HTML code inside our head tag and add our CSS properties inside the style tags.
	
	```
	<head>
		<style>
			body {
				text-align: center;
			}
		</style>
	</head>
	```

	This will align all the text in our body to the center of the page.

	We can also create reusable sets of properties in CSS by using the "class" attribute in HTML.

	```
	index.html
	
	<head>
		<style>
			.centered {
				text-align: center;
			}
		</style>
	</head>
	
	<body class="centered">
		<p>Text</p>
	</body>
	```

	This will align the text of every element with the "class" attribute "centered" to the center of the page.

3. We can create an separate CSS file, write all our properties,

	```
	style.css
	
	.centered {
		text-align: center;
	}
	```

	then link the external CSS file using the `<link>` tag in our head tag.
	`<link rel="stylesheet" href="/style.css"`

	```
	index.html
	
	<head>
		<link rel="stylesheet" href="/style.css">
	</head>
	```

	In this example, we are assuming our CSS file is called "style.css".

The third method is preferred when working with a team so as to avoid bumping heads with other developers, because it allows developers to work on separate files.

**FRAMEWORKS**
Frameworks make the development process easier.

Bootstrap is a CSS framework.
### See also:
[[Float CSS Present]]
[[The CSS box Model]]
