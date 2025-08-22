# Update package index
sudo apt-get update

# Upgrade all installed packages
sudo apt-get upgrade -y

# Install a specific package (example: curl)
sudo apt-get install -y curl

# Install multiple packages at once (example: git, htop, vim)
sudo apt-get install -y git htop vim

# Reinstall a package (example: curl)
sudo apt-get install --reinstall -y curl

# Remove a package (example: htop)
sudo apt-get remove -y htop

# Completely remove a package with config files (example: vim)
sudo apt-get purge -y vim

# Clean up retrieved package files
sudo apt-get clean

# Remove unused dependencies
sudo apt-get autoremove -y

# Show installed version of a package (example: git)
dpkg -l | grep git

# Show package information (example: curl)
apt-cache show curl

# Search for a package
apt-cache search apache

# Check package dependencies (example: curl)
apt-cache depends curl

# Check reverse dependencies (what depends on a package)
apt-cache rdepends curl

# List all installed packages
dpkg -l | less

# List files installed by a package (example: curl)
dpkg -L curl

# Verify package installation status
dpkg -s curl
