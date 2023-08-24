# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
### CLIENT
```py
import socket

s=socket.socket()
s.connect(('localhost',65124))
while(1):
msg=input("Client>")
s.send(msg.encode())
print("Server>"+s.recv(1024).decode())
```
### SERVER
```py
import socket

s=socket.socket()
s.bind(('localhost',65124))
s.listen(5)
c,addr=s.accept()

while(1):
msg=c.recv(1024).decode()
print(msg)
c.send(msg.encode())
```

## OUTPUT:
### CLIENT
![Screenshot 2023-08-24 155846](https://github.com/Sanjay-2610/Echoserver/assets/91368803/0ceafa68-0984-4b8e-80cd-465a4670f6c3)

### SERVER
![Screenshot 2023-08-24 155859](https://github.com/Sanjay-2610/Echoserver/assets/91368803/3e9d32f0-8bf6-4c64-aec1-bedf9ca9d096)

## RESULT:
The program is executed successfully
