# 2a_Stop_and_Wait_Protocol
## NAME : THARUN R
## REG.NO: 212224240172
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
## SERVER
```
import socket
s=socket.socket()
s.connect(('localhost', 8001))
while True:
print(s.recv(1024).decode())
s.send("Acknowledgement Recived frome the server".encode())
```
## CLIENT
```
import socket
s=socket.socket()
s.bind(('localhost', 8001))
s.listen(5)
c,addr=s.accept()
while True:
i=input("Enter a data: ")
c.send(i.encode())
ack=c.recv(1024).decode()
if ack:
print(ack)
continue
else:
c.close()
break
```

## OUTPUT
![WhatsApp Image 2025-04-12 at 11 31 26_5ef24cf9](https://github.com/user-attachments/assets/f58bebf7-db1e-4bfe-a5ff-bce438f96fae)
![WhatsApp Image 2025-04-12 at 11 31 27_2835dd5a](https://github.com/user-attachments/assets/6b33c85f-770d-43af-aae5-6ec06f93a35f)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
