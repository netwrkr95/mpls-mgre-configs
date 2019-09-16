 MPLS VPN over mGRE leverages the flexibility that point-to-point MPLS VPN over IP solutions offers, , while simplifying management, configuration, control plane protocols, and overall network operations of any MPLS VPN solution over IP.   Because mGRE is a point-to-multipoint model, fully meshed GRE tunnels are not required to interconnect MPLS VPN PE devices.  Thus, MPLS VPN over mGRE solves the cumbersome configuration issue that exist when attempting to configure 100's of sites, requiring a full-mesh of connectivity and cumbersome, and eliminating the time-consuming process of configuring and maintaining point-to-point GRE tunnels, and the IGP and LDP needed to run over them. 
 
 While MPLS requires that all core routers support MPLS label forwarding, the MPLS VPN over mGRE feature overcomes this requirement (see RFC 4797) by still leveraging the standard control plane of MPLS VPN (RFC 4364), while eliminating the need that the data plane for forwarding support MPLS labels.   This allows the MPLS forwarding to use IP encapsulation (RFC 4023 with GRE In this case) between endpoints across any form of existing IP transport networks, including L3 VPN providers, internal IP networks, and public/private IP transports. 

When the MPLS VPN over mGRE features is enabled, it allows the operator to deploy a "self deployed" MPLS VPN service on the CE/CPE router connected via the SP service transport offering.  This allows one to provision the L3 VPN services without using Label-Switched Path (LSP), Carrier Supporting Carrier (CsC), or a Label Distribution Protocol (LDP). MPLS VPN over mGRE uses IPv4-based mGRE tunnels to encapsulate VPNv4/v6 labeled packets between CE devices, over the IP transport.  It should also be noted that because the mGRE solution has no established destination in it configuration, some form of “signaling” is required to discover the interested endpoints.  For the MPLS VPN over mGRE  solution, BGP builds this IP tunnel end-point database between each PE, thus allowing IP encapsulation between MP-BGP end-points

In addition, MPLS VPN over mGRE also allows both IP transport and legacy MPLS forwarding to coexist In the same PE.  The ingress PE router determines which encapsulation technology to use when a packet is sent to the remote PE router, based on which PE signaled it via MP-BGP.  This feature is extremely powerful, as It offers a smooth transition from MPLS VPNs over an MPLS core as well as using IP encapsulation.

It is obvious the MPLS VPN over mGRE solution offers clear advantages for network designers wanting to leverage MPLS VPNs over an IP transport, specifically when a fully meshed traffic pattern is required between PE's.  MPLS VPN over mGRE drastically eliminates the amount of configurations required on each PE device, and simplifies the ability to support MPLS VPNs over IP.

More details can be found at Cisco's link: http://www.cisco.com/c/en/us/td/docs/ios-xml/ios/interface/configuration/xe-3s/ir-xe-3s-book/ir-mpls-vpnomgre-xe.html

The content here will provide working configuration examples in a rather basic topology.

Basic Topology:

![alt text](https://github.com/netwrkr95/mpls-mgre-configs/blob/master/mGRE-Domain.png "Test Topology for configuration files")




