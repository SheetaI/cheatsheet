**run**

`sudo systemctl enable getty@tty1.service`

`mkdir -p /etc/systemd/system/getty.target.wants`

`ln -s /usr/lib/systemd/system/getty@.service /etc/systemd/system/getty.target.wants/getty@tty1.service`

`sudo vim /etc/systemd/system/getty.target.wants/getty@tty1.service`

**Edit [Service]:**
ExectStart & Type lines

`ExecStart=-/sbin/agetty --autologin sheetal --noclear %I $TERM`

`Type=simple`

**Add in .bash_profile:**
Automatic startx

`[ "$(tty)" = "/dev/tty1" ] && exec startx`

**run**

`systemctl set-default multi-user.target`

**done**

**to reverse changes**

`systemctl set-default graphical.target`
