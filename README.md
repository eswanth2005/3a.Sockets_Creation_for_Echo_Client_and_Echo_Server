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
![Screenshot (41)](https://github.com/eswanth2005/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/164656722/4d4596c6-b4aa-47fd-a130-3579496d7e70)

### SERVER:
![Screenshot (43)](https://github.com/eswanth2005/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/164656722/31dd2c88-2347-4922-a582-f920909b97d3)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
