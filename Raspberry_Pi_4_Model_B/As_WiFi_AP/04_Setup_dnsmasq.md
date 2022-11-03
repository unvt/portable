## Install dependencies

- `sudo apt install -y dnsmasq`

### Edit `/etc/dnsmasq.conf`

- `sudo mv /etc/dnsmasq.conf /etc/dnsmasq.conf.orig`
- `sudo vim /etc/dnsmasq.conf`
- To enter the insert mode of vim, press `i`
- Rewrite all as following:

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

- To Save and Exit vim, press `Esc`, then input `:wq!`

### Start up `dnsmasq`

- Start up `dnsmasq`
  - `sudo systemctl enable dnsmasq`
  - `sudo systemctl start dnsmasq`

### Operation check

- You should do followings
  - Without connecting to `unvt-portable` WiFi AP but on the same network with Raspberry Pi
    - See http://raspberrypi.local/
  - With connecting to `unvt-portable` WiFi AP
    - See http://raspberrypi.local/
