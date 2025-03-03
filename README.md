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
## Client Code :
```
import socket

HOST = "127.0.0.1"
PORT = 65432

with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    s.sendall(b"Hello, I am Vasanth 03-03-2025")
    data = s.recv(1024)

print(f"Received {data!r}")
```
## Server Code :
```
import socket

HOST = "127.0.0.1"
PORT = 65432 

with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.bind((HOST, PORT))
    s.listen()
    conn, addr = s.accept()
    with conn:
        print(f"Connected by {addr}")
        while True:
            data = conn.recv(1024)
            if not data:
                break
            conn.sendall(data)
```

## OUTPUT:

![Screenshot 2025-03-03 114310](https://github.com/user-attachments/assets/76c437bd-1b65-4c20-a05c-188eec9f55ba)


## RESULT:
The program is executed successfully
