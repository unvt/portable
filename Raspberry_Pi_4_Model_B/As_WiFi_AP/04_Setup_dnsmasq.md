## Install dependencies

- `sudo apt install -y dnsmasq`

### Edit `/etc/dnsmasq.conf`

- `sudo mv /etc/dnsmasq.conf /etc/dnsmasq.conf.orig`
- `sudo vim /etc/dnsmasq.conf` and rewrite as following:

```
# Listening interface
interface=wlan0
# Pool of IP addresses served via DHCP
dhcp-range=192.168.10.2,192.168.10.100,255.255.255.0,24h
# Local wireless DNS domain
domain=local
# Alias for this router
address=/raspberrypi.local/192.168.10.1
# for `raspberrypi.local` name resolve
local=/local/
domain=local
expand-hosts
```

### Start up `dnsmasq`

- Start up `dnsmasq`
  - `sudo systemctl enable dnsmasq`
  - `sudo systemctl start dnsmasq`

### Operation check

- You should do followings
  - Without connecting to `unvt-portable` WiFi AP
    - See http://raspberrypi.local/
  - With connecting to `unvt-portable` WiFi AP
    - See http://raspberrypi.local/
