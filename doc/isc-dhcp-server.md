# DHCP SERVER
### Files
For the main server, we will need to edit the following files to configure it properly. First, we must install the service called `isc-dhcp-server` and configure the server with a static IP address.

First we install the service:
```
apt update 
apt upgrade
apt install isc-dhcp-server
```
After that, we can configure the following files:
`/etc/default/isc-dhcp-server`, `/etc/dhcp/dhcpd.conf` and `/etc/network/interfaces`

First, we need to configure /etc/network/interfaces to set a static IP address.
