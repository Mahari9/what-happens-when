# What happens when you type https://www.google.com into your browser and hit Enter?

![](https://miro.medium.com/v2/resize:fit:640/format:webp/1*K7zPdxS-_2sAHQL36P4x8g.png)

## Introduction
Let’s dive into what happens when we type https://www.google.com in our browser and press Enter. This question delves into the fascinating world of the web stack and how different technologies work together to deliver the content we see online. Buckle up, because we’re about to explore the fascinating journey from our keyboard to Google’s servers and back.

Before we get into the detailed and specific aspects or fundamental components of our topic, let’s see some basics about Client-Server Model. When we type URL like https://www.google.com and hit Enter, our web browsers like Chrome or Firefox becomes the client, and it requests information from a server. The server, on the other hand, is the one serving up that the requests and information. In our case, Google’s servers are the ones we’re after. They store webpages, sites, or apps and respond to our requests.

Now let’s dive into detailed and specific aspects of our topic, What happens when we type https://www.google.com into our browser and hit Enter? step by steps.

## Step 1: DNS Resolution

**1. DNS Request/lookup**

Basically it’s the process of translating names to numbers. The internet doesn’t understand website names. Instead, it relies on numerical addresses called IP addresses to locate specific computers.
When you enter a URL, your computer initiates a DNS (Domain Name System) lookup. Imagine the DNS as a giant phonebook that translates human-friendly domain names (like google.com) into their corresponding IP addresses (like 52.73.243.18) which are machine readable. The DNS server looks up the IP address associated with domain name (google.com). It might consult its own cache or recursively query other DNS servers until it finds the answer. This lookup process is handled by your DNS resolver, which could be your internet service provider (ISP) or a public DNS server. Once the DNS server has the IP address (e.g., 52.73.243.18), it sends it back to your computer.

## Step 2: Establishing a Connection
**1. TCP/IP**

Now the IP address is retrieved, then your computer(browser) sends a request to the web server to start communication using the TCP/IP protocol. TCP/IP acts like a universal language for communication across the internet. It ensures data is broken down into manageable packets, transmitted efficiently, and reassembled correctly at the destination server.
The browser would later establish an SSL (Secure Sockets Layer) or TLS (Transport Layer Security) connection with the server through an SSL/TLS handshake because the URL uses https (Hypertext Transfer Protocol Secure), and Google’s servers would redirect all http (Hypertext Transfer Protocol) requests to https. This enable Google to ensure that the communication between its servers and users are kept secure.

**2. Firewall**

Firewall is like guardian of the gate. before reaching the Google's web server, the data packets might pass through a firewall. This security system meticulously examine both incoming and outgoing data, following a set of pre-defined rules, to determine if a connection is safe or should be blocked. This watchful eye extends to all communication, including data packets exchanged with websites like Google. By filtering traffic in this way, firewalls significantly reduce the risk of malware attacks, making online communication much safer.

## Step 3: Load Balancing

**1. Load Balancer**

Ensure that when you access google.com, your request is efficiently distributed to the right server.

Imagine millions of people trying to squeeze through a single doorway at once. That’s what accessing a super popular website like Google with just one server would be like! Delays and crashes would be inevitable. To handle this, Google distributes its content across numerous powerful servers, each with its own unique address. But that’s not all! Just like rush hour traffic needs direction, these servers rely on a load balancer to ensure smooth information flow by distributing incoming requests efficiently. This way, no matter where you are in the world, you can access Google without encountering a digital traffic jam.

Assume a busy restaurant with a single waiter. Orders would back up, and customers would get frustrated. Websites face a similar challenge with high traffic. To avoid delays, companies like Google use load balancers. These act like traffic directors, cleverly routing incoming requests from users (clients) across a network of multiple servers. Each server, like a well-trained waiter, can handle its share of requests, ensuring smooth operation. Load balancing can be implemented in software using different algorithms, or it can be achieved using specialized hardware like routers or switches placed between clients and servers.

## Step 4: Serving the Webpage

**1. HTTPS/SSL**

After connecting to the server, your browser speaks a secret language and it follows a special set of instructions called HTTPS. HTTPS secures communication between websites and browsers. But how does it do that? Before any information gets sent, your computer and a website (like Google) go through this special handshake to confirm their identities and agree on a secret code. This code scrambles the data being exchanged, making it unreadable to anyone trying to eavesdrop. The conversation follows a specific format, with three main parts: a request line introducing itself, headers with additional details, and an optional message body. The request line specifies what the browser wants (using an HTTP method), where it wants it from (the resource path), and how they should talk (the HTTP version).

**2. Web Server**

As we mentioned above, load balancer acts like a traffic director, sending your request to the best available server, let’s call it server n. This server is a workhorse, built for handling website requests. Server n then retrieves the information you requested, like the Google homepage, from its storage. These servers are particularly good at delivering pre-built content quickly and efficiently.

## Step 5: Dynamic Content

**1. Application Server**

Plain webpages are great, but sometimes you need something more custom, like search results or recommendations. That’s where Google’s application servers come in. These clever servers act like behind-the-scenes assistants for Google website. They take your request, chat with databases to find the information you need, and then assemble a custom response just for you.

**2. Database**

Behind the scenes, Google’s databases hold vast amounts of information. When you search, these databases are queried, and the results are sent back to the application server.

Imagine a giant filing cabinet holding all of Google’s information, like user details, locations, and even what time zone you’re in. This filing cabinet is the database, managed by a system that keeps everything organized and easy to find. When you visit Google, the application server acts like a messenger. It talks to the database system to get specific information, like your location based on your IP address. With this info, the server can build a customized homepage just for you and send it back to your browser.

## Summary
This is a simplified look at how websites work, especially Google. Hopefully, it answers your question of what happens when you type ‘https://www.google.com' and hit enter! Thanks for your curiosity, and feel free to visit again if you have more questions.
