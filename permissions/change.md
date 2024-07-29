# change group
chgrp group_name file/directory

# change owner
sudo chown new_user file_name

# change owner and group
sudo chown new_user:group_name file_name

# change mode - modify permissions
chmod permissions file/directory

# write permisiion for user/owner
chmod u+w file

# remove permissions
chmod u-w file

# exact permission - only write permission
chmod u=w file

# basic syntax: 
add permission: (u/g/o)(+/-/=)(rwx/rw/wx/r/w/x)

# remove all permissions
chmod g= file
chmod g-rwx file

# chaining permissions
chmod u+rw,g=r,o= file

# octal permissions
640 = ugo
4 = r
w = 2
x = 1
- = 0

ex:
rw-|r--|---
420|400|000
640
