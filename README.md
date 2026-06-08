#OUTPUT-> 

Starting Network Sniffer...

Source IP      : 10.142.90.71
Destination IP : 52.178.17.2
Protocol       : 6
----------------------------------------
Source IP      : 10.142.90.71
Destination IP : 52.178.17.2
Protocol       : 6
----------------------------------------
Source IP      : 10.142.90.71
Destination IP : 52.178.17.2
Protocol       : 6
----------------------------------------
Source IP      : 10.142.90.71
Destination IP : 52.178.17.2
Protocol       : 6
----------------------------------------
Source IP      : 52.178.17.2
Destination IP : 10.142.90.71
Protocol       : 6
----------------------------------------
Source IP      : 52.178.17.2
Destination IP : 10.142.90.71
Protocol       : 6
----------------------------------------
Source IP      : 52.178.17.2
Destination IP : 10.142.90.71
Protocol       : 6
----------------------------------------
Source IP      : 10.142.90.71
Destination IP : 52.178.17.2
Protocol       : 6
----------------------------------------
Source IP      : 52.178.17.2
Destination IP : 10.142.90.71
Protocol       : 6
----------------------------------------
Source IP      : 10.142.90.71
Destination IP : 52.178.17.2
Protocol       : 6
----------------------------------------                                                                                                                                                                                                                        


# Basic-Network-Sniffer
 

1.  from scapy.all import sniff, IP
-> This line imports the sniff() function and the IP class from the Scapy library.
-> sniff() is used to capture network packets.
-> IP is used to access information from the IP layer of a packet.

2.  print("Starting Network Sniffer...\n")
-> This line displays a message indicating that the network sniffer has started and is ready to capture packets.

3. def capture_packet(packet):
 -> This defines a function named capture_packet.
 -> The function is automatically called whenever a packet is captured.

4. if packet.haslayer(IP):

-> This checks whether the captured packet contains an IP layer.
-> Only packets with IP information are processed.

5. print("Source IP :", packet[IP].src)
-> This extracts and displays the source IP address.
-> The source IP identifies the device that sent the packet.

6. print("Destination IP :", packet[IP].dst)
-> This extracts and displays the destination IP address.
-> The destination IP identifies the device receiving the packet.

7. print("Protocol :", packet[IP].proto)
This displays the protocol number used by the packet.
Examples:
1 = ICMP
6 = TCP
17 = UDP
   
8. print("-" * 40)
-> This prints a separator line of 40 hyphens.
-> It makes the output easier to read by separating packet details.
   
9. sniff(prn=capture_packet, count=10)
-> This starts the packet-capturing process.
-> prn=capture_packet tells Scapy to send each captured packet to the capture_packet() function.
-> count=10 means the program will stop after capturing 10 packets.

   
Working of the Program
1. The program starts and imports the required Scapy modules.
2. A message is displayed indicating that packet capture has begun.
3. The sniff() function begins listening to network traffic.
4. Whenever a packet is captured, the capture_packet() function is executed.
5. The function checks if the packet contains an IP layer.
6. If an IP layer exists, the source IP, destination IP, and protocol number are extracted and displayed.
7. The process repeats for each packet.
8. After capturing 10 packets, the sniffer automatically stops.


Purpose of the Code
-> To monitor network traffic.
-> To learn how packet sniffing works.
-> To identify source and destination IP addresses.
-> To understand different network protocols.
->To build a foundation for network analysis and cybersecurity projects.
