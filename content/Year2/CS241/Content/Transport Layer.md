TCP (Transmission Control Protocol) is a transport layer protocol

## TCP
### Fast Retransmit

- duplicate acknowledgements indicate something is wrong e.g. something needs to be resent
- Receiving 3 duplicate acks -> resend without waiting for timeout 

### TCP Flow Control

Control the rate at which sender sends data, using a receive window field.

- Data in pipeline should not exceed **receive buffer size** -> overflow 
- Tell the sender the receive window (rwnd)
	- rwnd is amount of free buffer space 
- Ensure $\text{LastByteSent} - \text{LastByteAcked} \leq \text{rwnd}$
	- this is because in-flight data is stored in the buffer 

### TCP Congestion Control

Reduce rate at which sender sends data if high perceived congestion
- want to reduce congestion
- congestion occurs when $\text{input rate} > \text{output rate}$

WHY do we want to reduce congestion?
- lost packets (buffer overflow)
- long delays from queueing in router buffers?
## Go Back N (GBN)

Only accept packets in order. 
- Lost packets handled poorly -> sending duplicate packets

## Selective Repeat (SR)