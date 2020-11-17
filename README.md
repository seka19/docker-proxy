> All as `sudo`

# Setup Docker

```
curl -fsSL https://get.docker.com -o get-docker.sh
sh get-docker.sh
usermod -aG docker username
```

# Setup docker-compose

```
curl -sL "https://github.com/docker/compose/releases/download/1.25.5/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
```

# Setup docker-proxy

```
curl -fsSL https://github.com/seka19/docker-proxy/archive/0.1.tar.gz -o docker-proxy.tar.gz
mkdir -p /var/www/docker-proxy
tar xfz docker-proxy.tar.gz --strip-components=1 -C /var/www/docker-proxy
cd /var/www/docker-proxy
docker-compose up -d
```