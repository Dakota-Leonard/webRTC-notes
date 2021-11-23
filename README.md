# webRTC-notes

WebRTC = Web Real-Time Communication

## Overview
* Used to find a peer to peer path to exchange video and audio in an efficient and low latency manner.
* Standardized API
* Enables rich communications between browsers

General Steps:
1. A wants to connect to B.
2. A finds out all possible ways the public can connect to it.
3. B finds out all possible ways the public can connect to it.
4. A and B signal this session information via other means (WhatsApp, QR, Tweet, WebSockets, HTTP Fetch, etc)
5. A connects to B via the most optimal path.
6. A & B also exchange their supported media and security.

## NAT  (Network Address Translation)
* Different translation methods: One to One NAT (Full-cone NAT), Address restricted NAT, Port restricted NAT, Symmetric NAT.
* WebRTC does not like Symmetric NAT.
* One to One NAT (Full cone NAT) - Packets to external IP:port on the router always map to internal IP:port without exceptions.
* Address Restricted NAT - Packets to external IP:port on the router always maps to internal IP:port as long as source address from packet matches the table (regardless of port). If it has communicated with the host before it is allowed.
* Port Restricted NAT - Packets to external IP:port on the router always map to internal IP:port as long as source address and port from the packet matches the table. If it has communicated with this host:port before it is allowed
