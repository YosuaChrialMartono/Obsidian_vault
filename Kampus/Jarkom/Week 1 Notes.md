#Jarkom #College #notes 
# The internet
## Nuts and bolt view
- internet is a network of networks
- Protocols are everywhere 
	- sending and receiving messages
	- e.g., HTTP(Web), streaming video, etc.
- Internet standards
	- RFC: Request for Comments
	- IETF: Internet Engineering Task Force

## Services View
- Infrastructures that provides services to applications
- Provides programming interface
	- “hooks” allowing sending/receiving apps to “connect” to, use Internet transport service
	- provides service options, analogous to postal service

# Protocol
```
Protocols define the format, order of receiving and sending messages, action taken, and receipt
```
![[Pasted image 20230905182600.png]]

# Network edge
## Network edge:
![[Pasted image 20230905183417.png]]
- hosts: client and servers
- servers often in data centers
## Access networks, physical media:
![[Pasted image 20230905183441.png]]
- wired, wireless communication links

## Network Core
![[Pasted image 20230905183459.png]]
- interconnected routers
- network of networks

## Access networks
- residential access nets
- institutional access networks (School, company)
- mobile access networks (WiFi, 4G/5G)
![[Pasted image 20230905184058.png]]
### Cable-based access
#### frequency division multiplexing
![[Pasted image 20230905184138.png]]
**Frequency division multiplexing (FDM):** different channels transmitted in different frequency bands

![[Pasted image 20230905184456.png]]
**HFC: Hybrid Fiber Coax**
- asymmetric: up to 40 Mbps - 1.2 Gbps downstream transmission rate, 30-100 Mbps upstream transmission rate
**Network of cable,** fiber attaches homes to ISP Routers
- homes **share access network** to cable headend

### Digital Subscriber Line (DSL)

![[Pasted image 20230905185435.png]]
- use **existing** telephone line to central office DSLAM
	- data over DSL phone line goes to internet
	- voice over DSL phone line goes to telephone net
- 24-52 Mbps dedicated downstream transmission rate
- 3.5-16 Mbps dedicated upstream transmission rate
### Home Networks
![[Pasted image 20230905185652.png]]
***Uses wireless access networks***

### Wireless access networks
*Connects end system to router*
	via base station aka "access point"
#### Wireless local area networks (WLANs)
- usually in or around building (~100 ft)
- 802.11b/g/n (WiFi): 11, 54, 450 Mbps transmission rate
- ![[Pasted image 20230905185926.png]]

