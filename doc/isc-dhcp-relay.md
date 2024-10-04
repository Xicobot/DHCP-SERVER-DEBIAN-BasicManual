# DHCP Relay
## Function of DHCP Relay:
A DHCP Relay agent is a network device that forwards DHCP packets between clients and servers that are on different subnets. When a DHCP client sends a request for an IP address, the relay agent intercepts this request and forwards it to the DHCP server, which may be located on a different network segment. Once the DHCP server responds with an offer, the relay agent forwards this offer back to the client.

## Purpose of DHCP Relay:
The primary objective of the DHCP Relay is to enable clients in different subnets to communicate with a centralized DHCP server. This is especially useful in larger networks where a single DHCP server may need to serve multiple subnets. By using a relay agent, network administrators can reduce the complexity of deploying multiple DHCP servers and ensure efficient IP address assignment across the entire network.

In summary, the DHCP Relay facilitates the smooth operation of DHCP services across different network segments, allowing for centralized management of IP address distribution.

## Configuration and instalation guide
First we do as always
```
apt update
apt upgrade
apt install isc-dhcp-relay
```
After install, we'll have to configure once again the local network, the local file is located in `/etc/network/interfaces`

### /etc/network/interfaces
![img](/img/Net-relay.png)
