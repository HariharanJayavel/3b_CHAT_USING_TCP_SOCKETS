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
### CLIENT.PY
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
### SERVER.PY
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
### CLIENT.PY
![Screenshot 2024-04-10 184606](https://github.com/HariharanJayavel/3b_CHAT_USING_TCP_SOCKETS/assets/144870546/bb5336c7-43f7-43d1-a04d-1008022f22a9)
### SERVER.PY
![Screenshot 2024-04-10 184554](https://github.com/HariharanJayavel/3b_CHAT_USING_TCP_SOCKETS/assets/144870546/8b38da7b-25d9-4903-96db-1ba7318831f3)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
