# Global Protect

When using global protect on any platform an antivirus is required, check [ITSS details](https://support.csuchico.edu/TDClient/1984/Portal/KB/?CategoryID=15690) for which ones are compatible.

## Using GlobalProtect on Windows/MacOS

ITSS has instructions for these:

* [Windows](https://support.csuchico.edu/TDClient/1984/Portal/KB/ArticleDet?ID=73364)
* [MacOS](https://support.csuchico.edu/TDClient/1984/Portal/KB/ArticleDet?ID=73363)

## Using GlobalProtect on Linux

Currently the only way to connect to GlobalProtect on Linux is using the unofficial [GlobalProtect-openconnect](https://github.com/yuezk/GlobalProtect-openconnect) package. This package is maintained by someone not associated with Chico State or Palo Alto Networks, but is Free Open Source Software. Below are instructions for installation provided by the package maintainer.  These instructions are excerpts from the [GlobalProtect-openconnect README](https://github.com/yuezk/GlobalProtect-openconnect/blob/main/README.md).  

### Debian/Ubuntu based distributions

#### Install from PPA (Ubuntu 18.04 and later, except 24.04)

```
sudo apt-get install gir1.2-gtk-3.0 gir1.2-webkit2-4.0
sudo add-apt-repository ppa:yuezk/globalprotect-openconnect
sudo apt-get update
sudo apt-get install globalprotect-openconnect
```

> [!Note]
>
> For Linux Mint, you might need to import the GPG key with: `sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 7937C393082992E5D6E4A60453FC26B43838D761` if you encountered an error `gpg: keyserver receive failed: General error`.

#### **Ubuntu 24.04 and later**

The `libwebkit2gtk-4.0-37` package was [removed](https://bugs.launchpad.net/ubuntu/+source/webkit2gtk/+bug/2061914) from its repo, before [the issue](https://github.com/yuezk/GlobalProtect-openconnect/issues/351) gets resolved, you need to install them manually:

```bash
wget http://launchpadlibrarian.net/704701349/libwebkit2gtk-4.0-37_2.43.3-1_amd64.deb
wget http://launchpadlibrarian.net/704701345/libjavascriptcoregtk-4.0-18_2.43.3-1_amd64.deb

sudo dpkg --install *.deb
```

And if the latest package is not available in the PPA, you can follow the [Install from deb package](#install-from-deb-package) section to install the latest package.

#### **Ubuntu 18.04**

The latest package is not available in the PPA either, but you still needs to add the `ppa:yuezk/globalprotect-openconnect` repo beforehand to use the required `openconnect` package. Then you can follow the [Install from deb package](#install-from-deb-package) section to install the latest package.

#### Install from deb package

Download the latest deb package from [releases](https://github.com/yuezk/GlobalProtect-openconnect/releases) page. Then install it with `apt`:

```bash
sudo apt install --fix-broken globalprotect-openconnect_*.deb
```


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
