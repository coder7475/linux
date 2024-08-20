# How To Send Processes Signals in Linux

Signals: OS way to tell program to terminate or modify

# List all signals

kill -l

# Command to Terminate a process

kill PID_of_target_process - Send TERM signal

kill -KILL PID - Send KILL signal

sudo kill -HUP pid_of_apache - Send HUP, or hang-up signal

killall firefox - Send TERM signal to all process of firefox

# Use regular Process names to terminate

pkill -9 ping ~= kill -9 `pgrep ping`

# Signals

TERM(15) - Tells process to please terminate, allow clean up operations and exit smootly

KILL(9) - Tells OS kernel to shut down the process

HUP - Tells apache webserver to reload the configuration

# Terminologies

Daemons - Process that are designed to run constantly in the background
