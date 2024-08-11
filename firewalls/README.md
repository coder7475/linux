# Firewalls

- All modern Linux firewall solution uses **Netfilter** subsystem.

- **Netfilter** is a packet filtering system that is used to
  manipulate the fate of network traffic headed into or through the server.

- _System administrator_ use userspace interface utility _siptables_ to set rules for how to manage the incoming traffic.

- _iptables_ is extremely effective and customizable, but it can be complex to configure.

- Developers produced several frontend to help user control their firewall without writing lengthy _iptables_ rules. Ex: ufw, firewalld etc

## ufw - Uncomplicated Firewall

- The default for debian based distros, ex: ubuntu, linux mint etc.

- Provides a user-friendly way to create IPv4 or IPv6 host-based firewall.

- `ufw` by default is initially disabled.

### Check the status

To see the firewall status, enter:

```bash
  sudo ufw status
```

And for more information, enter:

```bash
  sudo ufw status verbose
```

See numbered format:

```bash
  sudo ufw status numbered
```

Show all added rules:

```bash
ufw show added
```

### Enable or disable ufw

To enable `ufw`, run:

```bash
  sudo ufw enable
```

To disable `ufw`, run:

```bash
  sudo ufw disable
```

### Open or close a port

To open a port (port no: 22):

```bash
  sudo ufw allow 22
```

To close an opened port:

```bash
  sudo ufw deny 22
```

### Add or remove a rule

Add Rule For Services. To allow ssh connection

```bash
  ufw allow ssh
```

Some important rules to allow:

```bash
  ufw allow http
  ufw allow https
```

Rules can also be added using a _numbered_ format.

- See numbered format:

```bash
  sudo ufw status numbered
```

- To add a rule using _numbered_ format:

```bash
  sudo ufw insert 1 allow 80
```

This allowing 80 port as number 1 rule

- To remove a rule, use `delete` followed by the rule:

```bash
  sudo ufw delete deny 22
```

This delete the deny 22 rule

## Allow Access from specific hosts

- It can allow access from specific hosts or networks to a port

- Example: Allows SSH access from host `192.168.0.2` to any IP address on this host:

```bash
 sudo ufw allow proto tcp from 192.168.0.2 to any port 22
```

- To allow SSH access from entire subnet enter:

```bash
 sudo ufw allow proto tcp from 192.168.0.2/24 to any port 22
```

### Simulate Adding Rules

If you want to see what happens when you add a rule use `--dry-run` option to a `ufw` command.

```bash
  sudo ufw --dry-run allow http
```

### Configure to support IPv6

1. Open Config File: using nano(a text editor)

```bash
  sudo nano /etc/default/ufw
```

2. Then Change The IPV6 value to yes:

```bash
 IPV6=yes
```

### To check all open ports that are running

1. Install `net-tools` if not already installed

```bash
  sudo apt install net-tools
```

2. Show all open port that are currently running:

```bash
  netstat -tulpn
```

### ufw application integration

### Reset all rules of ufw

```bash
  ufw reset
```

### Special Tips For Newbies

- After enabling firewall **never** exit from your remote server connection without `enabling` rule for `ssh` connection. Otherwise you won't be able to log into your own server.

### References

- https://ubuntu.com/server/docs/firewalls

- https://opensource.com/article/20/2/firewall-cheat-sheet?ref=dailydev

- https://github.com/coder7475/GeekyShowsNotes/blob/main/ufw_firewall_setup.md

- https://www.digitalocean.com/community/tutorials/ufw-essentials-common-firewall-rules-and-commands

- https://betterprogramming.pub/understanding-ufw-8d70d5d8f9d2
