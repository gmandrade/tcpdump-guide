# tcpdump guide

## What is?
A network analysis tool

## Why tcpdump?
You can measure all TCP/IP communication details, explore some vulnerabilities, get network performance, watch possibilities of hacker attacks and a few more things. 

## Documentation

`$ man tcpdump`

http://www.tcpdump.org/manpages/tcpdump.1.html

https://linux.die.net/man/8/tcpdump

## Basic usage

Get all traffic:

`$ tcpdump`

Get all UDP traffic:

`$ tcpdump udp`

Get all TCP traffic:

`$ tcpdump tcp`

Get all ICMP traffic:

`$ tcpdump 'icmp or icmp6'`

Get all traffic for a especif host:

`$ tcpdump host google.com`

Get all ICMP traffic for a especif host:

`$ tcpdump host google.com and 'icmp or icmp6'`

## **TIPS** 
Try to use `-n` for not resolve the name of host. Help at velocity. 

`$ tcpdump -n host google.com and 'icmp or icmp6'`

Prefer to use a especific network interface.

`$ tcpdump -i eth0 -n host google.com and 'icmp or icmp6'`

Prefer to use verbose mode.

`$ tcpdump -v -i eth0 -n host google.com and 'icmp or icmp6'`

or

`$ tcpdump -vv -i eth0 -n host google.com and 'icmp or icmp6'`

or

`$ tcpdump -vvv -i eth0 -n host google.com and 'icmp or icmp6'`

# TODO

## Basic analysis
## Advanced usage
## Advanced analysis
## Integrate tools for help analysis