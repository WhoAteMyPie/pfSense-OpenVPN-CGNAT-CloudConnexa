Enable pfSense OpenVPN tunnel behind CGNAT using CloudConnexa

Difficulty: 5/10, if you know how to use OpenVPN in pfSense and general network theory.

What will this do?

Allow pfSense users, who are behind CGNAT (Carrier Grade Network Address Translation), to OpenVPN into their network.

What will I need?

pfSense Router
pfSense CloudConnexa cloud service account

As of 2023.04.09, CloudConnexa service is free, for 3 or less active connections, please read their T&Cs for more details.

Overview

The aim is to create a virtual network in CloudConnexa, configure a site-to-site OpenVPN connection between our pfSense router, behind the CGNAT, and the virtual network in CloudConnexa. Config CloudConnexa to route our required network traffic to the pfSense router, then...success! Once CloudConnexa is configured, a url will be provided. This url will replace the static ip address that we normally use to VPN into our network.
