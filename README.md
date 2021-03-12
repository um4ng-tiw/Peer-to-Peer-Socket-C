# Peer to peer program in C
This program involves a peer which can send and receive simultaneously, created using Socket programming in C. Multiple instances of the code can be run in seperate terminal environments to form a peer to peer chat network.

**Limitations**
1. The program requires the user to know the port numbers of other users on the same localhost beforehand. 
2. The program is just a demonstration of TCP/IP Socket programming in C.

**Simultaneous send and receive**
The program achieves simultaneous send and receive by running the receive method on seperate thread. The program involves the use of **select()** system call to identify the ready file descriptors and loop over them to receive the messages in queue. However, this simultaneous send and receive is not refined and may interrupt the user while sending the message. 

**Running instructions**
The program was executed on a Linux system using the gcc compiler.

```
gcc peer.c -o peer1
gcc peer.c -o peer2
./peer1
./peer2
```
