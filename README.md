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

client.py
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
server.py
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

CLIENT:

![Screenshot 2025-04-06 201403](https://github.com/user-attachments/assets/154891ee-1298-441a-989a-e5f24881f3b1)

SERVER:

![Screenshot 2025-04-06 201341](https://github.com/user-attachments/assets/8aa52348-abdd-4c8e-b75e-2b41f48347c5)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
