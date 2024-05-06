# 3b.CREATION FOR CHAT USING TCP SOCKETS
## Name : P.Bharathraj
## Register Number : 212223230031
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
![image](https://github.com/Bharathraj2006/3b_CHAT_USING_TCP_SOCKETS/assets/152376845/516338b3-f35a-43d1-a4bc-bf11b48a1b82)


### Server
![image](https://github.com/Bharathraj2006/3b_CHAT_USING_TCP_SOCKETS/assets/152376845/717dbe16-560c-4e81-a956-287dc208aade)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
