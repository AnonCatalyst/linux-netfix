RUN THIS ON YOUR TERMINAL

 systemctl enable systemd-networkd
 systemctl enable systemd-resolved
 systemctl start systemd-networkd
 systemctl start systemd-resolved
 ln -sf /run/systemd/resolve/resolv.conf /etc/resolv.conf
 
 -------------------------------
 service resolvconf restart
 service network-manager restart
 -------------------------------
 
IF ERROR USE BELLOW COMMANDS 
 --------------------------------
 systemctl restart NetworkManager
 systemctl enable NetworkManager
 --------------------------------

STILL NOT WORKING? TRY THIS!
 ----------------------------
 sudo rm -rf /etc/resolv.conf
 sudo echo 'nameserver 8.8.8.8' >/etc/resolv.conf
 ____________________________
 
 ping google.com

Restart your pc (recommended) 
