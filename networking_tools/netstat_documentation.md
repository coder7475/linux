
# Full Documentation on the Linux Tool: `netstat`

The `netstat` command is a versatile networking tool available in Linux and Unix-like operating systems. It provides various network-related information, such as network connections, routing tables, interface statistics, masquerade connections, and multicast memberships.

## Basic Syntax
```bash
netstat [OPTION]
```

## Commonly Used Options

- `-a` : Displays all sockets (listening and non-listening).
- `-t` : Shows TCP connections.
- `-u` : Shows UDP connections.
- `-n` : Shows numerical addresses instead of resolving hostnames.
- `-l` : Shows only listening sockets.
- `-p` : Displays the PID and name of the program to which each socket belongs.
- `-r` : Displays the kernel routing table.
- `-i` : Displays network interfaces.
- `-s` : Displays statistics for each protocol.
- `-c` : Continuously updates the output every second.

## Examples and Use Cases

1. **Show All Connections**
   ```bash
   netstat -a
   ```
   This command lists all active network connections, both TCP and UDP, including listening and non-listening ports.

2. **Display Only Listening Ports**
   ```bash
   netstat -l
   ```
   This command displays all ports that are currently in a listening state.

3. **Show Active TCP Connections**
   ```bash
   netstat -t
   ```
   Displays only active TCP connections.

4. **Show Active UDP Connections**
   ```bash
   netstat -u
   ```
   Displays only active UDP connections.

5. **Display Connections with Numerical Addresses**
   ```bash
   netstat -n
   ```
   This command prevents `netstat` from resolving hostnames and service names, displaying numerical addresses and ports instead. This can speed up the output and make it easier to read in some cases.

6. **Display Connections with Program Names**
   ```bash
   sudo netstat -p
   ```
   This command displays the PID and program names to which sockets belong. Note that this command requires superuser privileges, hence the `sudo`.

7. **Show Kernel Routing Table**
   ```bash
   netstat -r
   ```
   Displays the kernel routing table, similar to the `route -n` command. It shows the routes that the kernel will use for sending packets.

8. **Display Network Interfaces**
   ```bash
   netstat -i
   ```
   Shows a list of network interfaces along with their statistics.

9. **Display Statistics for Each Protocol**
   ```bash
   netstat -s
   ```
   Provides a statistical breakdown of each protocol (TCP, UDP, ICMP, etc.) including information such as packets received, packets sent, and errors.

10. **Continuous Network Status Updates**
    ```bash
    netstat -c
    ```
    Continuously displays the network status, updating every second.

## Combining Options

You can combine different options to refine the output to meet specific requirements. Here are some examples:

1. **List all listening TCP ports**
   ```bash
   netstat -lt
   ```
   This command shows only listening TCP ports.

2. **List all listening UDP ports**
   ```bash
   netstat -lu
   ```
   This command shows only listening UDP ports.

3. **Show all TCP and UDP ports in a numerical format, with program names**
   ```bash
   sudo netstat -tulnp
   ```
   This provides a comprehensive overview of all TCP and UDP connections with numerical addresses and the corresponding program names.

## Advanced Usage

1. **Show Detailed Interface Statistics**
   ```bash
   netstat -i -e
   ```
   The `-e` option shows extended information for interfaces, such as the number of packets transmitted and received, errors, and collisions.

2. **Display Multicast Group Memberships**
   ```bash
   netstat -g
   ```
   Shows the multicast group memberships for both IPv4 and IPv6.

3. **Display RAW Network Statistics**
   ```bash
   netstat -w
   ```
   Shows raw network statistics related to the RAW protocol.

## `netstat` vs. `ss`

In modern Linux distributions, `netstat` has been deprecated in favor of the `ss` command, which provides similar functionality but with more powerful features and better performance. The `ss` command can be used as a replacement for most of the `netstat` functionality. Here’s how you can use `ss` in place of `netstat`:

- Show all connections:
  ```bash
  ss -a
  ```

- Show listening ports:
  ```bash
  ss -l
  ```

- Show connections with program names:
  ```bash
  sudo ss -p
  ```

## Conclusion

The `netstat` command is a powerful tool for network diagnostics and analysis. Although it is deprecated in favor of `ss` in many distributions, it remains widely available and used for its simplicity and comprehensive output. For more detailed or high-performance requirements, consider using `ss` or other network analysis tools such as `nmap` or `tcpdump`.

Always ensure you have the necessary permissions (usually root) when working with network-related commands to access all available information.
