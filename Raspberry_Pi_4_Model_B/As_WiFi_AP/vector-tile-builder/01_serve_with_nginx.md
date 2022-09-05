## Install dependencies

- If you ignore step of install nginx, make sure to install
  - `sudo apt install -y nginx`

### Configure `nginx`

- `sudo vim /etc/nginx/sites-available/default`
- Rewrite root dir
  - `/home/pi/vector-tile-builder/docs`

### Restart `nginx`

- `sudo service nginx restart`

### Operation check

- You should do followings
  - Without connecting to `unvt-portable` WiFi AP but on the same network with Raspberry Pi
    - See http://raspberrypi.local/
  - With connecting to `unvt-portable` WiFi AP
    - See http://raspberrypi.local/
