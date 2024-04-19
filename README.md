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
client:
```
 
 
import socket 
s=socket.socket() 
s.connect(('localhost',8080)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode()) 
```
server:
```
 
import socket 
s=socket.socket() 
s.bind(('localhost',8080)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
            ClientMessage=c.recv(1024).decode() 
            print("Client > ",ClientMessage) 
            msg=input("Server > ") 
            c.send(msg.encode())
```

## OUPUT
server
![image](https://github.com/Priyanghaofficial/3b_CHAT_USING_TCP_SOCKETS/assets/147121154/74b5503f-6551-4c3b-9f20-2a6005f5a4a0)

client
![image](https://github.com/Priyanghaofficial/3b_CHAT_USING_TCP_SOCKETS/assets/147121154/2b2650cb-7e5d-46ad-b2b2-8fc4a1cc8d44)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
