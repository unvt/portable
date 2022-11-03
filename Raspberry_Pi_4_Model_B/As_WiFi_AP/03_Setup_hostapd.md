## Install dependencies

- `sudo apt install -y hostapd`

### Edit `/etc/dhcpcd.conf`

- `sudo vim /etc/dhcpcd.conf`
- To enter the insert mode of vim, press `i`
- ADD following lines to the END of file:

```
interface wlan0
    static ip_address=192.168.10.1/24
    nohook wpa_supplicant
```

- To Save and Exit vim, press `Esc`, then input `:wq!`

### Add `/etc/hostapd/hostapd.conf`

- `sudo vim /etc/hostapd/hostapd.conf`
- To enter the insert mode of vim, press `i`
- Create a new file with the following contents:

```
country_code=JP
interface=wlan0
ssid=unvt-portable
hw_mode=g
channel=7
wpa=2
wpa_passphrase=password
wpa_key_mgmt=WPA-PSK
wpa_pairwise=TKIP
rsn_pairwise=CCMP
```

- To Save and Exit vim, press `Esc`, then input `:wq!`

### Star up `hostapd`

- Unblock WiFi
  - Check status
    - `sudo rfkill list`
  - If wlan is blocked
    - `sudo rfkill unblock wlan`
- Enable `hostapd`
  - `sudo systemctl unmask hostapd`
  - `sudo systemctl enable hostapd`
  - `sudo systemctl start hostapd`

### Operation check

- You should see `unvt-portable` AP in list of WiFi
