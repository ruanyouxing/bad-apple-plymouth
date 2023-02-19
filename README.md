# bad-apple-plymouth
Bad Apple Plymouth bootup splash (in 60 fps)

# Dependencies
* Plymouth ([AUR](https://aur.archlinux.org/packages/plymouth-git))<br>
* Make sure your bootloader already has `quiet splash loglevel=3 rd.udev.log_priority=3` [kernel
  parameters](https://wiki.archlinux.org/title/kernel_parameters)
# How to install?
Install this repo into `/usr/share/plymouth/themes` folder
```
sudo git clone https://github.com/ruanyouxing/bad-apple-plymouth /usr/share/plymouth/themes/bad_apple/
```

Then regenerate your initramfs by executing:
```
sudo plymouth-set-default-theme -R bad_apple
```
Reboot and you are done!

# FAQ
## My boot time so fast and the splash screen don't fully show?
* Edit your `/usr/lib/systemd/system/plymouth-quit.service`
* In [Service] section add `ExecStartPre=/usr/bin/sleep 4 (or whatever seconds
  you prefer)`
### [Refrences from here](https://www.reddit.com/r/archlinux/comments/u5fjbi/how_do_i_make_my_boot_time_slower/)

## Demo video soon ...
