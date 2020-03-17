## Install Docker & docker-compose
```sh
sudo curl -sSL https://get.docker.com/ | sh
sudo curl -L "https://github.com/docker/compose/releases/download/1.25.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose && chmod +x /usr/local/bin/docker-compose
```
## Install BBRPlus Kernel
```sh
sudo wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh
```

## Build containers
```sh
git clone https://github.com/phlinhng/docker-caddy-v2ray.git
cd docker-caddy-v2ray/
vi docker-compose.yml
vi ./src/caddy/Caddyfile
vi ./src/v2ray/config.json
sudo docker-compose up --build
```

## Variables
+ `docker-compose.yml`: change `CLOUDFLARE_EMAIL` and `CLOUDFLARE_API_KEY` to your own
+ `./src/caddy/Caddyfile`: rename domain to your own domain (make sure your domain is resolved to your VPS IP)
+ `./src/v2ray/config.json`: modified whatever you prefer

