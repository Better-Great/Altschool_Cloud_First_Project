# Subnet Analysis for IP Address 193.16.20.35/29
## In this section, we will explore the subnet characteristics of the IP address 193.16.20.35 with a subnet mask of /29. Our focus will be on identifying the Network IP, the total number of hosts allowed within this subnet, the range of usable IP addresses, and the broadcast IP address

### Understanding Subnet Mask
The `/29` at the end of the IP address `(193.16.20.35/29)` is a shorthand for the subnet mask. Since a subnet mask tells us how many bits of the address are used for the network portion with the remaining bits used for host addresses. The `/29` means that the **first 29 bits of the IP address are designated for the network portion, leaving the remaining bits for host addresses**.
### Calculating the Subnet Mask in Decimal
The conversion of subnet mask to decimal helps visualize the division between the network and host portions of addresses. Therefore, a `/29` subnet mask corresponds to the binary mask `11111111.11111111.11111111.11111000`, which translates to `255.255.255.248` in decimal notation.
### Calculating the Network Address
To obtain the network address, a simple model is employed. 

First, we begin by calculating the IP address and converting it to binary. To convert a decimal number into binary, you align it with the powers of 2, which are, from left to right: 128, 64, 32, 16, 8, 4, 2, 1. Each position represents a binary digit (bit), which can be either 0 or 1. 

`Where IP= 193.16.20.35/29`
Using the model of identifying the power of 2: 128 64 32 16 8 4 2 1  
**For 193**  
Subtract from 193:
- 128 fits into 193. Subtract to get 65. (Binary so far: 1)  
- 64 fits into 65. Subtract to get 1. (Binary so far: 11)  
- Powers 32, 16, 8, 4, 2 do not fit into 1. (Binary so far: 1100000)  
- 1 fits into 1. Subtract to get 0. (Complete Binary: 11000001)  

**The binary equivalent of 193 is 11000001**  

**For 16**  
Subtract from 16:  
- **16** fits into 16. Subtract to get 0. (Binary so far: 1)  
- Powers 128, 64, 32, 8, 4, 2, 1 (except for 16) either don't fit or are not considered because we've reached a remainder of 0.

**The binary equivalent of 16 is 00010000**.  

**For 20**  
Subtract from 20:  
- **16** fits into 20. Subtract to get 4. (Binary so far: 1)  
- **8**, **32**, **64**, and **128** do not fit into 4. (Binary so far: 10000)  
- **4** fits into 4. Subtract to get 0. (Binary so far: 10001)  
- **2** and **1** do not fit into 0. (No changes to binary so far)

**The binary equivalent of 20 is 00010100**.

**For 35**  
Subtract from 35:  
- **32** fits into 35. Subtract to get 3. (Binary so far: 1)  
- **16**, **8**, **64**, and **128** do not fit into 3. (Binary so far: 100000)  
- **4** does not fit into 3. (No change to binary so far)  
- **2** fits into 3. Subtract to get 1. (Binary so far: 100001)  
- **1** fits into 1. Subtract to get 0. (Binary so far: 1000011)

**The binary equivalent of 35 is 00100011**.

The ip address for `193.16.20.35/29` is `11000001  00010000  00010100  00100011`  
#### To Obtain the Network Address
The network address is the first address in a subnet, representing the subnet itself in network communications.   
Since `/29` implies the first 29 digit belong to the network and the last 3 to the host. The network address can be represented with ` 11000001 00010000  00010100  00100 000`. Here in the last octet,`000` represent the host. **The network address could also be written as** `193.16.20.32/29`  
### Calculate the Number of Usable Hosts
To calculate the number of usable host, yo use 2 raised to the power of the number of host bits. In our case (32-29=3 hosts). **Therefore 2^3 = 8**  
Now it is important to note that one address is reserved for the network identifier, and another is reserved for the broadcast address. Therefore from the 8 gotten we subtract 2, (8-2=6) which gives us **6 usable IP addresses**
### Find the Broadcast Address  
The broadcast address is the last address in the subnet and is used to send data to all hosts within that subnet. To find it, you make all the host bits in the address '1'.  
This implies that from ` 11000001 00010000  00010100  00100 000` using the last octet we now have ` 11000001 00010000  00010100  00100 111` since `000` is the host.   
Since we changed the last octet which is the network address 193.16.20.32 also written as 00100000 in binary form to 00100111 which is 39 in decimal. Therefore, the broadcast address is `193.16.20.39.`  
### Determine the Range of IP Addresses
In simple terms, the rannge of ip addresses is the broadcast address -1 and network address +1.   
Since the network address is 193.16.20.32 as previously calculated,. The first usable IP address is `193.16.20.33` because of the addition of one (+1).  
Furthermore, since the broadcast address is 193.16.20.39,the last usable IP address is `193.16.20.38`. This is because of the subtraction of one (-1) from the broadcast address.   
**Therefore, the  IP addresses, from 193.16.20.33 to 193.16.20.38, represent the range of addresses available for devices within the subnet.** This range includes 6 addresses, suitable for assigning to hosts, servers, or any other devices that need to be part of this subnet. 
