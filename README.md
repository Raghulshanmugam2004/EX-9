# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER
# DATE :04-05-2023

# AIM :
To write a python program for creating Chat using TCP Sockets Links.

# ALGORITHM :

1.Start the program.

2.Get the frame size from the user.

3.To create the frame based on the user request.

4.To send frames to server from the client side.

5.If your frames reach the server, it will send ACK signal to client otherwise it will sendNACK signal to client.

6.Stop the program

# PROGRAM :
# CLIENT :
```
# Developed By : RAGHUL.S
# Register Number : 212222040128
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
 ```
# SERVER :
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    print("Client > ",ClientMessage)
    msg=input("Server > ")
    c.send(msg.encode())
```
# OUTPUT :
# CLIENT :
![image](https://github.com/Raghulshanmugam2004/EX-9/assets/119561118/c075372f-8faa-4f94-b1db-84df6fcd6247)
# SERVER :
![image](https://github.com/Raghulshanmugam2004/EX-9/assets/119561118/d55430a8-f425-4c90-bb40-ef85417c43df)
# RESULT :
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
