# modules/01-packets-frames.md
# Module: Packets and Frames — TryHackMe


## What I Learned
- A packet contains IP address information; a frame does not
- A packet is the information inside the envelope; the frame is the envelope itself
- Packets have headers including Time to Live, Checksum, Source address, and Destination address
- **Three-Way Handshake**: the process used to establish a connection between two devices
  - **SYN** — initial packet sent by the client to initiate and synchronize the connection
  - **SYN/ACK** — sent by the server to acknowledge the client's sync attempt
  - **ACK** — confirms a series of messages/packets were successfully received (used by either side)
  - **DATA** — actual data (e.g. file bytes) sent once the connection is established
  - **FIN** — cleanly closes the connection once communication is complete
  - **RST** — abruptly terminates the connection, indicating an error (e.g. service failure, low resources)

## What I Did

**Re-Assembling TCP Handshake Lab**
1. Clicked SYN
2. Clicked SYN/ACK
3. Clicked ACK
4. Clicked DATA
5. Clicked FIN
6. Clicked ACK
7. Clicked FIN
8. Clicked ACK

**Ports 101 Practical Lab**
1. Entered the IP address and port number into the terminal
2. Successfully connected to the open port

## What I'd Do Next
In a real investigation, I'd use this to read a packet capture and reconstruct what actually happened in a session — for example, spotting a handshake that never completes (SYN with no SYN-ACK reply) as a possible sign of a SYN flood or port scan, or seeing unexpected RST packets as a sign something failed or was blocked. 

---
*Completed: 6/30/26 | Room: https://tryhackme.com/room/packetsframes*
