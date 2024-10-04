# Introduction 
## What's a DHCP 
DHCP (Dynamic Host Configuration Protocol) it's a protocol that offers IP's addresses automaticaly to network devices to identify and administrate private or local networks.

This is usually helpful for administrators 'cause if you know anything about administrate local networks manually, you can say that it is very tedious.
So in this documentation you'll see how to install this service and how it works.

## How it works?

![Img](https://imgs.search.brave.com/aa1oDanJVZpIlxpir4-xMj9SPVVTEQ1GKL41oprl7go/rs:fit:860:0:0:0/g:ce/aHR0cHM6Ly93d3cu/dGVjaHRhcmdldC5j/b20vcm1zL29ubGlu/ZUltYWdlcy9uZXR3/b3JraW5nLWRoY3Bf/aGFuZHNoYWtlX21v/YmlsZS5qcGc)

The DHCP protocol works through a four-step process known as DORA or DHCP Handshake: Discovery, Offer, Request, and Acknowledgment.

1. DHCP Discovery (DHCPDISCOVER)
When a client device (such as a laptop or phone) joins a network, it sends out a DHCPDISCOVER message to discover DHCP servers on the network.
This is a broadcast message, meaning it’s sent to all devices on the local network because the client doesn’t have an IP address yet.

3. DHCP Offer (DHCPOFFER)
When a DHCP server receives the DHCPDISCOVER message, it checks its pool of available IP addresses and assigns one to the client.
The server responds with a DHCPOFFER message, which includes:
- The offered IP address.
- Subnet mask.
- Gateway (router) address.
- Lease time (how long the client can use the IP).
- DNS server addresses (if provided).
- This message is sent back to the client, but still as a broadcast since the client doesn’t have a specific IP address yet.
4. DHCP Request (DHCPREQUEST)
The client receives the DHCPOFFER and sends back a DHCPREQUEST message to indicate that it accepts the offered IP address and configuration from the specific DHCP server.
This message is sent as a broadcast as well, to inform all DHCP servers that it is accepting an offer from a particular server (and rejecting offers from other DHCP servers, if there are any).
5. DHCP Acknowledgment (DHCPACK)
The DHCP server confirms the IP address assignment with a DHCPACK message.
This message includes the IP address, lease time, and any other network settings.
Once the client receives the DHCPACK, it configures its network interface with the provided information and starts using the network with the assigned IP address.
