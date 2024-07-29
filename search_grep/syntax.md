
# General Syntax for grep search

grep [options] `search_pattern` file_name

options: 
-i = case insensitive
-r = recurcive - specify a directory
-ir = can use it
-v = invert match - doest not contain search pattern
-w = only words
-o = only matching options
 
ex: grep 'CentOS' /etc/os-release
ex: sudo grep -ir 'centos' /etc/

