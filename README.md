# Mullvad VPN Linux Command Lines

This repository contains a collection of command lines for installing Mullvad VPN on various Linux-based operating systems. 
These commands allow users to purge, download, and install Mullvad VPN regardless of its version.

## Supported Operating Systems

The following Linux-based operating systems are supported:

- Arch Linux
- Debian
- Fedora
- Linux Mint
- Manjaro
- openSUSE Leap
- openSUSE Tumbleweed
- Ubuntu

## Package Managers

Package managers are used to install, update, and manage software packages on Linux-based operating systems. Here are the package manager commands used in the previous examples:

- apt: Advanced Packaging Tool (Debian, Ubuntu, and other Debian-based distributions)
- dnf: Dandified YUM (Fedora and other Red Hat-based distributions)
- pacman: Package Manager (Arch Linux and other Arch-based distributions)
- zypper: Zypper Package Manager (openSUSE Leap and Tumbleweed)

## Command Lines

### Arch Linux

```sudo pacman -R mullvad-vpn && wget --content-disposition https://mullvad.net/download/app/arch/latest && sudo pacman -U $(ls | grep mullvad-vpn | grep .pkg.tar.zst | head -n 1) && sudo mv $(ls | grep mullvad-vpn | grep .pkg.tar.zst | head -n 1) Mullvad-vpn.pkg.tar.zst```

## CentOS

```sudo yum remove -y mullvad-vpn && sudo rpm --import https://mullvad.net/media/mullvad-gpg-key.txt && sudo wget https://mullvad.net/media/app/latest/rpm/mullvad-vpn-client-*.x86_64.rpm && sudo rpm -i $(ls | grep mullvad-vpn-client | head -n 1) && sudo rm -f $(ls | grep mullvad-vpn-client | head -n 1)
```
### Debian

```sudo apt purge mullvad-vpn && wget --content-disposition https://mullvad.net/download/app/deb/latest && sudo apt install -y $(ls | grep MullvadVPN | head -n 1) && sudo mv $(ls | grep MullvadVPN | head -n 1) Mullvad-vpn.deb```

## Linux Mint

```sudo apt purge mullvad-vpn && wget --content-disposition https://mullvad.net/download/app/deb/latest && sudo apt install -y $(ls | grep MullvadVPN | head -n 1) && sudo mv $(ls | grep MullvadVPN | head -n 1) Mullvad-vpn.deb```

## Manjaro

```sudo pacman -R mullvad-vpn && wget --content-disposition https://mullvad.net/download/app/arch/latest && sudo pacman -U $(ls | grep mullvad-vpn | grep .pkg.tar.zst | head -n 1) && sudo mv $(ls | grep mullvad-vpn | grep .pkg.tar.zst | head -n 1) Mullvad-vpn.pkg.tar.zst ```

### openSUSE and openSUSE Tumbleweed

```sudo pacman -R mullvad-vpn && wget --content-disposition https://mullvad.net/download/app/arch/latest && sudo pacman -U $(ls | grep mullvad-vpn | grep .pkg.tar.zst | head -n 1) && sudo mv $(ls | grep mullvad-vpn | grep .pkg.tar.zst | head -n 1) Mullvad-vpn.pkg.tar.zst ```

### Ubuntu

```sudo apt purge mullvad-vpn && wget --content-disposition https://mullvad.net/download/app/deb/latest && sudo apt install -y```
