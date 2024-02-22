# Global Protect

When using global protect on any platform an antivirus is required, check [ITSS details](https://support.csuchico.edu/TDClient/1984/Portal/KB/?CategoryID=15690) for which ones are compatible.

## Using GlobalProtect on Windows/MacOS

ITSS has instructions for these:

* [Windows](https://support.csuchico.edu/TDClient/1984/Portal/KB/ArticleDet?ID=73364)
* [MacOS](https://support.csuchico.edu/TDClient/1984/Portal/KB/ArticleDet?ID=73363)

## Using GlobalProtect on Linux

Currently the only way to connect to GlobalProtect on Linux is using the unofficial [GlobalProtect-openconnect](https://github.com/yuezk/GlobalProtect-openconnect) package. This package is maintained by someone not associated with Chico State or Palo Alto Networks, but is Free Open Source Software. Below are instructions for installation provided by the package maintainer.

### Linux Mint, Ubuntu 18.04+
```sh
sudo add-apt-repository ppa:yuezk/globalprotect-openconnect
sudo apt-get update
sudo apt-get install globalprotect-openconnect
```

> For Linux Mint, you might need to import the GPG key with: `sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 7937C393082992E5D6E4A60453FC26B43838D761` if you encountered an error `gpg: keyserver receive failed: General error`.

### Arch Linux, Manjaro

```sh
sudo pacman -S globalprotect-openconnect
```

### AUR snapshot version

```sh
yay -S globalprotect-openconnect-git
```

### Fedora

```sh
sudo dnf copr enable yuezk/globalprotect-openconnect
sudo dnf install globalprotect-openconnect
```

### Using GlobalConnect

The GlobalConnect's GUI option has a trial period, the best way to connect is via the terminal

Once installed you can connect to the vpn with the following command:
```sh
sudo gpclient connect vpn.csuchico.edu
```
You can exit GlobalConnect with `ctrl + c`
