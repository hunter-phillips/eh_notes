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
## Passive Recon
https://tryhackme.com/room/passiverecon

### Commands
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
