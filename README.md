# server.py
import socket

PORT=8000
HEADER=1024

server=s.socket()
server.bind((IP,PORT))
server.listen()
print(f"[LISTENING]Él servidor esta esperando conexiones en{IP}")

conn,add=server.accept()
connected=True
print (f"nueva conexion{addr}")

while True:
    encoded=conn.recv(HEADER)
    msg=encoded.decode("utf-8")
    print(f"[CLIENT]Recibi:{msg}")
