
     ENTERPRISE ACTIVE DIRECTORY – SINGLE DOMAIN MULTI-SITE ARCHITECTURE

[ PROJECT OVERVIEW ]
A complete enterprise-grade Active Directory infrastructure designed from 
 Features a single domain across multiple sites with full redundancy, 
routing, and service integration, reflecting real-world production architecture.

[ CORE FEATURES ]
* Multi-site AD replication (Building-A ↔ Building-B).
* AD-Integrated DNS with forest-wide replication.
* DHCP failover (Load Balance mode) across three subnets.
* pfSense-based routing and gateway segmentation.
* High availability via Additional Domain Controller (ADC).

[ INFRASTRUCTURE SUMMARY ]
* Subnets         : 192.168.1.0/24 (B-A), 192.168.2.0/24 (B-A), 192.168.3.0/24 (B-B)
* Domain Cont.    : DC-SRV01 (192.168.1.210), ADC-SRV01 (192.168.3.210)
* DHCP Servers    : DHCP-SRV01 (192.168.1.215), DHCP-SRV02 (192.168.1.220)
* pfSense Gateway : 192.168.1.1, 192.168.2.1, 192.168.3.1

[ VALIDATION WORKFLOW ]
* Replication Health: repadmin /showrepl
* DNS Verification  : nslookup
* DHCP Verification : Get-DhcpServerv4Lease
* Connectivity      : Inter-site gateway testing & domain join validation.

[ REPOSITORY STRUCTURE ]
* /docs    : Architecture, IP plans, and runbooks.
* /configs : DHCP scope, DNS zone, and pfSense XML.
* /scripts : PowerShell automation scripts.
* /notes   : Troubleshooting and validation checklists.
* /diagrams: enterprise-ad-multi-site-architecture.png

[ DESIGN PHILOSOPHY ]
* First-principles architecture; zero templates used. 
* Self-designed network layout tailored for enterprise-grade redundancy.

System Environment: Windows Server & pfSense | Architecture: Self-Designed
