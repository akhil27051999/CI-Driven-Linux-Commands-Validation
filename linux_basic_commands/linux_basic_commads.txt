# Show current user
whoami

# Show current directory
pwd

# List files in the current directory
ls -l

# Create a new directory
mkdir test_directory

# Navigate into the new directory
cd test_directory

# Create a new file
touch testfile.txt

# Write some text into the file
echo "This is a test file created in GitHub Actions" > testfile.txt

# Display file content
cat testfile.txt

# Append more content to the file
echo "Another line added." >> testfile.txt

# Show file content again
cat testfile.txt

# Rename the file
mv testfile.txt renamed_file.txt

# Copy the file
cp renamed_file.txt copy_of_file.txt

# List all files again
ls -l

# Display disk usage of current directory
du -sh .

# Display free disk space
df -h

# Display current date and time
date

# Display calendar
cal

# Show system uptime
uptime

# Show hostname
hostname

# Show kernel version
uname -r

# Show system information
uname -a

# Display currently running processes
ps aux | head -10

# Sleep command for 2 seconds (simulate a wait)
sleep 2

# Remove copied file
rm copy_of_file.txt

# Go one level back
cd ..

# Remove the directory created
rm -r test_directory
