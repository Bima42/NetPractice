# NetPractice
Project made to learn basics of networking
Pretty simple but you have to be confortable with some concept like IP address and mask

## IP address
- allows elaboration and transport of IP datagrams (data packet) WITHOUT ENSURING THE DELIVERY
- process packets independently of each other by defining their representation, routing and forwarding
![[IP_address]](/readme_doc/ip_address.png)
---
Composed of 4 bytes, each composed of 8 bits
- a part reserved for the machine | part of the network
- Two IP addresses belong to the same subnet if they have the **subnet mask bits in common.**
- **There are unavailable addresses:**
  - **From 10.0.0.0 to 10.255.255.255.**
  - **From 172.16.0.0 to 172.31.255.255**
  - **From 192.168.0.0 to 192.168.255.255**
They are **not unique**: they are reserved for naming machines in a local network. Most of the time, the first machine connected to a Box will have the address 192.168.0.1. It is therefore **not a routable address on the Internet at all.**
---

## Mask
- Special feature: the masks include a sequence of bits of 1 then 0
- Number of machines that can be put on a network are defined by mask (right part or upper part)
![[Mask]](/readme_doc/masque_sous_reseau.png)

Example :
- **IP address: 192.168.0.0**
- **Subnet mask: 255.255.255.0**
- Takes the upper part: image above, represents a byte which is 0. Can go from 0 to 255, or 256 numbers.
- Can code 256 addresses, but 2 addresses are reserved (0 and 255)
- **0: identifies the network** (see image: _192.168.0.0_)
- **255: broadcast address** -> used to send a message to all network addresses (see image: _192.168.0.255_)
- 256 - 2 = 254 usable addresses
![[Plage]](/readme_doc/plage_adressable.png)

### CIDR
= Classless Inter-Domain Routing
- Another way to describe a mask
- gives the network number followed by a slash (or slash, “/”) and the number of bits at 1 in the binary notation of the subnet mask.
- /32 designates a network that has only one IP address, ie an individual IP address.
- _Example: The mask 255.255.224.0, equivalent in binary to 11111111.11111111.11100000.00000000, will therefore be represented by **/19** (19 bits at the value 1, followed by 13 bits 0)._

---
## Sources
- [Tuto : IP and Mask](https://www.youtube.com/watch?v=RnpSaDSSjR4)
- [Route](https://infoforall.fr/reseau/reseau-act030.html#:~:text=Etape%202%20%3A%20le%20switch%20va,de%20sa%20table%20de%20routage.)
- [Calculator](https://cric.grenoble.cnrs.fr/Administrateurs/Outils/CalculMasque/ "https://cric.grenoble.cnrs.fr/Administrateurs/Outils/CalculMasque/") 
- [Other Calculator](https://www.calculator.net/ip-subnet-calculator.html "https://www.calculator.net/ip-subnet-calculator.html") 
- [Routage](https://fr.wikipedia.org/wiki/Routage)
