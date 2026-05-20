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
## CLIENT
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## SERVER
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
## CLIENT
<img width="910" height="152" alt="Screenshot 2026-05-20 085227" src="https://github.com/user-attachments/assets/e069ae17-d10e-480a-a097-ca73dbf8b9e6" />

## SERVER
<img width="923" height="152" alt="Screenshot 2026-05-20 085243" src="https://github.com/user-attachments/assets/afe369ea-16ff-43dd-be9e-d5b54bd7e466" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
