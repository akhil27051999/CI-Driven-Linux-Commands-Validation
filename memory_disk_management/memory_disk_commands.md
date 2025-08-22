# Show total and free memory in human-readable format
free -h

# Show memory usage by processes
ps aux --sort=-%mem | head -n 10

# Show top memory-consuming processes dynamically
top -o %MEM -b -n 1 | head -n 20

# Display swap usage
swapon --show

# Display disk usage for all mounted file systems
df -h

# Display disk usage per directory in current path
du -sh *

# Display disk usage for all files and directories (recursive)
du -ah . | sort -rh | head -n 10

# Show inode usage (file/directory count usage)
df -i

# Show mounted file systems and types
mount | column -t

# Display disk partitions and sizes
lsblk

# Show detailed block device information
sudo fdisk -l

# Display disk I/O stats
iostat

# Display memory statistics
vmstat 1 5

# Check disk space usage with summary
sudo du -sh /home/*

# Display partition usage in tree format
sudo tree -L 2 / | head -n 50

# Check available and used RAM with details
cat /proc/meminfo | head -n 10

# Show memory usage per user
ps -eo user,pmem | sort -k2 -nr | head

# Check space occupied by each user in home directory
sudo du -sh /home/*

# List top 10 directories consuming space
sudo du -a / | sort -n -r | head -n 10

# Display information about disk cache
sudo dmidecode -t memory

# Check RAM slots and installed memory
sudo lshw -short -C memory

# Check filesystem disk space usage (human-readable)
sudo df -Th

# List mounted file systems in use
findmnt

# Display all UUIDs of partitions
blkid
