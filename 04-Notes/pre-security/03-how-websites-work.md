# How websites Work

There are two major components that make up a website:
1. Front end (Client-Side) - the way your browser renders a website.
2. Back End (Server-Side) - a server that processes your request and returns a response

Websites are primarily created using:
HTML, to build websites and define their structure
CSS, to make websites look pretty by adding styling options
JavaScript, implement complex features on pages using interactivity

Hyper Text Markup Language (HTML) is the language websites are written in. Elements are the
building blocks of HTML pages and tell the browser how to display content.
JavaScript allows pages to become interactive. HTML is used to create the website structure
and content, while JavaScript is used to control the functionality of web pages - without Java
Script, a page would not have interactive elements and would always be static.
JavaScript is added within the page source code and can be either loaded within <script> tags
or can be included remotely with the src attribute : <script src= "/location/of/javascript_file.js">
</script>

Sensitive Data Exposure
Sensitive Data Exposure occurs when a website doesn't properly protect sensitive clear-text
information to the end-user; usually found in a site's frontend source code. Whenever you're assessing a web application for security issues, one of the first things you
should do is review the page source code to see if you can find any exposed login credentials or
hidden links.
Input sanitisation is very important in keeping a website secure, as information a user inputs into
a website is often used in other frontend and backend functionality.

HTML Injection
HTML injection is a vulnerability that occurs when unfiltered user input is displayed on the page.
If a website fails to sanitise user input, and that input is used on the page, an attacker can inject
HTML code into a vulnerable website.

Load Balancers
Load balancers provide two main features, ensuring high traffic websites can handle the load
and providing a failover if a server becomes unresponsive.
Load balancers perform what is called a health check.

CDN (Content Delivery Networks)
A CDN can be an excellent resource for cutting down traffic to a busy website. Allows you to
host static files from your website, such as JavaScript, CSS, Images, Videos, and host them
across thousands of servers all over the world. '

Databases
Web servers can communicate with databases to store and recall data from them. Databases
can range from just a simple plain text file up to complex clusters of multiple servers providing
speed and resilience.

WAF (Web Application Firewall)
A WAF sits between your web request and the web server; its primary purpose is to protect the
web server from hacking or denial of service attacks. It analyses the web requests for common
attack techniques, whether the request is from a real browser rather than a bot.

# HTTP in detail

HTTP is the set of rules used for communicating with web servers for the transmitting of
webpage data, whether that is HTML,Images, Videos,etc.
HTTPS is the secure version of HTTP. HTTPS data is encrypted so it not only stops people from
seeing the data you are receiving and sending

HTTP
HyperText Transfer Protocol

Uniform Resource Locator
A URL is predominantly an instruction on how to access a resource on the internet.

FEATURES of a URL EXAMPLE!
Scheme : http://
User: user:password
Host / Domain: tryhackme.com:
Port 80
Path view-room
Query String : ?id=1
Fragment #task3

