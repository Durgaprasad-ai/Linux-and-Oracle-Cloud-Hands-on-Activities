# 1. What is Network Time Protocol ? its purpose ?
Ans: Network Time Protocol ( NTP ) is a protocol that is used to synchronize the clocks of computers and devices over a network. It is essential for ensuring that devices across a network have accurate time, as synchronized clocks are critical for the many network and security applications.
NTP operates over UDP ( User Datagram Protocol ) and typically used port number 123.

# Purpose of NTP :
**Logging** : Mainains accurate timestamps in logs over multiple systems.

**Scheduled Tasks :** Tools like cron requires precise system time for scheduled tasks.

**Security :** Some protocols like SSL/TLS , Kerberos rely on synchronized clocks for authentication.

**Distributed systems :** Ensures consistency in databases and time- sensitive operations. 

# Time Synchronization Process :
**NTP implementation**
> The client sends an NTP request packet to the server. The packet contains the timestamp t1 when the packet leaves the client.

> The NTP server receives the NTP request packet at t2, and returns an NTP response packet to the client at t3. This response packet carries timestamps t1, t2, and t3.

> The client receives the NTP response packet at t4.

 The client calculates the following key parameters based on the preceding four timestamps:

Round-trip delay of NTP packets between the client and the server
Rount-trip delay = ( t4 - t1 ) - ( t3 - t2 ) 

Time offset between the client and server can be caluculated by using RTD and timestamps 


NTP typically adjusts the system clock gradually to avoid the sudden jumps that can disrupt services  is called Stewing.
