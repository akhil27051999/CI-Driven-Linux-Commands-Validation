# Display current network interfaces and IP addresses
ip a

# Display IP routing table
ip route

# Show default gateway
ip route | grep default

# Show DNS configuration
cat /etc/resolv.conf

# Show network interface statistics
ifconfig -a || ip -s link

# Ping a host to check connectivity (example: google.com)
ping -c 4 google.com

# Check TCP/UDP listening ports and open connections
ss -tuln

# Show active connections
ss -s

# Display all network sockets
netstat -tulnp || ss -tulnp

# Trace the route to a host
traceroute google.com

# Perform DNS lookup for a domain
nslookup google.com

# Alternative DNS query using dig (if installed)
dig google.com

# Check the hostname of the system
hostname

# Set hostname (temporary until reboot)
sudo hostname new-hostname

# Download a file using curl (example)
curl -O https://example.com/sample.txt

# Check network connectivity with wget (if installed)
wget https://example.com

# Test internet connection via curl
curl -Is https://google.com | head -n 1

# Show firewall rules (if ufw is used)
sudo ufw status

# Enable firewall (if ufw is used)
sudo ufw enable

# Allow HTTP and HTTPS ports (80 and 443)
sudo ufw allow 80
sudo ufw allow 443

# Deny incoming ping requests (ICMP)
sudo iptables -A INPUT -p icmp --icmp-type echo-request -j DROP

# List current iptables rules
sudo iptables -L -n -v
