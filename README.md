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

### Server code:
```python
import socket
HOST, PORT = '192.168.183.34', 65432
with socket.create_server((HOST, PORT)) as s:
    conn, addr = s.accept()
    with conn:
        print(f'Connected by {addr}')
        while data := conn.recv(1024):
            conn.sendall(data)

```
### Client Code:
```python
import socket
HOST, PORT = '192.168.183.34', 65432
with socket.create_connection((HOST, PORT)) as s:
    s.sendall(b'KABIL , 212222040067')
    print(f'Received: {s.recv(1024)!r}')

```

## OUTPUT:
### Server side:
![Screenshot 2025-03-06 114600](https://github.com/user-attachments/assets/b6eff0d0-fbf1-4ee2-99e9-f2a726f5fe9a)



### Client side:
![Screenshot 2025-03-06 114552](https://github.com/user-attachments/assets/4f236af0-faf8-49c4-b220-c38a30ee50cf)



## RESULT:
The program is executed successfully.
