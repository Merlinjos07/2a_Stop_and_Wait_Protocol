# 2a_Stop_and_Wait_Protocol
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM

CLIENT:
```
import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept()
while True:
i=input("Enter a data: ")
c.send(i.encode())
Type your text
ack=c.recv(1024).decode()
if ack: 
print(ack) 
continue
else: 
c.close() 
break
```
SERVER:

```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True:
print(s.recv(1024).decode())
s.send("Acknowledgement Recived".encode())
```

## OUTPUT
<img width="1153" height="967" alt="image" src="https://github.com/user-attachments/assets/eb6e5ee0-0962-4870-8048-992a5e458444" />
<img width="1138" height="857" alt="image" src="https://github.com/user-attachments/assets/f8e242c4-2180-4dc9-a76a-e832adee291c" />

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
