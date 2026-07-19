# Day 25 of Cisco Linux Essentials Course

Today in the Linux Essentials course, I understood a few more important topics.

## Email Servers
Email relies on 3 main tasks:

**MTA (Mail Transfer Agent):** The MTA is the software that picks up your email from one system and delivers it to another — like a courier taking a letter from one city's post office to another.

**Mail Delivery Agent (MDA):** Also known as local delivery — once the email reaches its destination MTA, the MDA delivers it to the recipient's specific mailbox.

**POP/IMAP Server:** POP and IMAP are two protocols that let your computer or mobile device connect to email servers to fetch and display emails.

**Dovecot & Cyrus IMAP:** Dovecot is a popular POP/IMAP server due to its ease of use and low maintenance. Cyrus IMAP is another option.

**Open Source vs Closed Source:** Microsoft Exchange ships as a complete closed package. In the open source world, Linux offers full customization according to your needs.

## File Sharing & Network Infrastructure

**Samba:** Lets Linux behave like a Windows machine on the network, enabling seamless file sharing with Windows systems.

**Netatalk:** Allows a Linux server to behave like an Apple Mac server for file sharing with Mac systems.

**NFS (Network File System):** The native file system for Unix/Linux — lets a remote system's file system be mounted directly, just like a local disk.

**DNS (Domain Name System):** The oldest directory system on a network, converting IP addresses into human-readable names, and keeping records like email server addresses.

**LDAP (Lightweight Directory Access Protocol):** A central directory system for storing user accounts, usernames, and passwords, stored in a tree structure.

**OpenLDAP:** The most commonly used LDAP implementation in Linux infrastructure.

**DHCP (Dynamic Host Configuration Protocol):** Handles IP address requests from computers, assigning a free IP from the address pool whenever a device connects to a network.

**ISC DHCP**, maintained by the Internet Systems Consortium, is the most widely-used open source DHCP server in the world.

#Linux #DevOps #CiscoNetworkingAcademy #LearningInPublic #NetworkInfrastructure
