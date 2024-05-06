A screenshot of one terminal running server.rs on the top right corner and 3 terminal around it, each act 
as a client.

![image](https://github.com/Nabilcodes/chat-async/assets/71275597/3527346e-a68f-4eb6-9484-0e7614da7f52)

How to run it :
Server : cargo run --bin server
Client : cargo run --bin client

When I type some text in the client, two things happened :
1. The server records and print the client's address and the text it sent
2. Clients receive the text from client that sent the text (in this implementation, the sender
   also receives the text that it sent from it self)

=== changing port ===

A screenshot of one terminal running server.rs on the top right corner and 3 terminal around it, each act 
as a client.

![image](https://github.com/Nabilcodes/chat-async/assets/71275597/949fc20d-f401-409c-bf7e-3870263201e3)

The file that should be modifed was client.rs and server.rs.
They still use the same websocket protocol.
It was defined in TcpListener and ClientBuilder, both at the main function.
