# ECN-Website-Support-Check
Explicit Congestion Notification protocol is an extension to the IP protocol wherein if the qdisc (AQM) on an intermediate networking device determines it wants to drop a packet based on its calculated drop probability, rather than doing so, it will simply mark the packet if the software queue is not full to signal the TCP sender to lower its congestion window.

A TCP sender signals that it supports ECN by turning its Congestion Window Reduce (CWR) and its ECN Echo (ECE) bits on while sending a SYN during a TCP three way handshake with a receiver. If the SYN-ACK sent by the receiver has the ECE bit turned on, then the receiver supports ECN and this connection will avoid unnecessary packet drops.

The program takes an IP address as input and sends it a SYN packet with CWR and ECE bits turned on. If the response has the ECE bit turned on, then the IP address you have entered supports ECN.

The IP address of a website can be found out using the [nslookup](https://g.co/kgs/ZDeGDx) tool. It obtains the corresponding DNS mapping to the URL you've entered from which you can get the IP address. 

Scapy can be installed from [here](https://scapy.readthedocs.io/en/latest/installation.html#installing-scapy-v2-x). 