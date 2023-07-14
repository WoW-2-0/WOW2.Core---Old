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
* We can't just send requests from the browser just like we do with REST APIs



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







* What: gRPC (Google Remote Procedure Call) is an open-source framework used for building high-performance, cross-platform remote procedure call (RPC) APIs. It allows services to communicate with each other efficiently and seamlessly, using various programming languages and platforms.
* How: gRPC uses the Protocol Buffers (protobuf) data format to define the service interface and message types. It generates client and server code based on the defined interface, which enables developers to easily interact with remote services. Under the hood, gRPC utilizes HTTP/2 for transport and supports different serialization formats, including binary and JSON.
* Why: gRPC offers several advantages over traditional communication protocols, making it popular in modern distributed systems:
  1. Efficient and Fast: gRPC uses binary serialization and HTTP/2 to achieve high-performance communication with low latency and reduced bandwidth usage.
  2. Language and Platform Agnostic: gRPC supports multiple programming languages, enabling services written in different languages to seamlessly communicate with each other.
  3. Code Generation: gRPC generates client and server code from the service definition, which simplifies the development process and ensures type safety.
  4. Bi-directional Streaming: gRPC supports both unary (single request/response) and streaming (continuous data transfer) communication patterns, allowing for flexible and efficient data exchange.
  5. Service Contracts: With the use of protobuf, gRPC provides a clear and structured way to define service contracts, making it easier to maintain and evolve APIs.
* When: gRPC is particularly useful in scenarios that require high-performance, low-latency communication between services. It is well-suited for microservices architectures, where services need to communicate over networks and handle large amounts of data efficiently. Additionally, gRPC can be used in scenarios where cross-platform communication is required, such as client-server communication between different mobile or web applications.

Overall, gRPC is a powerful framework that enables efficient and flexible communication between services. It provides benefits such as performance, language agnosticism, code generation, and streaming capabilities, making it a popular choice for building modern distributed systems.





