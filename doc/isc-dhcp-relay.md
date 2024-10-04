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
After installation, we will need to configure the local network and the configuration files once again.

### 1. /etc/network/interfaces
![img](/img/Net-relay.png)
Change the address and the netmask to match your local network. After that, we will configure the DHCP server files.
### 2. /etc/default/isc-dhcp-relay
![img](/img/relay-config.png)
### 3. /etc/sysctl.conf
![img](/img/ipforwarding.png)
