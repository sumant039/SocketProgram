# SocketProgram
Socket programming is a way of connecting two nodes on a network to communicate with each other. One socket(node) listens on a particular port at an IP, while other socket reaches out to the other to form a connection. Server forms the listener socket while client reaches out to the server.
They are the real backbones behind web browsing. In simpler terms there is a server and a client. 
Socket programming is started by importing the socket library and making a simple socket.
import socket
s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
Here we made a socket instance and passed it two parameters. The first parameter is AF_INET and the second one is SOCK_STREAM. AF_INET refers to the address family ipv4. The SOCK_STREAM means connection oriented TCP protocol. 
Now we can connect to a server using this socket.

Connecting to a server:
Note that if any error occurs during the creation of a socket then a socket.error is thrown and we can only connect to a server by knowing it’s ip. You can find the ip of the server by using this :
$ ping www.google.com
You can also find the ip using python:
import socket 

ip = socket.gethostbyname('www.google.com')
print ip
