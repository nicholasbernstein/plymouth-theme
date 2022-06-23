# Ubuntu Darwin
An BatBoy flavored plymouth for Linux Ubuntu.

## Installation

Add `ubuntu-darwin` to your `plymouth` themes directory.

    git clone https://github.com/nicholasbernstein/plymouth-theme.git
    sudo mv plymouth-theme/ubuntu-darwin /usr/share/plymouth/themes/ubuntu-darwin
    
Add `ubuntu-darwin` to `default.plymouth`'s alternatives

    sudo update-alternatives --install /usr/share/plymouth/themes/default.plymouth default.plymouth /usr/share/plymouth/themes/ubuntu-darwin/ubuntu-darwin.plymouth 10

To use the newly installed alternative, run

    sudo update-alternatives --config default.plymouth
    
and select `ubuntu-darwin`.

Finally update your `initramfs` to see changes on reboot

    sudo update-initramfs -u
    
### Uninstalling

    sudo update-alternatives --remove default.plymouth /usr/share/plymouth/themes/ubuntu-darwin/ubuntu-darwin.plymouth
    sudo rm -R /usr/share/plymouth/themes/ubuntu-darwin
    sudo update-initramfs -u
    
    
## Credits
Derived from the original `darwin` plymouth [with Apple Logo]: https://www.gnome-look.org/content/show.php/Darwin+Plymouth?content=170649
