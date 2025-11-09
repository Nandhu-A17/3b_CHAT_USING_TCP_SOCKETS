# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
Server:
~~~
 
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
~~~
Client:
~~~
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
~~~
## OUPUT
<img width="677" height="307" alt="image" src="https://github.com/user-attachments/assets/3ac3a7ca-b5b7-4aae-b518-233743118b44" />
<img width="658" height="292" alt="image" src="https://github.com/user-attachments/assets/2f785a33-05aa-420b-b801-91b0e31fcb01" />
## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
