# pfSense-OpenVPN-CGNAT-CloudConnexa
Enable pfSense OpenVPN tunnel behind CGNAT using CloudConnexa

Difficulty: 5/10, if you know how to use OpenVPN in pfSense and general network theory.

If you are a pfSense user, who was using the built-in OpenVPN to remote log into your home network or alike, then suddenly no longer because you switched ISP, or your ISP went to CGNAT (Carrier-Grade Network Address Translation) infrastructure, then this guide may help you get the VPN going again.

I am by no means a network expert, just an IT admin who has done a fair amount of basic network setups, and had in the past 'attempted' CCNA. Thus this setup may contain flaws that I am not aware of. Use at your own discretion! 

The general approach is that we will need an external server that sits outside our home network, where going forward, will be the server that we will connect to, when we want to access our home network resources while away from home. This external server will act like a proxy/router that route traffic between our remote devices and our home router. 

This implmentation will use CloudConnexa to act as the external server, we will establish a site-to-site VPN between the home router and CloudConnexa. Then on our remote devices, add/update our OpenVPN connection profile to connect to CloudConnexa. And done!

CloudConnexa is a cloud based network service. Instead of creating a VPS in AWS/Azure/Other, and installing OpenVPN and performing varies complicated configurations, CloudConnexa provides a fairly easy to use network service that you can connect directly to, and manage all the setup in their dashboard. Thus no VPS to manage or complicated OS configurations.

As of 2023.04.09, CloudConnexa service is free, likely only for personal use, and for 3 or less active connections. 
