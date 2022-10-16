Introduction

Chat Room (or Chat Application)
A chat room is a place where people from all over the world may talk with one another about a variety of topics. The themes might be anything from software development to cooking recipes. Chat rooms are excellent places to practise communication skills.
 It can be defined as a virtual channel where people talk with one another over the Internet in plain text. Images and emoticons can now be sent in a chat room thanks to recent advancements in Web technology. 
The phrase can refer to synchronous or asynchronous conferencing in online chatting, instant messaging, and online forums. To log in or join a conversation, some chat rooms demand a username and password combination, allowing for user privacy.

Python For Networking (Why python is good for networking projects)
Python is a great programming language for computer networking. It allows us to create solid applications very fast and easily. It offers two degrees of network service access. You can use the underlying operating system's basic socket support to construct clients and servers for both connection-oriented and connectionless protocols at a low level.
Python also has libraries that give you higher-level access to application-level network protocols like FTP and HTTP.
Therefore, we are going to implement a fully functioning TCP chat using python. We will have one server that hosts the chat and multiple clients that connect to it and communicate with each other. 

What is a Socket?
In the TCP/IP protocol suite, a socket serves as an intermediary between the application layer and the transport layer. We can create a chat application where socket provides the necessary connections between Server and Client Side
Socket programming is a method of allowing two network nodes to communicate with one another. One socket (node) listens on a specific port at an IP address, while another socket establishes a connection with it. While the client connects to the server, the server creates the listener socket.
It can be regarded of as endpoints of a bi-directional communication channel that establishes communication between a server and one or more clients. Any client with a socket on the same port as the server socket can talk with it.

Working of Project (How the project works)
Duplex communication (where both parties can send and receive messages) is a common method of communication and can be one to one (simple chat) or many to many (chat room)
Generally, in real-world, conversation is carried out at once with the use of voice in a perfect situation (distance among speaking parties, identity of parties), whereas in virtual conversation the position of air is performed through community channel (coaxial cable, fibre optics, etc.) and conversation is managed through a server. 
A server is an application which regulates the conversation among sender and receiver.
So, to create a Python Chat Application, one must write a server program and client program/s (sender and receiver). Suppose two parties, let’s say, Adrenex and Ragasur want to chat with each other and then the programmer must develop a chat application where he has to design a server program and a client program (different instance of the same program will be used by both Adrenex and Ragasur or even more users).
 Then once the server program is running, both the clients can be connected to the server and can chat to each other, through the chatroom created. 

Libraries Used:
Socket: The socket module in the Python Standard Library provides a BSD socket interface counterpart. For constructing full-fledged network applications, including client and server programmes, the socket module includes many objects, constants, functions, and related exceptions.
Threading: A thread library provides the programmer an API for creating and managing threads. Here we use this for various functions, mainly for keeping a thread of all the messages, or for listening messages from sender’s and receiver’s side.
Tkinter: Python provides a variety of GUI development possibilities (Graphical User Interface). Tkinter is the most widely used GUI technique out of all the options. It's a standard Python interface to the Python-supplied Tk GUI toolkit. The fastest and simplest approach to construct GUI applications is with Python and tkinter. Using tkinter to create a GUI is a simple operation.

Chatroom SERVER-Side Socket Programming
The server accepts connections from the clients to establish a network interface. Hence, we assign a unique IP address to each client. The role of the server is to collect any incoming messages and deliver them to the other client/clients.
Server program has all the logic to control and regulate the Chat, so most of the chat logic is implemented with a server program. So, first step of communication is to identify the users. In network communication, users are identified by a socket which is nothing but a combination of IP address and port address. So, for human understanding, Adrenex and Ragasur will be chatting but for a network, it is two sockets process which is sending and receiving bytes. 

Steps involved in the server side
1.	Create socket
2.	Communicate the socket address
3.	Keep waiting for an incoming connection request/s
4.	Connect to client
5.	Receive the message
6.	Decode the destination user and select the socket
7.	Send a message to the intended client
8.	Keep repeating step 5 & 6 as per users wish
9.	End the communication by terminating the connection

Chatroom CLIENT-Side Socket Programming
The user runs the client script; therefore, each user will run the identical client code, but each will have their own socket, giving them their own communication channel. Client scripts are thin because they do very little work, such as connecting to the server and sending and receiving messages. All the main connection work is don’t on the server side.

Steps involved on the client side

1. For each instance/user, create a unique client socket. 

2. Connect to the server using the supplied socket address (IP and port)

3. Messages sent and received

4. Repeat step 3 according to the arrangement.

5. Make the connection secure.

Future Scope

This chat application can be improved in the future, by various additions. The GUI could be better, and more attractive, by using numerous tkinter functions. More features can be applied, like sending a message that can be viewed only once, or sending a message inside a group chat, but only the desired client will receive the message. More roles could be applied on the clients, like admin or moderator, where special powers could be assigned to these roles. 

Already there are various chat applications, easily accessible on the internet, and one thing that can be done, is to add all the best features of all working chat applications in this program.
