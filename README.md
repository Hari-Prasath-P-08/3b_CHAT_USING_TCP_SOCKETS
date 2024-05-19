# 3b.CREATION FOR CHAT USING TCP SOCKETS

### Name: HARI PRASATH. P
### Reg. No: 212223230070

## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM:

## CLIENT:

```python
   import socket
   
   s=socket.socket()
   
   s.connect(('localhost',8000))
   
   while True:
       
       msg=input("Client > ")
       
       s.send(msg.encode())
       
       print("Server > ",s.recv(1024).decode())
```

## SERVER:

```python
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

## OUPUT:

![326367849-fced3315-227b-4227-bfa2-168514279b6b](https://github.com/Hari-Prasath-P-08/3b_CHAT_USING_TCP_SOCKETS/assets/139455593/f527b4b9-a644-4384-ab9c-5fd766603d47)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
