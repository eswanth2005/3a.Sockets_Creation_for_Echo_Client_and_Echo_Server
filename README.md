# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS

## Name: ESWANTH KUMAR K
## Reg No: 212223040046
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
### CLIENT:
```import socket
s=socket.socket()
s.bind(('localhost',9000))
s.listen(5)
c,addr=s.accept()
while True:
    clientMessage=c.recv(1024).decode()
    c.send((clientMessage.encode()))

```
### SERVER:
```
import socket
s=socket.socket()
s.connect(('localhost',9000))
while True:
    msg=input("client>")
    s.send(msg.encode())
    print("server>",s.recv(1024).decode())
```
## OUPUT
### CLIENT:
![image](https://github.com/eswanth2005/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/164656722/bf41103b-51fa-4266-85c3-a3cae3d0f444)

### SERVER:
![image](https://github.com/eswanth2005/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/164656722/c165f082-0a6e-4ea9-980c-558fc99047c7)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
