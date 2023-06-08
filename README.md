# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER

# DATE :26-04-2023

# AIM :
To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.


# ALGORITHM :
Import the necessary modules in python Create a socket connection to using the socket module.
Send message to the client and receive the message from the client using the Socket module in server. 
Send and receive the message using the send function in socket.

# PROGRAM :
# CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())

```

# SERVER:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
   ClientMessage=c.recv(1024).decode()
   c.send(ClientMessage.encode())
```


# OUTPUT :
# CLIENT OUTPUT :
![243255348-a6be0354-6125-4399-9e9b-0c3a01f35900](https://github.com/Hemaprasad-N/EX-8/assets/135933397/076b4cbf-fbf2-46d7-bd07-af3fb961bf8c)

# SERVER OUTPUT:
![243255445-0808792f-1c81-418e-b7fa-972191155390](https://github.com/Hemaprasad-N/EX-8/assets/135933397/792b7dcf-46f0-4911-a6c1-10834dce8ab7)

# RESULT :
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
