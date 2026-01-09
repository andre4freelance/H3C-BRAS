# H3C BRAS PPPoE
This repository provides configuration examples for an **H3C BRAS PPPoE environment** using GNS3.  
The scenario demonstrates a comprehensive setup where the **H3C vBRAS device acts as the PPPoE server**, with subinterfaces using VLAN tagging on an aggregated interface. These VLANs are forwarded to **SW-DIST**, which distributes them to client devices (MikroTik routers).

For NAT and routing, a **MikroTik RO-GATEWAY** device is utilized, directly connected to both the internet and the BRAS through an aggregated port. The NAT configuration ensures that PPPoE clients can access the internet seamlessly.

This setup demonstrates a practical understanding of **VLAN forwarding**, **aggregated interfaces**, **NAT**, and **routing**, creating a fully functional PPPoE-based network topology.

---

## Topology

![Project topology](images/1-topology.png)

---

## vBRAS PPPoE Session

The vBRAS successfully establishes PPPoE sessions with connected clients.

![vBRAS PPPoE Session](images/2-bras-pppoe-session.png)

---

## Client Internet Connectivity

PPPoE clients are able to access the internet without any issues through the RO-GATEWAY NAT.

![Client Internet Status](images/3-client-internet-status.png)

---

## RO-GATEWAY NAT & Routing

The RO-GATEWAY handles NAT and routing for PPPoE clients to access the internet.

![RO-GATEWAY NAT and Routing](images/4-ro-gateway-nat&routing.png)

---

## SW-DIST Interface & MAC Address

VLAN distribution and interface details on the SW-DIST switch.

![SW-DIST Interface and MAC](images/5-sw-dist-show-interface&mac.png)

---

## Devices

- **BRAS**: H3C vBRAS1000
- **SW-DIST**: ArubaOS-CX Virtual.10.07.0004
- **RO-GATEWAY**: MikroTik RouterOS 7.14.3
- **CLIENT**: MikroTik RouterOS 6.48.1

---

## Future Plans

I am open to collaboration, especially in implementing a **RADIUS server** for user management in the PPPoE environment. Feel free to reach out if you are interested in exploring this further.

---

## Links

Origin:  
<https://github.com/andre4freelance/H3C-BRAS>

LinkedIn post:  
<https://www.linkedin.com/posts/link-andre-bastian_pppoe-bras-vlan-activity-7277007112029790208-eYpM?utm_source=share&utm_medium=member_desktop&rcm=ACoAAD73JlUBty-p-mBfMEW0-O4j0sv-e_PRQvc>

Facebook post:  
<>
