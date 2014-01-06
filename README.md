Programatic Knowledge Interface
===============================

The Programatic Knowledge Interface (or PKI) is an extensible, highly flexible
API/Protocol for the exchange of knowledge between applications and web services
over HTTP and HTTPS. Its primary goal is to provide a standardized interface
which applications can use to exchange data with each other, which isn't
dependant on custom, application-specific APIs. Basically, I want to make the
internet just as accessible and easy to navigate for machines as it currently is
for humans; the Programatic Knowledge Interface is my first attempt at
accomplishing this.

Okay, enough with the buzzwords and vague abstractions; what is this thing and
how does it work?

How it Works
------------
At its core, the Programatic Knowledge Interface is just JSON requests and
responses over HTTP/HTTPS. JSON requests may be queries asking for specific
information (HTTP GET), or authenticated requests requesting that information be
added or modified (HTTP POST, PUT, or PATCH).

All information in the Programatic Knowledge Interface is represented as
"entities" which may refer to each other to create a sort of graph or web of
knowledge. Entities have keys which are unique across all PKI nodes.



All objects are nodes on the graph and contain meta information on what interfaces they support and links to "duplicate" nodes on other servers. The result: a giant graph of all the world's knowledge under one standard API.

Features:
Built-in protocol for RESTFUL queries
Built-in protocol for authentication and fault-tolerant rejection (and timeout) of queries and update requests
Built-in protocol for requesting notifications of changes to a remote node
Nodes can declare what standard APIs they support (node links to another node on authoritative remote which contains API specs)
Nodes can declare extended, custom APIs (either APIs of their own or APIs from an authoritative source) which may not be supported by all applications (for extra stuff like Video Streaming, live collaborative editing, etc) These APIs must be a strict superset of the standard APIs.

This is the internet for machines.

Related: Adapters for existing APIs that don't support this protocol yet
