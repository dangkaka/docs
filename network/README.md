## Basic

#### [OSI Model](https://en.wikipedia.org/wiki/OSI_model)

TL;DR The Open Systems Interconnection model (OSI model) is a conceptual model that characterizes and standardizes the communication functions of a telecommunication or computing system without regard to its underlying internal structure and technology. There are 7 layers

| Layer | Protocol data unit | Function | Examples |
| ---- | ---- | ---- | ---- |
| Physical |  Bit | Transmission and reception of raw bit streams over a physical medium | |
| Data link | Frame | Reliable transmission of data frames between two nodes connected by a physical layer | |
| Network | Packet | Structuring and managing a multi-node network, including addressing, routing and traffic control | IP (Internet Protocol) |
| Transport | Segment (TCP) / Datagram (UDP) | Reliable transmission of data segments between points on a network, including segmentation, acknowledgement and multiplexing | |
| Session | Data | Managing communication sessions, i.e. continuous exchange of information in the form of multiple back-and-forth transmissions between two nodes | |
| Presentation | Data | Translation of data between a networking service and an application; including character encoding, data compression and encryption/decryption | |
| Application | Data | High-level APIs, including resource sharing, remote file access | Telnet, FTP, SMTP, HTTP|
