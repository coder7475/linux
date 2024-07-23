sudo useradd john   # Create a user
sudo groupadd developers # create a group

# add john to developers
sudo gpasswd --add john developers
OR
sudo gpasswd -a john developers
# find johns groups
groups john

# remove from group

sudo gpasswd --delete john developers
OR
sudo gpasswd -d john developers

# Change users primary group
sudo usermod -g developers john
OR
sudo usermod --gid developers john

# Rename a group from developers to programmers
sudo groupmod --new-name programmers developers
OR
sudo groupmod -n programmers developers

# Delete a group
sudo groupdel programmers

