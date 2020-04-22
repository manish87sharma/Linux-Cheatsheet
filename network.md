# NETWORKING

```bash

# Send ICMP echo request to host
> ping host

# Display whois information for domain
# yum install whois
> whois domain

# Display DNS information for domain
> dig domain

# Reverse lookup of IP_ADDRESS
> dig -x IP_ADDRESS

# Display DNS ip address for domain
> host domain

# Display the network address of the host name.
> hostname -i

# Display all local ip addresses
> hostname -I

# Download http://domain.com/file
> wget http://domain.com/file

# Display listening tcp and udp ports and corresponding programs
# p - program, l - listening, e - extend, n - numeric
> netstat -pluten

# lsof utility
> sudo lsof -iTCP -sTCP:LISTEN -P

# tracert utility
> tracert <host>

# curl command
# l - list , i -include header ,v - verbose, -o output, L - location
> curl -Lvil <host> -o /dev/null

# nslookup utility is used query Internet domain name servers
> nslookup <url>

```
