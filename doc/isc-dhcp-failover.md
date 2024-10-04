# DHCP Failover
A DHCP failover server is a backup server designed to provide high availability and redundancy in a DHCP environment. Its primary purpose is to ensure that DHCP services continue to operate smoothly in the event that the primary DHCP server fails or becomes unreachable.

### How DHCP Failover Works:
In a failover setup, two DHCP servers (the primary and the failover) share the responsibility of assigning IP addresses to clients. The failover server monitors the primary server's status and takes over if the primary server becomes unresponsive. The DHCP failover mechanism can work in two main modes:

Load balancing mode: Both the primary and failover servers are active, and they share the load of DHCP requests. Each server handles a portion of the client requests based on predefined rules (such as splitting the IP address pool).

Hot standby mode: The primary server handles all DHCP requests, while the failover server stays in a passive state. If the primary server goes down, the failover server automatically takes over all DHCP functions until the primary server is restored.

Both servers communicate regularly through a failover protocol, ensuring that the IP address lease database stays synchronized. This way, if one server fails, the other can seamlessly continue to manage the leases without causing conflicts or interruptions in network service.

In our case, we need to configure the failover in case the primary DHCP server suddenly shuts down.
