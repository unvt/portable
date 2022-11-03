## Start up your Raspberry Pi

- Insert Micro SD Card to your Raspberry Pi
- Connect the USB-C power adapter to your Raspberry Pi
- Connect the Network cable to your Raspberry Pi

### SSH Log in to your Raspberry Pi

- `ssh pi@raspberrypi.local`
  - default password is `raspberry`

### Update package list

- `sudo apt update && sudo apt full-upgrade -y`

### Install `nginx` for check

- `sudo apt install -y nginx`
  - You should see http://raspberrypi.local/

### Install `vim` for edit files

- `sudo apt install -y vim`
