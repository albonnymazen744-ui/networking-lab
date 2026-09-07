First GNS3 Network Lab

Objective

Build a simple network using GNS3 and test communication between two PCs.

Topology

PC1 ───────── PC2

IP Addressing

Device| IP Address| Subnet Mask
PC1| 192.168.1.10| /24
PC2| 192.168.1.20| /24

Configuration

PC1:

ip 192.168.1.10/24

PC2:

ip 192.168.1.20/24

Connectivity Test

A ping was performed from PC1 to PC2.

Result: Successful

The two PCs are in the same subnet:

"192.168.1.0/24"

Therefore, they can communicate directly without a router.

Wireshark Analysis

Wireshark was used to capture the ping traffic.

The packets were filtered using:

icmp

The communication consisted of:

- ICMP Echo Request — PC1 → PC2
- ICMP Echo Reply — PC2 → PC1

The packet structure observed was approximately:

Ethernet II
    └── IPv4
          └── ICMP

What I Learned

- How to create a basic topology in GNS3.
- How to configure IP addresses on VPCS.
- How devices communicate within the same subnet.
- The role of ICMP in the ping process.
- How to use Wireshark to analyze network packets.
- The difference between an IP address and a MAC address.

Next Step

The next lab will introduce a router and demonstrate communication between two different subnets.
