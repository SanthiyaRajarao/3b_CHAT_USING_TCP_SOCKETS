# 3b.CREATION FOR CHAT USING TCP SOCKETS
~~~
NAME : SANTHIYA R
REG NO : 212223230192
~~~
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## CLIENT
~~~
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
~~~
## SERVER
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
## OUPUT
![echo](https://github.com/SanthiyaRajarao/3b_CHAT_USING_TCP_SOCKETS/assets/144979216/7e21204a-ec05-4ec5-9d51-3bd980345621)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
