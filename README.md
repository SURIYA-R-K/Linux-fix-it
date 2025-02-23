# 🛠️ General Linux Troubleshooting Tips

Linux is powerful, but sometimes things go wrong. Here are some quick tips to diagnose and fix common issues.

## 🔍 System Information & Monitoring

* uname -a → Check system details

* uptime → See system load & uptime

* df -h → Check disk space

* free -h → Monitor memory usage

* top or htop → View running processes

## 🌐 Network & Internet Issues

* ping -c 4 google.com → Test internet

* ip a → Show network interfaces

* netstat -tulnp → Check open ports

## 🔑 User & Permissions Issues

* sudo <command> → Run as superuser

* chmod 755 file → Change file permissions

* chown user:group file → Change file ownership

* ⚡ Fixing Package Issues

### Debian/Ubuntu:

```bash
sudo apt --fix-broken install  
sudo dpkg --configure -a  
```
### RHEL/CentOS:

```bash
sudo dnf clean all
sudo dnf update  
```
## 🔄 System & Boot Issues

* sudo update-grub → Fix bootloader

* journalctl -xe → View system logs

* dmesg → Check kernel messages

## 🛑 Force Restart or Shutdown

* reboot → Restart system

* shutdown -h now → Shutdown immediately

## 💡 This is just a basic guide.
## contents:

✅ "How to encrypt a folder in Linux"

✅ "How to decrypt a folder in Linux"
