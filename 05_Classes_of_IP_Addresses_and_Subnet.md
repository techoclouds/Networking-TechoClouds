
# Chapter 5: Classes of IP Addresses and Subnetting Basics

## 5.1 Classes of IP Addresses
- **Overview**: IP address classes organize the IP address space into blocks of varying sizes to suit different types of networks.
- **Class A**: Range: 1.0.0.0 to 126.255.255.255. Used in very large networks due to the large number of hosts it can accommodate.
- **Class B**: Range: 128.0.0.0 to 191.255.255.255. Suitable for medium-sized networks.
- **Class C**: Range: 192.0.0.0 to 223.255.255.255. Commonly used in small networks.
- **Class D and E**: Class D (224.0.0.0 to 239.255.255.255) is used for multicast. Class E (240.0.0.0 to 255.255.255.255) is reserved for experimental purposes and not typically used in standard networking.

## 5.2 Public vs. Private IP Addresses
- **Public IPs**: Unique worldwide and used on the internet to ensure global connectivity.
- **Private IPs**: Used within private networks, they are not routed on the internet. Common ranges include 10.x.x.x, 172.16.x.x to 172.31.x.x, and 192.168.x.x.

## 5.3 Subnetting Basics
- **Why Subnet?**: Subnetting divides a network into smaller, manageable parts, improving performance and security while reducing congestion.
- **Subnet Masks**: A subnet mask is used to identify the network and host portions of an IP address. It helps determine which part of an address represents the network and which part represents the host.
- **Calculating Subnets**: Subnetting involves dividing a network into smaller networks by extending the network mask.

## 5.4 Classful vs. Classless Addressing
- **Classful Addressing**: Involves strict boundaries that can lead to inefficient IP space usage.
- **Classless Inter-Domain Routing (CIDR)**: CIDR allows for flexible subnetting by using a prefix and efficient IP space usage without adhering strictly to class boundaries.

## 5.5 Practical Subnetting Example
- **Example**: Subnetting a Class C network (e.g., 192.168.1.0) with a default subnet mask of 255.255.255.0. If you need to create 4 subnets, you would extend the subnet mask to 255.255.255.192 (/26), providing up to 62 hosts per subnet.
- **Tools for Subnetting**: Subnet calculators can assist in automating these calculations, ensuring accuracy and saving time.

## 5.6 Conclusion
- **Summary of the Chapter**: This chapter detailed the classification of IP addresses, introduced subnetting, and explained the efficiencies brought by CIDR.
- **What’s Next**: The subsequent sections or chapters could explore more advanced networking concepts, the implementation of these skills in real-world scenarios, or delve into network security.


