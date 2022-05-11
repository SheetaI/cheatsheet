**Note: sc = systemctl**

- Install needed pkgs

  `sudo pacman -S virt-manager qemu vde2 ebtables dnsmasq bridge-utils openbsd-netcat --needed`

- Enable & Start libvirtd

  `sc enable libvirtd --now`

- Verify if running

  `sc status libvirtd`

- Overwrite firewalld config to fix no connection

  `sudo touch /etc/firewalld/firewalld.conf`


      alternatively, edit FirewallBackend=nftables to FirewallBackend=iptables in /etc/firewalld/firewalld.conf 


- Restart firewalld for changes to take effect

  `sc restart firewalld`

- Restart libvirtd

  `sc restart libvirtd`

- Add user to libvirt group

  `sudo usermod -aG libvirt sheetal`

- Add the user above without logging-out/restarting

  `newgrp libvirt`

- Restart libvirtd

  `sc restart libvirtd`

- Activate default networking

  `sudo virsh net-start default`

- Verify if default is | active | yes | yes

  `sudo virsh net-list`
