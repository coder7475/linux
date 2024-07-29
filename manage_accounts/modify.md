# Change Home directory

 sudo usermod -d /home/otherdirectory -m john
 

# change user name from john to jane

 sudo usermod --login jane john
 sudo usermod -l jane john 

# Change user shell

 sudo usermod --shell /bin/othershell jane
 sudo usermod -s /bin/othershell jane

# Diable account
sudo usermod --lock jane
sudo usermod -L jane

# Eenable 

sudo usermod --unlock jane
sudo usermod -U jane

# Time Limit account

sudo usermod --expiredate 2024-12-10 jane
sudo usermod -e 2024-12-10 jane

# Remove expiration daate

sudo usermod -e "" jane

# Password change
#
chage = change age

# Password expiration
sudo chage --lastday 0 jane

sudo chage -d 0 jane

# Undo expiration
sudo chage -d -1 jane

# MAX DAYS
sudo chage --maxdays 30 jane

sudo chage -M 30 jane


# Find list of pass

sudo change --list jane

sudo change -l jane





