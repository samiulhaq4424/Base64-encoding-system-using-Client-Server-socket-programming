
# Base64 encoding system using Client Server socket programming
## To Run:

Command for compiling
---------------------
gcc server.c -o server

gcc client.c -o client


Command for running Server and Client 
-------------------------------------
Server: <executable code><Server Port number>

Client: <executable code><Server IP Address><Server Port number>


Example:

Server: ./server 3200

Client: ./client localhost 3200


## Working

Initially, server will be waiting for a TCP connection from the client. Then, client will connect to the server using
server’s TCP port already known to the client. After successful connection, the client accepts the text input from
the user and encodes the input using Base64 encoding system. Once encoded message is computed the client
sends the Message (Type 1 message) to the server via TCP port. After receiving the Message, server should
print the received and original message by decoding the received message, and sends an ACK (Type 2 message)
to the client. The client and server should remain in a loop to communicate any number of messages. Once the
client wants to close the communication, it should send a Message (Type 3 Message) to the server and the TCP
connection on both the server and client should be closed gracefully by releasing the socket resource.

Note: Server is able to support multiple clients.


