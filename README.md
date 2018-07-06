<p align="center">
  <img src="https://github.com/e-corp-sam-sepiol/Documentation/blob/master/images/vertcoin-branding.png" width="343" height="68" /> <img src="https://i.imgur.com/1RKi4wd.png" width="90">
</p>

------------

# Vertnode 
## An automated installation for Vertcoin full node(s) on a Raspberry Pi 3
- [x] Install dependencies
- [x] Modify `ufw` firewall rules for security
- [x] Find, format and configure USB flash drive
- [x] Create and configure swap space on USB flash drive
- [x] Download & compile Berkeley DB
- [x] Clone, build and install Vertcoin Core
- [x] Provide option to grab latest release rather than building from source
* Add version detection for release based on lshw detection
- [x] Configure `~/.vertcoin/vertcoin.conf`
- [x] Prompt to transfer blockchain
- [x] Provide option for `bootstrap.dat` sideload
- [x] Begin Vertcoin Sync
- [x] Clone & build `p2pool-vtc`
- [x] Configure & launch `p2pool-vtc` 
- [x] Setup crontab jobs
- [x] Display installation report
- [ ] Modify user input prompt to capture all user input at start of script
- [x] Script installation introduction, Vertcoin full node: what, why and how?
------------

### Instructions | How to use
* **Raspberry Pi 3**
```
git clone https://github.com/e-corp-sam-sepiol/vertnode.git
cd vertnode/
chmod +x install-vertnode.sh
sudo ./install-vertnode.sh 
```
### Functioning Status
- [x] Raspberry Pi 3 B+ | ARM Cortex-A53 1.4GHz | 1GB SRAM | 

## Testing Errors

- [x] **Configuring firewall | Fixed with: `sudo reboot` then re-run `install_vertnode.sh`**

**`RECOMMENDED:` When you first boot your Raspberry Pi ensure that you `sudo apt-get update ; sudo apt-get upgrade -y ; sudo reboot` and `ssh` back into the Raspberry Pi before running the `install-vertnode.sh` script.**

**This error occurs when `sudo apt-get upgrade` installs a new kernel to the Raspberry Pi, it affects `iptables` which is a part of the kernel. Updating the kernel requires a reboot.**
```
ERROR: initcaps
[Errno 2] iptables v1.6.0: can't initialize iptables table `filter': Table does not exist (do you need to insmod?)
Perhaps iptables or your kernel needs to be upgraded.
```
------------
### Vertnode | Automated Vertcoin full node Installation Testing Results
- [x] Raspberry Pi 3 - **Installs Vertcoin full node** | **Installs p2pool-vtc node** | **Looks for USB flash drives (`sda`) for storage.** More testing to be done. Small amount of user input required. 
- [ ] Raspberry Pi Zero W - Not tested
- [ ] Intel NUC - Not tested

------------

### [Manual Installation Walkthrough: Raspberry Pi 3](https://github.com/vertcoin-project/VertDocs/blob/master/docs/FullNodes/raspberry-pi.md)
### [Manual Installation Walkthrough: Raspberry Pi Zero W](https://github.com/vertcoin-project/VertDocs/blob/master/docs/FullNodes/raspberry-pi-zero-w.md)
### [Manual Installation Walkthrough: Intel NUC](https://github.com/vertcoin-project/VertDocs/blob/master/docs/FullNodes/intel-nuc.md)

------------

<p align="center">
  <img src="https://i.imgur.com/zgx4uiu.jpg">
</p>
