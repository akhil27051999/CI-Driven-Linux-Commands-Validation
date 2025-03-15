# View system log (most common syslog file)
sudo cat /var/log/syslog || echo "/var/log/syslog not found"

# View authentication logs
sudo cat /var/log/auth.log || echo "/var/log/auth.log not found"

# View kernel log
sudo dmesg | tail -n 50

# View last 50 lines of system log
sudo tail -n 50 /var/log/syslog || echo "/var/log/syslog not found"

# View login attempts and sessions
lastlog

# View failed login attempts
sudo cat /var/log/faillog || echo "/var/log/faillog not found"

# View cron job logs
sudo cat /var/log/cron.log || echo "/var/log/cron.log not found"

# Show recent journal logs
sudo journalctl -n 50

# Show boot logs (fallback if boot.log not present)
sudo journalctl -b || echo "boot journal not found"

# Show logs for a specific service (example: sshd)
sudo journalctl -u ssh || echo "No ssh logs available"

# Show logs for previous boot
sudo journalctl -b -1 || echo "No previous boot logs"

# Filter logs by time (last 1 hour)
sudo journalctl --since "1 hour ago"

# View system logs with priority level (e.g., error)
sudo journalctl -p err -n 20

# Show disk usage of /var/log directory
sudo du -sh /var/log

# List all log files in /var/log
ls -lh /var/log

# Compress old logs to save space
sudo gzip /var/log/syslog.1 || echo "No old syslog to compress"

# Remove old compressed logs (example cleanup)
sudo find /var/log -name "*.gz" -type f -mtime +30 -exec rm -f {} \;

# Monitor syslog in real time
sudo tail -f /var/log/syslog || echo "/var/log/syslog not found"

# Monitor journal logs in real time
sudo journalctl -f

# Export all journal logs to a file
sudo journalctl > journal_backup.log
