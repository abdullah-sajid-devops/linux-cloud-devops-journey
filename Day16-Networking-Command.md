# Day 16: Linux Networking Commands Mastery 🌐🐧

Welcome to Day 16 of my Linux System Administration & DevOps journey. Today's focus was entirely on understanding how Linux interacts with networks, resolves DNS, diagnoses latency, secures traffic, and handles file transfers over interfaces.

---

## 🗺️ 1. Infrastructure, Identity & Discovery

### `ip` / `ifconfig` (Interface Configuration)
Used to examine network interfaces, assign IP addresses, and manage routing paths.
```bash
# Modern approach to list interfaces and IP addresses
ip addr show

# Legacy approach (requires net-tools)
ifconfig
hostname / hostnamectl / hostid
Manages and views the unique network name and identifier of the system.

Bash
# View or change the system's hostname
hostnamectl status
sudo hostnamectl set-hostname devops-node-01
host / nslookup (DNS Query Utilities)
Performs forward and reverse DNS lookups to resolve domain names to IP addresses.

Bash
host google.com
nslookup github.com
arp (Address Resolution Protocol)
Displays and manipulates the IPv4 neighbor cache (maps local IPs to physical MAC addresses).

Bash
arp -a
🛠️ 2. Connectivity, Diagnostics & Socket Analytics
ping (Packet Internet Groper)
Sends ICMP ECHO_REQUEST packets to network hosts to check end-to-end reachability.

Bash
ping -c 4 google.com
nc or netcat (The Networking Swiss Army Knife)
Arguably the most powerful utility for raw port scanning, connection spawning, and network debugging.

Bash
# Check if a remote web server is listening on port 80 safely
nc -zv 192.168.1.50 80
route / traceroute / tracepath
Tracks how network packets travel. route reveals the routing table, while traceroute maps out every intermediary gateway hop.

Bash
# Show routing table configuration
ip route   # (Alternative to legacy 'route')

# Trace network paths hop-by-hop
traceroute google.com
netstat / nmcli
netstat inspects active network connections, sockets, and interface statistics, while nmcli manages NetworkManager configurations directly from the terminal.

Bash
# View all active listening TCP/UDP ports with process IDs
sudo netstat -tunlp
🔒 3. Security, Performance Monitoring & Transfers
iptables / iptables-save
The native netfilter framework for configuring custom firewall rulesets, packet inspection, and port forwarding.

Bash
# View active firewall rules with line numbers
sudo iptables -L -n -v --line-numbers
iftop / vnstat
Real-time interface traffic monitors. iftop monitors active network bandwidth utilization per host pair, while vnstat provides historical traffic logs.

Bash
sudo iftop -i eth0
curl / wget
Command-line utilities used to transfer data from or to a server using supported protocols (HTTP, HTTPS, FTP, etc.).

Bash
# Download a remote binary programmatically
wget [https://example.com/tool.tar.gz](https://example.com/tool.tar.gz)

# Hit an API endpoint and inspect response headers
curl -I [https://api.github.com](https://api.github.com)
ssh / scp / rsync
Secure infrastructure channels. ssh provides secure shell terminal access, scp handles secure file copies, and rsync synchronizes large directory trees with delta compression over network sockets.

Bash
# Sync local logs folder securely to a backup server
rsync -avz -e ssh ./logs/ user@remote_host:/var/backup/logs/
ipcs / ipcrm
Used to check and remove System V Inter-Process Communication (IPC) facilities like shared memory segments or message queues over network-aware clusters.

💡 Key Takeaway: Legacy utilities (like ifconfig, route, and netstat) are still highly relevant to know, but modern cloud environments favor the modular iproute2 suite (ip, ss).