#### Wide-area cellular access networks
- provided by mobile, cellular network operator (10's km)
- 10's Mbps
- 4G Cellular networks
- ![[Pasted image 20230905190037.png]]

### Enterprise Networks
![[Pasted image 20230905190106.png]]
- Companies, universities, etc.
- mix of wired, wireless link technologies, connecting a mix of switches and routers
	- Ethernet: wired access at 100Mbps, 1Gbps, 10Gbps
	- WiFi: wireless access points at 11, 54, 450 Mbps

### Data Center Networks
high-bandwidth links (10s to 100s Gbps) connect hundreds to thousands of servers together, and to Internet
![[Pasted image 20230905190211.png]]
![[Pasted image 20230905190218.png]]

## Host: sends *packets* of data
host sending function:
1. takes application message
2. breaks into smaller chunks, known as *packets*, of length *L* bits
3. transmits packet into access networks at *transmission rate R*
	- link transmission rate, aka link *capacity, aka link bandwith*
	- ![[Pasted image 20230905190409.png]]
- ![[Pasted image 20230905190416.png]]

## Links: Physical Media
- bit: propagates between transmitter/receiver pairs
- physical link: what lies between transmitter & receiver
- guided media: 
	- signals propagate in solid media: copper, fiber, coax
- unguided media:
	- signals propagate freely, e.g., radio
### Twisted pair(TP)
- two insulated copper wires
	- Category 5: 100 Mbps, 1 Gbps Ethernet
	- Category 6: 10Gbps Ethernet
	![[Pasted image 20230905190756.png]]
### Coaxial cable:
- two concentric copper conductors
- bidirectional
- broadband:
	- multiple frequency channels on cable 
	- 100’s Mbps per channel
	- ![[Pasted image 20230905190912.png]]

### Fiber optic cable:
- glass fiber carrying light pulses, each pulse a bit 
- high-speed operation: 
	- high-speed point-to-point transmission (10’s-100’s Gbps)
- low error rate: 
	- repeaters spaced far apart 
	- immune to electromagnetic noise
	- ![[Pasted image 20230905191018.png]]

### Wireless radio
- signal carried in various “bands” in electromagnetic spectrum 
- no physical “wire” 
- broadcast, “half-duplex” (sender to receiver) 
- propagation environment effects: 
	- reflection 
	- obstruction by objects 
	- Interference/noise

### Radio link types
- Wireless LAN (WiFi) 
	- 10-100’s Mbps; 10’s of meters 
- wide-area (e.g., 4G cellular) 
	- 10’s Mbps over ~10 Km 
- Bluetooth: cable replacement 
	- short distances, limited rates 
- terrestrial microwave 
	- point-to-point; 45 Mbps channels 
- satellite 
	- up to 45 Mbps per channel 
	- 270 msec end-end delay

# The network core
- mesh of interconnected routers
- *packet-switching:* hosts break application-layer messages into *packets*
	- network **forwards** packets from one router to the next, across links on path from **source to destination**

### Forwarding
![[Pasted image 20230905192059.png]]

- aka "switching"
- *local* action: 
	  move arriving packets from router's input link to appropriate router output link
### Routing
![[Pasted image 20230905192053.png]]
- routing algorithms
- global action:
	determine source destination paths taken by packets

### Packet-switching: store-and-forward

![[Pasted image 20230905192344.png]]

- ***packet transmission delay:*** takes *L/R* seconds to transmit (push out) *L*-bit packet into link at *R* bps
- ***store and forward:*** *entire* packet must arrive at router before it can be transmitted on next link
![[Pasted image 20230905192540.png]]

### Packet-switching: queueing

![[Pasted image 20230905192707.png]]

***Queueing*** occurs when work arrives faster that it can be serviced

***Packet queuing and loss:*** if arrival rate (in bps) to link exceeds transmission rate (bps) of link for some period of time:
- packets will queue, waiting to be transmitted on output link
- packets can be dropped (lost) if memory (buffer) in router fills up
#### Alternative to packet switching circuit switching
![[Pasted image 20230905193345.png]]
`end-end resources allocated to, reserved for "call" between source and destination`

- in diagram, each link has four circuits.
	- call gets 2nd circuit in top link and 1st circuit in right link
- dedicated resources: no sharing
	- circuit-like (guaranteed) performance
- circuit segment idle if not used by call (**no sharing**)
- commonly used in traditional telephone networks

## Circuit switching: FDM and TDM
![[Pasted image 20230905193626.png]]
### Frequency Division Multiplexing (FDM)
- optical, electromagnetic frequencies divided into (narrow) frequency bands.
- each call allocated its own band, can transmit at max rate of that narrow band.

### Time Division Multiplexing (TDM)
- time divided into slots
- each call allocated periodic slot(s), can transmit at maximum rate of (wider) frequency band (only) during its time slot(s)

## Packet switching vs circuit switching
![[Pasted image 20230905193746.png]]
Q : how many users can use this network under circuit-switching and packet switching?
A : 
- Circuit-switching: 10 users
- packet switching: with 35 users, probability > 10 active at same time is les than .0004*

probability can be further explored *

### Is packet switching the winner?
- great for "bursty" data - sometimes has data to send, but at other times not
	- resource sharing
	- simpler, no call setup
- **excessive congestion possible:** packet delay and loss due to buffer overflow
	- protocols needed for reliable data transfer, congestion control

## Internet structure: a “network of networks”
```
connecting each access ISP to each other directly doesn’t scale: O(N2 ) connections.
```

![[Pasted image 20230905194839.png]]
- Connecting multiple isps to one central ISP, though there would be many ISP since there is also a lot competition for them
- We will connect those ISP's with IXP(Internet exchange point) and peering link(red line between isp), 
- Regional ISP to connect access nets to ISPs 
- content provider networks (e.g., Google, Microsoft, Akamai) may run their own network, to bring services, content close to end users

![[Pasted image 20230905195251.png]]

- at the center there is a small number of well connected large networks
	- “tier-1” commercial ISPs (e.g., Level 3, Sprint, AT&T, NTT), national & international coverage
	- content provider networks (e.g., Google, Facebook): private network that connects its data centers to Internet, often bypassing tier-1, regional ISPs