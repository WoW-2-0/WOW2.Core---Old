# Intro





gRPC - language agnostic, high-performance Remote Procedure Call (RPC) framework



* Modern, high-performance, lightweight PRC framework
* Contract-first API development
* Tools available for strongly typed clients and servers
* Supports client, server and bi-directional streaming calls
* Reduced network usage with Protobuf binary serialization
* Uses&#x20;
  * HTTP/2
  * `Protobuf`
* We can think gRPC service as a controller where methods of that service are actions



Ideal for&#x20;

* Lightweight microservices where efficiency is critical
* Polyglot systems where multiple languages are required for development
* Point-to-point real-time service that need to handle streaming requests or responses











Proto buffer file

* Must bet set for either&#x20;
  * `Client` -&#x20;
  * `Server` -
  * `Client and Server` -&#x20;





* When Proto file is built, if it is for
  * Server - service base file is generated
  * Client - service client is generated





Example&#x20;

* Image if Server had to execute multiple processes and what if we might want to receive those process results when they finish on the client side ?
* On gRPC communication model, we can send each result as response using streams









