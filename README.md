* [Time synchronization](#chapter-0)
* [Wi-Fi](#chapter-1)
* [Journalctl](#chapter-2)

<a id="chapter-0"></a>
# Time synchronization

```
sudo ntpdate pool.ntp.org

# Add to autoloading
sudo crontab -e
@reboot /usr/bin/ntpdate pool.ntp.org
```

<a id="chapter-1"></a>
# Wi-Fi

```
sudo apt install network-manager
sudo systemctl start NetworkManager
sudo systemctl enable NetworkManager

sudo nmcli dev wifi connect "iCherry" password "0663414413"

nmcli device status
nmcli dev wifi list
```

<a id="chapter-1"></a>
# Journalctl 

```
journalctl

sudo nano /etc/systemd/journald.conf
```

`Storage=none` - logging exclusion