# Using GlobalProtect on Linux

## Connecting on Ubuntu and Fedora

You can get the tar with the package files [here](https://www.dropbox.com/s/je49kik69doj2r1/PanGPLinux-6.0.4-c25.tgz?dl=0), and once you download the file, extract it with `tar -xzf PanGPLinux-6.0.4-c25.tgz` and install using your preferred package manager:

Using Apt (Ubuntu)
```
sudo apt install ./GlobalProtect_UI_deb-6.0.4.1-28.deb
```

Using Yum (Fedora, RedHat, CentOS) 
```
sudo yum localinstall GlobalProtect_UI_rpm-6.0.4.1-28.rpm
```

After this you should be able to launch the GlobalProtect client. Enter `vpn.csuchico.edu` as the portal address and press connect, you will be asked to sign in.

## Connecting on Arch

**DUE TO VPN CHANGES THIS MAY NO LONGER WORK**

Arch has a workaround as it does not have an official package for global protect that can be found [here](https://archlinux.org/packages/community/x86_64/globalprotect-openconnect/) and you will be able to connect using this package with the following command:
```bash
sudo openconnect --protocol=gp vpn.csuchico.edu
```