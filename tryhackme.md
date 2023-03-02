# TryHackMe
## Setting Up the VPN
* Download the configuration file on https://tryhackme.com/access
* Open the file and change `cipher AES-256-CBC` to `data-ciphers AES-256-CBC`
* Start the VPN with `sudo openvpn [file].ovpn`
* Check `ip a` for `tun0`
* Leave the terminal open while utilizing the website

# Penetration Testing Fundamentals
* https://tryhackme.com/room/pentestingfundamentals

# Network Security
## Passive Reconnaissance
* Passive reconnaissance lets you gather information about your target without any kind of direct engagement or connection. You are watching from afar or checking publicly available information.
* https://tryhackme.com/room/passiverecon

### Commands and Websites
* `whois [domain_name]` | request and response protocol that lists on TCP port 43 for incoming requests, provides:
  * registrar
  * contact information of registrant
  * creation, update, and expiration dates
  * name server
  * example
    * `whois mercyhurst.edu`
* `nslookup [-type=options] [domain] [server]` | name server look up
  * options contain the query type
    * `a` | IPv4
    * `aaaa` | IPv6
    * `cname` | canonical name
    * `mx` | mail servers
    * `soa` | start of authority
    * `txt` | TXT records
  * server is the DNS server to query
    * Cloudfare offers 1.1.1.1 and 1.0.0.1
    * Google offers 8.8.8.8 and 8.8.4.4
    * Quad9 offers 9.9.9.9 and 149.112.112.112
  * example
    * `nslookup -type=a tryhackme.com 1.1.1.1`
* `dig [@server] [domain] [type]` | more advanced DNS queries and additional functionality (Domain Information Groper (DIG))
  * Uses the same options as above
  * example:
    * `dig @1.1.1.1 tryhackme.com MX`
* [DNSDumpster](https://dnsdumpster.com/) offers detailed answers to DNS queries about different subdomains that can reveal much information about the target.
* [Shodan.io](https://www.shodan.io/) tries to connect to every device reachable online to build a search engine of connected "things" in contrast with a search engine for web pages.

## Active Reconnaissance 
* Active reconnaissance requires you to make some kind of contact with your target. This contact can be a phone call or a visit to the target company under some pretence to gather more information, usually as part of social engineering. Alternatively, it can be a direct connection to the target system, whether visiting their website or checking if their firewall has an SSH port open. Think of it like you are closely inspecting windows and door locks. Hence, it is essential to remember not to engage in active reconnaissance work before getting signed legal authorization from the client.
* https://tryhackme.com/room/activerecon

### Commands
* `ping [ip address]` | checks whether a remote system can be reached and whether it can reach you back.
 * `-c [num of pings]`
 * `-s [size of packet]`
* `traceroute [ip address]` | traces the route taken by the packets from one system to another
 * reveals the number of routers between your system and the target host
* `telnet [ip address] [port]` | used to connect with a remote system
* `nc [ip address] [port]` | netcat can function as a client that connects to a listening port, or it can act as a server that listens on a port
 * `-l` | listen mode
 * `-p` | port number
 * `-n` | numeric only
 * `-v` | verbose output
 * `-vv` | very verbose
 * `-k` | keep listening after client disconnects
* `nc -lvnp [port]` | use netcat as a server

# Nmap Live Host Discovery
Nmap is an industry-standard tool for mapping networks, identifying live hosts, and discovering running services. Nmap’s scripting engine can further extend its functionality, from fingerprinting services to exploiting vulnerabilities. A Nmap scan usually goes through the steps shown in the figure below, although many are optional and depend on the command-line arguments you provide.

![image](https://user-images.githubusercontent.com/82356945/222522651-6357f141-cb55-42a9-b08c-b77bcf411e9b.png)
## Enumerating Targets
* `nmap -sL -n [targets]` | provides a detailed list of the hosts that namp will scan without scanning them
 * `targets` can be a list (`domain.com scanme.nmap.org example.com`), range (`10.11.12.15-20`), subnet (`MACHINE_UP/30`), or use a file (`nmap -iL list_of_hosts.txt`)

## Discovering Live Hosts
![image](https://user-images.githubusercontent.com/82356945/222522704-c2ab6a64-f598-434e-95e0-ae18204a43ab.png)

## ARP Scans
![image](https://user-images.githubusercontent.com/82356945/222522284-6aae6339-2717-429d-99fa-8e3bbe27b9b8.png)
* ARP scans are only possible if you are on the same subnet as the target systems.
 * `nmap -PR -sn [machine_ip/24]` can be used to discover all the live systems on the same subnet as the target machine.

# Vulnerability Research (Vuln 101)

# Penetration Testing Tools (CompTIA Pentest+ - all)
