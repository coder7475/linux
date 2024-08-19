## Why Change SSH Port?

**Port 22** is the standard designated port for SSH connections.For enhanced security, it's highly recommended to change the default SSH port to a different, less obvious one. This makes it harder for attackers to target your SSH connection.

Here's why changing it is a smart security practice:

- **Brute-Force Attacks**: Automated scripts and bots constantly scan the internet for open port 22, trying to crack passwords with repeated login attempts (brute-force attacks). An unusual port number significantly reduces this risk.

- **Reduced "Noise"**: A standard SSH port receives constant connection attempts, many of them unauthorized. This generates unnecessary logs and can mask real attack attempts.

- **Security Through Obscurity**: It's one layer of defense (not a replacement for strong passwords or firewalls!). Attackers are less likely to spend time probing random ports.

- **Improved Organization**: If you manage multiple servers, using different SSH ports can help to identify and manage them more easily.

**Note**: Consider selecting a port outside the well-known range **(0-1023)** and the registered ports range **(1024-49151)**. It’s advisable to opt for a custom port within the dynamic or private ports range **(49152-65535)**.

## How to change default ssh port in vps

1. Login to your

### References

1. https://www.youtube.com/watch?v=bFgPpJs4ndQ&list=PLbGui_ZYuhij0mM8xP2udM_EDvl8JNdtn&index=13

2. https://www.hostinger.com/tutorials/how-to-change-ssh-port-vps

3. https://www.hostinger.com/tutorials/how-to-change-ssh-port-vps

4. https://monovm.com/blog/default-ssh-port/#:~:text=There%20are%20over%2065%2C000%20possible,designated%20port%20for%20SSH%20connections
