<h1>WebServers, Node.js and Nginx</h1>

<h3>WebServers</h3>

Web browsers are an example of a webserver. They are software programs that 
integrates HTTP requests from clients. When the URL is entered in the browser, it 
automatically sends a DNS request to capture the IP address of the domain. Thus responding
with a HTTP requested page.

<h3>Nginx</h3>

Nginx is a popular web server that is highly regarded for its fast and efficient performance. 
One of the key reasons for its speed is the way it uses worker processes and connections 
to handle requests and responses. Each worker connection in Nginx is designed to handle up 
to 1024 requests, making it one of the fastest web servers available. Companies such like Netflix, 
Google rely on Nginx to deliver to their users.

<h3>Node.js</h3>

Node.js is an open-source, cross-platform runtime environment for executing JavaScript code on the server-side. 
Unlike traditional web servers, which rely on multi-threading to handle multiple requests, NodeJS uses an event-driven, 
single-threaded model that enables it to process multiple requests simultaneously with greater efficiency.

Compared to traditional web servers, which handle each request sequentially, NodeJS can process multiple 
requests simultaneously, resulting in faster and more efficient web applications. It is particularly useful 
for streaming web applications, and chatbots.

<h3>User Cases of Node.js</h3>

The following are a few examples of user cases:

- Developing Streaming Web Applications
- Developing Real-Time Chat-bots
- Facilitating Wireless Connectivity
- Enabling Server-side proxy
- Automation solutions
- Developing Single-Page Applications

<h3>Dependencies of Node.js</h3>

Dependencies include:

- Development , production , bundled.

However, they can be separated into two categories which are:

Core:
- HTTP / HTTPS
- Path
- Stream
- Crypto

External:
- Express
- Async
- Socket.io
- NodeMailer
- Mongoose

<h3>NPM</h3>

NPM is a widely-used software package manager and installer that simplifies the process of managing 
and sharing code packages for JavaScript developers. The NPM registry contains an expansive collection of more than 
800,000 code packages, making it a popular choice for open-source developers looking to distribute their software. 
Additionally, NPM serves as a go-to solution for organizations looking to manage private development by securing 
internal packages and establishing their private registries.

<h3>Reverse Proxy</h3>

A reverse proxy is a server that sits between a client and a web server, forwarding client requests to the appropriate 
server and returning the server's response to the client. Reverse proxies can be used for network protection, privacy, caching,
load balancing. 






