## Install dependencies

- `sudo apt install -y git make`

### Clone repository

- `git clone -b main --depth 1 https://github.com/yuiseki/vector-tile-builder.git`
- `cd vector-tile-builder`

### Configure `.env`

- `vim .env`

```
REGION=asia/japan/kanto
PORT=80
TILES_URL=http://raspberrypi.local/zxy/
```

### Run `make`

- `make`
- This step really takes an amazing amount of time, so let's go to bed!
