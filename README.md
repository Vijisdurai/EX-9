# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

## DATE : 04-05-2023

## AIM :
    To write a python program for creating Chat using TCP Sockets Links.    

## ALGORITHM :
    1. Start the program.
    2. Get the frame size from the user.
    3. To create the frame based on the user request.
    4. To send frames to server from the client side.
    5. If your frames reach the server, it will send ACK signal to client otherwise it
    will sendNACK signal to client.
    6. Stop the program.

## PROGRAM :

## CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',4000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## SERVER:
```
import socket
s=socket.socket()
s.bind(('localhost',4000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
```
## OUTPUT:
![server](https://github.com/Vijisdurai/EX-9/assets/118343184/fd846ff5-d326-41ad-a5ac-986d9c46cf26)

## CLIENT :
![client](https://github.com/Vijisdurai/EX-9/assets/118343184/d4af4d10-8c9c-45a7-bb39-aaffb6f88f1d)

## SERVER:

## RESULT:
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.


