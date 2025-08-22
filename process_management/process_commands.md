# Show all running processes
ps aux

# Show processes for the current user
ps -u $(whoami)

# Display top processes (limited to top 10 for GitHub Actions visibility)
ps aux --sort=-%cpu | head -10

# Start a background process (sleep for 60 seconds)
sleep 60 &

# Display jobs running in the current shell
jobs

# Display process ID of sleep command
pgrep sleep

# Use 'top' command for system monitoring (limited to 5 seconds output)
top -b -n 1

# Show system load average
uptime

# Kill a background process (example: kill sleep)
pkill -f "sleep 60"

# Kill a process by PID (example)
# First, start a new process
sleep 100 &
# Then get its PID
PID=$(pgrep -f "sleep 100")
# Kill the process
kill $PID

# Display memory usage by processes
ps aux --sort=-%mem | head -10

# Check if a specific process is running (example: sleep)
pgrep sleep && echo "Sleep process is running" || echo "Sleep process not running"

# Show parent and child processes (hierarchical view)
pstree -p | head -20

# Display process start time
ps -eo pid,etime,cmd | head -10

# Show CPU and memory usage in % for each process
ps -eo pid,%cpu,%mem,cmd --sort=-%cpu | head -10
