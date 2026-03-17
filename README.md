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
[WhatsApp Image 2026-03-17 at 18 47 51](https://github.com/user-attachments/assets/00b1283d-ac9d-46cc-8bdf-7ec9e4dd86c7)
## client
[WhatsApp Image 2026-03-17 at 18 48 04](https://github.com/user-attachments/assets/8980e613-5626-427f-8be4-0952cc341638)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
