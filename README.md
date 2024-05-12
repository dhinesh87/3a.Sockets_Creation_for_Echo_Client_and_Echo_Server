# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
## NAME : DHINESH.M
## REGISTER NUMBER : 212223040040
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
### CLIENT 
```py
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    clientmessage=c.recv(1024).decode()
    c.send(clientmessage.encode())

```
### SERVER 
```py
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client>")
    s.send(msg.encode())
    print("server>",s.recv(1024).decode())
```
## OUTPUT
### CLIENT OUTPUT
![CLIENT (1)](https://github.com/dhinesh87/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/146917182/d841d374-e766-4f59-a578-0e31292f4c99)

### SERVER OUTPUT
![SERVER (1)](https://github.com/dhinesh87/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/146917182/a05d5a85-6e95-4c0a-b348-b1e16f83aa84)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
