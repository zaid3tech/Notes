# gRPC [Golang] Master Class
Notes for gRPC [Golang] Master Class udemy course.
## Course Content

### 1- gRPC Introduction

-   RPC, remote procedure call.
    
-   ​​gRPC is a modern open-source high-performance Remote Procedure Call (RPC) framework that can run in any environment. It can efficiently connect services in and across data centers with pluggable support for load balancing, tracing, health checking, and authentication. It is also applicable in the last mile of distributed computing to connect devices, mobile applications, and browsers to backend services.
    
-   Focus on data and leave the rest(latency, payload, auth.. etc ) to the framework.
    
-   Course will focus on a theory first and then hands-on.

## gRPC internals, theory

### 1- Protocol Buffers

-   gRPC uses protocol buffers to communicate due to the smaller payload size.
-   protocol buffers are less CPU intensive than JSON, as the prior one serializes into binary format
### 2- HTTP/2

-   HTTP/1 is chattier than HTTP/2, due to a single request returning a single response.
    
-   HTTP/2 is more secure due to SSL requirements.
    
-   Headers in HTTP/2 are compressed, while in HTTP/1 headers are plain text.
    

### 3- Four Types of gRPC APIs

-   Unary, the client will send one request and the server will respond with a single response.
    
-   Server Streaming, the client will send one request and the server can respond with one or multiple responses.
    
-   Client Streaming, Client can send multiple requests and the server will respond with a single response.
    
-   Bi-Directional Streaming, the client can send one or multiple requests and can receive as many responses per request.
    

### 4- Scalability in gRPC

-   On the server side everything is async i.e main is not blocked, while there is freedom on the client side
    

### 5- Security in gRPC (SSL)

-   Binary data is not easily readable though possible.
    
-   SSL.
    
-   Auth Interceptors.
    

### 6- gRPC vs REST

-   gRPC uses Protocol buffers, which is a strict data format, while Rest uses JSON, which is not a strict data format.
    
-   gRPC uses HTTP/2 which makes it much more secure, while most of the Rest APIs use HTTP/1
    
-   gRPC supports streaming of data, while Rest only supports request/response
    
-   gRPC is Bi-Directional, while Rest is a Client/Service
    
-   gRPC offers free design, whereas in Rest we have GET, POST, UPDATE and DELETE