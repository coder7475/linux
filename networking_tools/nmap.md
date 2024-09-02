# NMAP

`nmap` - Network exploration tool and security/port scanner

## Syntax

```bash
nmap [<Scan Type>...] [ <Options> ] { <target Specification> }
```

## Description

- Nmap ("Network Mapper") is an open-source tool for network exploration and security auditing.
- Designed to scan large networks quickly but also works on single hosts.
- Uses raw IP packets to:
  - Identify available hosts on a network.
  - Discover services (application names and versions) running on hosts.
  - Detect operating systems and their versions.
  - Identify packet filters or firewalls.
- Commonly used for security audits and routine tasks like:
  - Network inventory.
  - Managing service upgrade schedules.
  - Monitoring host or service uptime.
- Output includes a list of scanned targets with detailed information.
- Key output component is the "interesting ports table," which shows:
  - Port number and protocol.
  - Service name.
  - Port state (open, filtered, closed, or unfiltered).
- Can also provide additional details, such as:
  - Reverse DNS names.
  - Operating system guesses.
  - Device types.
  - MAC addresses.

## Examples

A representative Nmap scan:

```bash
nmap -A -T4 scanme.nmap.org
```

Here, the flags:
`-A`: flag is to enable OS and version detection, script running and traceroute
`-T4`: Fater Execution

Output for this command:

```bash
Starting Nmap 7.80 ( https://nmap.org ) at 2024-09-02 12:18 +06
Nmap scan report for scanme.nmap.org (45.33.32.156)
Host is up (0.23s latency).
Other addresses for scanme.nmap.org (not scanned): 199.19.57.1 199.249.120.1 199.19.56.1 199.19.54.1 199.249.112.1 199.19.53.1 199.19.57.1 199.249.120.1 199.19.56.1 199.19.54.1 199.249.112.1 199.19.53.1 2001:500:f::1 2001:500:48::1 2001:500:e::1 2001:500:c::1 2001:500:40::1 2001:500:b::1 2600:3c01::f03c:91ff:fe18:bb2f 2001:500:f::1 2001:500:48::1 2001:500:e::1 2001:500:c::1 2001:500:40::1 2001:500:b::1
Not shown: 972 closed ports
PORT      STATE    SERVICE        VERSION
22/tcp    open     ssh            OpenSSH 6.6.1p1 Ubuntu 2ubuntu2.13 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey:
|   1024 ac:00:a0:1a:82:ff:cc:55:99:dc:67:2b:34:97:6b:75 (DSA)
|   2048 20:3d:2d:44:62:2a:b0:5a:9d:b5:b3:05:14:c2:a6:b2 (RSA)
|   256 96:02:bb:5e:57:54:1c:4e:45:2f:56:4c:4a:24:b2:57 (ECDSA)
|_  256 33:fa:91:0f:e0:e1:7b:1f:6d:05:a2:b0:f1:54:41:56 (ED25519)
80/tcp    open     http           Apache httpd 2.4.7 ((Ubuntu))
|_http-server-header: Apache/2.4.7 (Ubuntu)
|_http-title: Go ahead and ScanMe!
135/tcp   filtered msrpc
139/tcp   filtered netbios-ssn
445/tcp   filtered microsoft-ds
593/tcp   filtered http-rpc-epmap
1024/tcp  filtered kdm
1025/tcp  filtered NFS-or-IIS
1026/tcp  filtered LSA-or-nterm
1027/tcp  filtered IIS
1028/tcp  filtered unknown
1029/tcp  filtered ms-lsa
1030/tcp  filtered iad1
1080/tcp  filtered socks
1433/tcp  filtered ms-sql-s
1434/tcp  filtered ms-sql-m
1719/tcp  filtered h323gatestat
1720/tcp  filtered h323q931
1721/tcp  filtered caicci
2001/tcp  filtered dc
3128/tcp  filtered squid-http
4444/tcp  filtered krb524
5060/tcp  filtered sip
5061/tcp  filtered sip-tls
9929/tcp  open     nping-echo     Nping echo
12345/tcp filtered netbus
31337/tcp open     tcpwrapped
49152/tcp filtered unknown
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 48.75 seconds
```
