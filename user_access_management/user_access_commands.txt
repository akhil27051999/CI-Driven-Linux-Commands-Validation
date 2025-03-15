# Check current logged-in user
whoami

# Display current user ID and group ID
id

# Show all users on the system
cut -d: -f1 /etc/passwd

# Show all groups on the system
cut -d: -f1 /etc/group

# Create a new group 'devops' (if not already exists)
getent group devops || sudo groupadd devops

# Create a new user 'akhil' and assign to devops group (if not exists)
id -u akhil &>/dev/null || sudo useradd -g devops akhil

# Create another user 'atchyuth' and assign to devops group (if not exists)
id -u atchyuth &>/dev/null || sudo useradd -g devops atchyuth

# Set password for user 'akhil' (non-interactive)
echo "akhil:MySecurePass123" | sudo chpasswd

# Set password for user 'atchyuth' (non-interactive)
echo "atchyuth:MySecurePass456" | sudo chpasswd

# Add user 'akhil' to group 'devops'
sudo usermod -aG devops akhil

# Add user 'atchyuth' to group 'devops'
sudo usermod -aG devops atchyuth

# Display groups that user 'akhil' belongs to
groups akhil

# Display groups that user 'atchyuth' belongs to
groups atchyuth

# Show all users in group 'devops'
getent group devops

# Change user's primary group to 'devops'
sudo usermod -g devops akhil

# Rename a user (rename akhil to akhildev)
id -u akhildev &>/dev/null || sudo usermod -l akhildev akhil

# Rename a group (rename devops to devsecops)
getent group devsecops || sudo groupmod -n devsecops devops

# Lock user 'atchyuth' account
sudo usermod -L atchyuth

# Unlock user 'atchyuth' account
sudo usermod -U atchyuth

# Expire user password to force change on next login
sudo chage -d 0 akhildev

# Set account expiration date for user
sudo chage -E 2025-12-31 akhildev

# View password aging information for user
sudo chage -l akhildev

# Delete user 'atchyuth' (if exists)
id -u atchyuth &>/dev/null && sudo userdel -r atchyuth

# Change primary group of 'akhildev' to another group before deleting devsecops
sudo usermod -g users akhildev

# Delete group 'devsecops' (if exists)
getent group devsecops && sudo groupdel devsecops

# Add user to sudoers file
echo "akhildev ALL=(ALL) NOPASSWD:ALL" | sudo tee /etc/sudoers.d/akhildev

# View sudo permissions for a user
sudo -l -U akhildev
