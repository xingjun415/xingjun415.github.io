# Install NVIDIA on Ubuntu 16.04
1. uninstall old nvidia driver
sudo apt-get purge nvidia*
2. disable nouveau driver
modify /etc/modprobe.d/blacklist.conf, and add the following lines:  
blacklist vga16fb  
blacklist nouveau  
blacklist rivafb  
blacklist rivatv  
blacklist nvidiafb  
3. execute the following command :  
sudo update-initramfs -u   
4. reboot system and enter init 1 mode, then execute the following command to stop x-window service  
  sudo service lightdm stop  
5. install NVIDIA driver  
6. execute the following command :  
  sudo service lightdm start  


