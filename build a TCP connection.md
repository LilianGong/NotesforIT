### Steps for Building a TCP Connection


Assuming that we now have two networks: **network A** (IP address: 10.1.1.0/24) and **network B** (IP address: 192.168.1.0/24), they are connected to the same router: **router C** (with a interface 10.1.1.1 through network A, and a interface 192.168.1.1 through network B). *\<physical layer>*

Now there is a client named **computer 1** in network A, whose IP address is 10.1.1.12 and acquire data from **computer 2**, a server set in network B, whose IP address is 192.168.1.25 and listening on port 80. *\<physical layer>*

Here are the detailed steps of building a TCP connection between  computer 1 and computer 2:

1. First of all, computer 1 opened a web browser and entered the IP address of computer 2, which is 192.168.1.25, indicating it wants to acquire data from computer 2. *\<application layer>*

2. Then, the web browser communicated with the local networking stack (in the operating system), and the networking stack began examining its own subnet. Soon the networking stack found out that computer 1 lived on the netwo10.1.1.0/24, so it was not in the same subnet as computer 2. Therefore, computer 1 known that it should send data to the gateway for routing to a remote network with the configured gateway of 10.1.1.1. *\<application layer>*

3. Next, to send data to the gateway, computer 1 should know the **MAC address** of the gateway. So, computer 1 looked up its ARP table, but it couldn’t find the MAC address of gateway. Therefore, it broadcasted the FF:FF:FF:FF:FF and the gateway received its broadcast, and sent its MAC address 00:11:22:33:44:55 to computer 1. *\<data link layer>*

4. Then, the operating system found the ephemeral port 51000 were available, so it opened a socket connecting the web browser to this port, and began building up a TCP segment including source port of 51000, destination port of 80, a sequence number and a SYN flag. *\<transport layer>*

5. Next, the TCP segment was inserted as the data payload for the IP datagram with a **checksum** to calculate for the whole thing. The IP header included the source IP address, the destination IP address, and a **TTL of 64**. *\<network layer>*

6. Then, the IP datagram was inserted as the data payload for the Ethernet frame which also contained the information of the source and destination MAC address (00:11:22:33:44:55) to the gateway. and another **checksum** is calculated and checked.*\<data link layer>*

7. Next, the switch received the whole Ethernet frame and inspected its destination MAC address, then sent the binary data from computer 1 through a CAT6 cable to the gateway of Router C. Router C calculated the checksum and compared this checksum with the one in the Ethernet frame and check if they match. *\<physical layer, data link layer>*

8. Then, router C striped away the Ethernet frame, leaving it with just the IP datagram. Again it performed the checksum check against the IP datagram to make sure all data were received.*\<data link layer>*

9. Next, router C inspected the destination IP address in the IP datagram, and lookup it up on its **routing table** and found itself was connected to the network B where the computer 2 lied in.*\<network layer>*

10. Then, router C decremented the TTL by 1 and recalculated a new checksum, then made a new IP datagram with this data and sent it to the computer 2 though the gateway: 192.168.1.1. *\<network layer>*

11. Next, computer 2 striped the IP datagram, leaving it with just the TCP segment. Again, the checksum for this layer was examined, and the destination port was examined and checked too. Computer 2 then saw that this packet has the SYN flag set. So it examined the sequence number and stores that, since it would need to put that sequence number in the acknowledgement field once it crafts the response.*\<transport layer>*

Till now, we’ve finally finished a single TCP segment containing a SYN flag from computer 1 to computer 2.
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTkwOTM5Njc3MSwtNjMwNTUzNjAxXX0=
-->