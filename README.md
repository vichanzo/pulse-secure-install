# pulse-secure-install

#https://community.pulsesecure.net/t5/Pulse-Desktop-Clients/pulseUi-doesn-t-work-in-ubuntu-20-04/td-p/42721

#https://askubuntu.com/questions/1135065/cant-run-pulse-secure-on-ubuntu-19-04-because-libwebkitgtk-1-0-so-0-is-missing

cd /usr/local/pulse/

sudo sed -i "s/UBUNTU_VER\ \=\ 18\ \]/& \|\|\ [\ \$UBUNTU_VER\ \=\ 20 \]/" PulseClient_x86_64.sh

sudo apt-get install libenchant1c2a

/usr/local/pulse/pulseUi


#above didn't work
======================================
# https://community.pulsesecure.net/t5/Pulse-Desktop-Clients/pulseUi-doesn-t-work-in-ubuntu-20-04/td-p/42721

# change sources.list to 18.04

# Download ps-pulse-linux-9.1r5.0-b151-ubuntu-debian-64-bit-installer.deb
# https://www.isis.vanderbilt.edu/vpn 

# Install deb file
cd ~/Downloads/
sudo dpkg -i ps-pulse-linux-9.1r5.0-b151-ubuntu-debian-64-bit-installer.deb

sudo sed -i "s/UBUNTU_VER\ \=\ 18\ \]/& \|\|\ [\ \$UBUNTU_VER\ \=\ 20 \]/" PulseClient_x86_64.sh

sudo /usr/local/pulse/PulseClient_x86_64.sh install_dependency_packages

/usr/local/pulse/pulseUi



=========================================

sudo add-apt-repository 'deb http://archive.ubuntu.com/ubuntu bionic main universe'
sudo apt install -t bionic libwebkitgtk-1.0-0
sudo dpkg -i ps-pulse-linux-9.1r5.0-b151-ubuntu-debian-64-bit-installer.deb

