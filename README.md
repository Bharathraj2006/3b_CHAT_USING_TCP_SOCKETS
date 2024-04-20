# 3b.CREATION FOR CHAT USING TCP SOCKETS
## Register Number : 212223230031
## Name : P.Bharathraj
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### Client
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
### Server
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
```
## OUPUT
### Client
![Screenshot 2024-04-20 084739](https://github.com/Bharathraj2006/3b_CHAT_USING_TCP_SOCKETS/assets/152376845/3ebab851-c26e-49cc-98bf-c8b96a733743)

### Server
![Screenshot 2024-04-20 084754](https://github.com/Bharathraj2006/3b_CHAT_USING_TCP_SOCKETS/assets/152376845/3edaeada-b354-4839-bada-15b9ba045033)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
