# Update and upgrade Termux packages
pkg update -y && pkg upgrade 

# Install Go
pkg install golang -y

# Add the path of the Go binaries to the PATH
echo 'export PATH="$PATH:$HOME/go/bin"' >> ~/.bashrc

# Reload .bashrc to apply changes
source ~/.bashrc

# Enter the folder binary
cd binary/

# COPY BINARY BSMOD TO PATH
cp bsmod /data/data/com.termux/files/home/go/bin/

# EXCUTE BINARY USING COMMAND
run the bsmod binary with the following example
bsmod scan sni -f file.txt -t 200
either
bsmod scan direct -f file.txt -t 200
The sni mode is to check the hosts as an SSL connection and the DIRECT mode is to check which host they will load, and if they belong to a CDN it will tell you in the responses
Keep in mind that you have to navigate into the other binary folders where there are also list files with domains to check their connection

