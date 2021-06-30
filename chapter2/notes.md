# Chapter 2

### Principles of Network Applications

#### Network Application Architectures

**Client-server architecture.** Always-on server host communicates with other client hosts.

* Clients don't directly communicate.
* Server has a fixed IP address.
* Example applications: Web, FTP, Telnet, e-mail.

<div style="text-align: center"><img src="./images/client_server_architecture.png" width="300px" /></div>
<div align="center">
</div>

**Data center.** Place to put many hosts together and create a powerful virtual server.

**Peer-to-peer (P2P) architecture.** No dedicated server, replies on direct communication between pairs of connected hosts (peers).

<div style="text-align: center"><img src="./images/peer_to_peer_architecture.png" width="300px" /></div>
<div align="center">
</div>

* Example applications: File sharing (BitTorrent, self-scalability), peer-assisted download acceleration (Xunlei), Skype.

Mixed architecture: Instant messaging applications.

### Processes

How processes running on different hosts communicate.

A network application consists of pairs of (client and server) processes that send messages to each other over network:

| Application      | Server                  | Client                    |
| ---------------- | ----------------------- | ------------------------- |
| Web              | Web server              | Web browser               |
| P2P file sharing | Host uploading the file | Host downloading the file |

**Client process.** The process that initiates the communication (contacts the other process to initiate comm session).

**Server process.** The process that waits to be contacted.

**Socket.** Software interface (API) between process and computer network.

<div style="text-align: center"><img src="./images/socket.png" width="600px" /></div>
<div align="center">
</div>

To send message to a process, we need 

1. the IP address of the destination host, and 
2. a port number that identifies the receiving process.

**IP address.** A 32-bit quantity that uniquely identifies the host.

**Port number.** Identifier for the receiving process on the destination host.

* E.g., web server is identified by port number 80, mail server is identified by port number 25.