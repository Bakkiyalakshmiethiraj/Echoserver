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
## Server.py
```
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_server((HOST, PORT)) as s:
    conn, addr = s.accept()
    with conn:
        print(f'Connected by {addr}')
        while data := conn.recv(1024):
            conn.sendall(data)
```

## Client.py
```
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_connection((HOST, PORT)) as s:
    s.sendall(b'Bakkiyalakshmi E., 2122223220012')
    print(f'Received: {s.recv(1024)!r}')
```
## OUTPUT:

![Screenshot 2025-03-03 135710](https://github.com/user-attachments/assets/76097980-f7c7-412b-9bbb-ac604bbbeeab)

## RESULT:
The program is executed successfully.
