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
```
# echo-server.py

import socket
HOST = "127.0.0.1"  # Standard loopback interface address (localhost)
PORT = 65432  # Port to listen on (non-privileged ports are > 1023)

with socket.socket(socket.AF_INE
T, socket.SOCK_STREAM) as s:
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
```
# echo-client.py
import socket


HOST = "127.0.0.1"  # The server's hostname or IP address
PORT = 65432  # The port used by the server


with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    s.sendall(b"Hello, world")
    data = s.recv(1024)


print(f"Received {data!r}")
```        
## OUTPUT:
<img width="722" height="626" alt="2" src="https://github.com/user-attachments/assets/25a45821-5717-4f09-bd47-9cbdfe6ac8f5" />
<img width="1600" height="532" alt="1" src="https://github.com/user-attachments/assets/99147327-279d-422f-a187-4e4aa1db4741" />
<img width="1600" height="621" alt="3" src="https://github.com/user-attachments/assets/36ccdb08-6ba6-422c-b6db-590abb3fcc7c" />

## RESULT:
The program is executed successfully
