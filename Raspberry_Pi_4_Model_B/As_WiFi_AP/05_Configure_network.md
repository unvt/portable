## Install dependencies

- `sudo DEBIAN_FRONTEND=noninteractive apt install -y netfilter-persistent iptables-persistent`

### Edit `/etc/sysctl.conf`

- `sudo vim /etc/sysctl.conf`
- Uncomment following line

```
net.ipv4.ip_forward=1
```

- `sudo sysctl -p`

### Configure network

- Change and save configure of `iptables`
  - `sudo iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE`
  - `sudo netfilter-persistent save`

### Operation check

- You should do followings
  - Connect to `unvt-portable` WiFi AP
  - See https://www.google.com/
