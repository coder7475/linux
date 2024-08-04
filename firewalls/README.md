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

Rules can also be added using a _numbered_ format.

See numbered format:

```bash
  sudo ufw status numbered
```

To add a rule using _numbered_ format:

```bash
  sudo ufw insert 1 allow 80 # Add allowing 80 port as number 1 rule
```

To remove a rule, use `delete` followed by the rule:

```bash
  sudo ufw delete deny 22 # delete the deny 22 rule
```

## Allow Access from specific hosts

### References

- https://ubuntu.com/server/docs/firewalls

- https://opensource.com/article/20/2/firewall-cheat-sheet?ref=dailydev
