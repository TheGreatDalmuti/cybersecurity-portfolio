# Web Application Basics

HTTP messages are packets of data exchanged between a user and the web server
HTTP messages:
● HTTP Requests: Sent by the user to trigger actions on the web application
The request line is the first part of an HTTP request and tells the server what kind of
request it's dealing with. It has three main parts: the HTTP method, the URL path, and
HTTP version.
Example : Method/ path HTTP / version
Get / login HTTP/ 1.1

Method - What action the client wants.
Path - The resource being requested.
HTTP Version - Protocol version (usually HTTP/1.1 or HTTP/2).

Method Purpose Example
GET Retrieve data Load a webpage
POST Send data to the server Submit a login form
PUT Replace/update an existing
resource
Update a user's profile
DELETE Remove a resource Delete a file or account

Headers are key-value pairs that provide additional information about the request.
They tell the server who the client is, what data is being sent, and how to process it.
Example
Host: example.coom
User-Agent: Mozilla/5.0
Content-Type: application/json

Headers to Know
Host
● Specifies the website/domain being requested.
● Required in HTTP/1.1
User-Agent
● Identifies the browser or client making the request.
● Can be changed (spoofed)
Content-Type
Tells the server what format the request body is in.

HTTP Request Body
In HTTP requests such as POST and PUT, where data is sent to the web server as opposed to
requested from the web server, the data is located inside the HTTP Request Body. The
formatting of the data can take many forms, but some common ones are URL Encoded, Form
Data, JSON, or XML

● HTTP Responses: Sent by the server in response to the user's request.
When you interact with a web application, the server sends back an HTTP response to
let you know whether your request was successful or something went wrong.
The responses include a status code and a short explanation that gives insight into how
the server handled your request.

Status Line
The first line in every HTTP response is called the Status Line. It gives you three key
pieces of info.
1. HTTP Version: This tells you which version of HTTP is being used.
2. Status Code: A three-digit number showing the outcome of your request
3. Reason Phrase: A short message explaining the status code in human-readable
terms.

The Status Code is the number that tells you if the request succeeded or failed, while the
Reason Phrase explains what happened. These codes fall into five main categories:

Informational Responses (100-199)
These codes mean the server has received part of the request and is waiting for the rest. It's a
"keep going" signal.

Successful Responses (200-299)
These codes mean everything worked as expected. The server processed the request and sent
back the requested data.

Redirection Messages (300-399)
These codes tell you that the resource you requested has moved to a different location, usually
providing the new URL.

Client Error Responses (400-499)
These codes indicate a problem with the request. Maybe the URL is wrong, or you're missing
some required info, like authentication.

Server Error Responses (500-599)
These codes mean the server encountered an error while trying to fulfil the request. These are
usually server-side issues and not the client's fault.

Security Headers
HTTP Security Headers help improve the overall security of the web application by providing
mitigations against attacks.

Insecure Direct Object Reference.
IDOR vulnerabilities are consistently ranked among the most common web application flaws.
They occur because developers assume users will access only their own resource, an
assumption that breaks the moment someone changes a URL parameter.

Telemetry is the black box of an endpoint with everything necessary for detection and
investigation.

CVE
Common vulnerabilities and exposures
An answer to a CVE is always a patch

SSH (Secure Shell) is a protocol that lets you securely connect to another computer over a
network and use its command line as if you were sitting in front of it.

# General Skills in CTF's I

● Web Application Basics
● HTTP in more depth
● SQL Fundamentals
● OWASP Top 10
●

Webexploitationrooms
