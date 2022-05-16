# run
`sudo systemctl edit getty@tty1`

# Edit the line ExectStart=
`ExecStart=-/sbin/agetty --autologin sheetal --noclear %I $TERM`

# Automatic startx
`[ "$(tty)" = "/dev/tty1" ] && exec startx`

# run
`systemctl set-default multi-user.target`

# done!

# to reverse changes
`systemctl set-default graphical.target`