Scheme: This instructs on what protocol to use for accessing the resource such as HTTP,
HTTPS, FTP ( File Transfer Protocol.
User: Some services require authentication to log in, you can put a username and password
into the URL to log in.
Host: The domain name or IP address of the server you wish to access.
Port : The Port that you are going to connect to , usually 80 for HTTP and 443 for HTTPS, but
this can be hosted on any port between 1-65535.
Query String: Extra bits of information that can be sent to the requested path . For example,
/blog?id=1 would tell the blog path that you wish to receive the blog article with the id of 1
Fragment: This is a reference to a location on the actual page requested. This is commonly
used for pages with long content and can have a certain part of the page directly linked to it, so
it is viewable to the user as soon as they access the page.

Making a Request
Request to a web server with just one line "GET / HTTP/1.1"

Example Request:
GET / HTTP/1.1
Host: tryhackme.com
User-Agent: Mozilla/5.0 Firefox/87.0
Referer: https://tryhackme.com/

Line 1: This request is sending the GET method, request the home page with / and
telling the web server we are using HTTP protocol version 1.1.
Line 2: We tell the web server we want the website tryhackme.com
Line 3: We tell the web server we are using the Firefox version 87 Browser
Line 4: We are telling the web server that the web page that referred us to this one is
https://tryhackme.com
Line 5: HTTP requests always end with a blank line to inform the web server that the
request has finished.

Example Response:
HTTP/1.1 200 OK
Server: nginx/1.15.8
Date: Fri, 09 Apr 2021 13:34:03 GMT
Content-Type: text/html
Content-Length: 98

<html> <head> <title>TryHackMe</title> </head> <body>
Welcome To TryHackMe.com </body> </html>

To breakdown each line of the response:
Line 1: HTTP 1.1 is the version of the HTTP protocol the server is using and then
followed by the HTTP Status Code in this case "200 OK" which tells us the request has
completed successfully.
Line 2: This tells us the web server software and version number.
Line 3: The current date, time and timezone of the web server.
Line 4: The Content-Type header tells the client what sort of information is going to be
sent, such as HTML, images, videos, pdf, XML.
Line 5: Content-Length tells the client how long the response is, this way we can
confirm no data is missing.
Line 6: HTTP response contains a blank line to confirm the end of the HTTP response.
Lines 7-14: The information that has been requested, in this instance the homepage.

HTTP methods are a way for the client to show their intended action when making an HTTP
request.

GET Request
This is used for getting information from a web server.
POST Request
This is used for submitting data to the web server and potentially creating new records
PUT Request
This is used for submitting data to a web server to update information
DELETE Request
This is used for deleting information/records from a web server.

HTTP Status Codes.
Status codes inform the client of the outcome of their request and also potentially how to
handle it. These status codes can be broken down into 5 different ranges:

100-199 Information Response : These are sent to tell the client the first part of their request
has been accepted and they should continue sending the rest of their request. These codes are
no longer very common.
200-299 Success : This range of status code is used to tell the client their request was
successful.
300-399 Redirection : These are used to redirect the client's request to another resource. This
can be either to a different webpage or a different website altogether.
400-499 Client Errors : Used to inform the client that there was an error with their request.
500-599 Server Errors This is reserved for errors happening on the server-side and usually
indicate quite a major problem with the server handling the request

Common HTTP Status Codes :
There are a lot of different HTTP status codes and that's not including the fact that applications
can even define their own, we'll go over the most common HTTP responses you are likely to
come across

200-OK The request was completed successfully
201-created A resource has been created (for example a new user or new blog post).
301 - Moved Permanently This redirects the client's browser to a new webpage or tells search
engines that the page has moved somewhere else and to look there instead
302 found Similar to the above permanent redirect, but as the name suggests, this is only a
temporary change and it may change again in the near future.
400 Bad Request : This tells the browser that something was either wrong or missing in their
request. This could sometimes be used if the web server resource that is being requested
expected a certain parameter that the client didn't send
401 Not Authorised : You are not currently allowed to view this resource until you have
authorised with the web application, most commonly with a username and password.
403 - Forbidden : You do not have permission to view this resource whether you are logged in or
not.
405 - Method Not Allowed : This resource does not allow this method request, for example, you
send a GET request to the resource/ create-account when it was expecting a POST request
instead.
404 - Page Not Found The page/ resource you requested does not exist.
500 - Internal Service Error : The server has encountered some kind of error with your request
that it doesn't know how to handle properly
503 - Service Unavailable : This server cannot handle your request as it's either overloaded or
down for maintenance.

Common Request Headers
These are headers that are sent from the client (usually your browser) to the server.
Host : Some web servers host multiple websites so by providing the host headers you can tell it
which one you require , otherwise you'll just receive the default website for the server.
User-Agent: This is your browser software and version number, telling the web server your
browser software helps it format the website properly for your browser and also some elements
of HTML, JavaScript are only available in certain browsers.
Content-Length : When sending data to a web server such as in a form, the content length tells
the web server how much data to expect in the web request. This way the server can ensure it
isn't missing any data.
Accept Encoding : tells the web server what types of compression methods the browser
supports so the data can be made smaller for transmitting over the internet.
Cookie: Data sent to the server to help remember your information.

Common Response Headers
These are the headers that are returned to the client from the server after a request.
Set-Cookie: Information to store which gets sent back to the web server on each request.
Cash-Control: how long to store the content of the response in the browser's cache before it
requests it again.
Content-Type: This tells the client what type of data is being returned,
HTML,CSS,JavaScript,Images, PDF, Video, ets. Using the content-type header the browser
then knows how to process the data.
Content-encoding: what method has been used to compress the data to make it smaller when
sending it over the internet.

Cookies
Cookies are a small piece of data that is stored on your computer.
Cookies are saved when you receive a "Set-Cookie" header from a web server
