## Install Docker

- `sudo curl -fsSL https://get.docker.com | sudo bash`

### Add user to docker group

- `sudo gpasswd -a $(whoami) docker`
- `sudo chgrp docker /var/run/docker.sock`

### MUST Reboot Raspberry Pi

- `sudo reboot`

### Operation check

- You should do followings
  - Check Docker is working correctly
    - `docker -v`
    - `docker ps`
