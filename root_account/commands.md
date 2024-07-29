# Run Command as root
sudo ls /root/

# Login as a root
sudo --login
or sudo -i

# Exit
logout

# Login with password
su - / su -l / su --login

# Choose new password
sudo passwd root

# Change existing password
sudo passwd --unlock root 
      OR
sudo passwd -u root

# Lock root account with password
sudo passwd --lock root
     OR
sudo passwd -l root
