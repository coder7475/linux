# command

 sudo useradd john

# result:
 
 1. new user: john 
 2. new group: john
 3. new directory: /home/john
 4. new user bash: /bin/bash 
 5. All files from /etc/skel copied to home directory 

# Find Default Jobs For terminal when creating new user

 useradd --defaults
 
 find explanation: cat /etc/login.defs

# Setup A Password doe john

sudo passwd john

# Delete a account

sudo userdel john

# Delete home directory with user

sudo userdel --remove john

# Use Different Shell
#
sudo useradd --shell /bin/othershell --home-dir /home/otherdirectory/ john

sudo useradd -s /bin/othershell -d /home/otherdirectory/ john

sudo useradd -s /bin/othershell john

# find data 
cat /etc/passwd

# Select an ccustom id when new user is created
sudo useradd --uid 1100 smith

# Home directory of users premissin
ls -l /home/
ls -ln /home = user per with uid






