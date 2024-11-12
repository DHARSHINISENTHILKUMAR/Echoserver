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
## client.py
```
import socket
HOST = "127.0.0.1"
PORT = 65432
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT)) 
    s.sendall(b"Pooja V,")
    s.sendall(b"212221040122")
    data = s.recv(1024)
print(f"\nRecived {data!r}")
```
## server.py
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

![17313874116017531811135157909121](https://github.com/user-attachments/assets/170ef77e-2f1e-4eed-b13a-d83109c3c327)

## RESULT:
The program is executed successfully
