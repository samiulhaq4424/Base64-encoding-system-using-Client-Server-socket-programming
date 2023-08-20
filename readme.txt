Application #4:Base64 encoding system using Client-Server socket programming 



Initially, server will be waiting for a TCP connection from the client. Then, client will connect to the server using server’s TCP port already known to the client. After successful connection, the client accepts the text input from the user and encodes the input using Base64 encoding system. Once encoded message is computed the client sends the Message (Type 1 message) to the server via TCP port. After receiving the Message, server should print the received and original message by decoding the received message, and sends  an  ACK  (Type  2  message)  to  the  client.  The  client  and  server  should  remain  in  a  loop  to communicate any number of messages. Once the client wants to close the communication, it should send a Message (Type 3 Message) to the server and the TCP connection on both the server and client should be closed gracefully by releasing the socket resource. 




Base64 encoding is used for sending a binary message over the net. In this scheme, groups of 24bit are broken into four 6 bit groups and each group is encoded with an ASCII character. For binary values 0 to 25 ASCII character ‘A’ to ‘Z’ are used followed by lower case letters and the digits for binary values 26 to 51 & 52 to 61 respectively. Character ‘+’ and ‘/’ are used for binary value 62 & 63 respectively. In case the last group contains only 8 & 16 bits, then “==” & “=” sequence are appended to the end. 





