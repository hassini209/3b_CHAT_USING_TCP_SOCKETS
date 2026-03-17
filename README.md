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
## server
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
## client
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## OUPUT
## server
<img width="937" height="238" alt="506706502-46742da9-77e9-4093-a954-15b23365e2f3" src="https://github.com/user-attachments/assets/9c752977-219a-4c3e-a59b-504cf1c007c3" />
## client
<img width="942" height="235" alt="506706781-44418330-ffc9-4096-9c41-880b83e41ebf" src="https://github.com/user-attachments/assets/3e35631a-9bfc-4350-be00-8fd5ed3679b7" />



## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
