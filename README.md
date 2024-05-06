# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
CLIENT
```
import socket
s=socket.socket()
s.connect(('localhost',800))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
SERVER
```
import socket
s=socket.socket()
s.bind(('localhost',800))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
```
## OUPUT
CLIENT OUTPUT

![image](https://github.com/mdgj2005/3b_CHAT_USING_TCP_SOCKETS/assets/145533936/a8b74bc2-3934-4634-8bc8-9b53c21985fb)

SERVER OUTPUT

![image](https://github.com/mdgj2005/3b_CHAT_USING_TCP_SOCKETS/assets/145533936/f8ee84e2-2b96-481d-ac9e-ac78c32cc239)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
