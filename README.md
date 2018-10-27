# tcpdump guide

## What is?
A network analysis tool

## Why tcpdump?
You can measure all TCP/IP communication details, explore some vulnerabilities, get network performance, watch possibilities of hacker attacks and a few more things. 

## Documentation

In bash:
`$ man tcpdump`

Man pages:

http://www.tcpdump.org/manpages/tcpdump.1.html

https://linux.die.net/man/8/tcpdump

## Useful links

ipv4 vs ipv6:

https://www.ibm.com/support/knowledgecenter/en/ssw_ibm_i_72/rzai2/rzai2compipv4ipv6.htm

tcpdump Cheat Sheet:

http://packetlife.net/media/library/12/tcpdump.pdf

Sans Institute - TCP/IP to ipv4

https://www.sans.org/security-resources/tcpip.pdf

Sans Institute - TCP/IP to ipv6

https://www.sans.org/security-resources/ipv6_tcpip_pocketguide.pdf

tcpdump filters:

http://alumni.cs.ucr.edu/~marios/ethereal-tcpdump.pdf

## Usage

Get all traffic:

`$ tcpdump`

Get all UDP traffic:

`$ tcpdump udp`

Get all TCP traffic:

`$ tcpdump tcp`

Get all traffic in a specific port:

`$ tcpdump port 80`

Get all ICMP traffic:

`$ tcpdump 'icmp or icmp6'`

Get all traffic for a specific host:

`$ tcpdump host google.com`

Get all ICMP traffic for a specific host:

`$ tcpdump host google.com and 'icmp or icmp6'`

Get all TCP traffic for a specific host in a specific port:

`$ tcpdump host google.com and tcp and port 80`

Get all UDP traffic for a range of IPs:

`$ tcpdump net 192.168.1.0/24 and udp`

Get all ICMP traffic for a two range of IPs:

`$ tcpdump net 192.168.1.0/24 or net 10.138.0.0/20 and 'icmp or icmp6'`

### **TIPS** 
Try to use `-n` for not resolve the name of host. Help at velocity. 

`$ tcpdump -n host google.com and 'icmp or icmp6'`

Prefer to use a specific network interface, `-i network-interface`.

`$ tcpdump -i eth0 -n host google.com and 'icmp or icmp6'`

Prefer to use verbose mode.

`$ tcpdump -v -i eth0 -n host google.com and 'icmp or icmp6'`

or

`$ tcpdump -vv -i eth0 -n host google.com and 'icmp or icmp6'`

or

`$ tcpdump -vvv -i eth0 -n host google.com and 'icmp or icmp6'`


# TODO

## Analysis

## Integrate tools for help analysis