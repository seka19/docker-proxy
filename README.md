# Setup Docker

```
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo usermod -aG docker $USER
```

Then reboot server.

# Setup docker-compose

```
sudo curl -sL "https://github.com/docker/compose/releases/download/1.25.5/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

# Setup docker-proxy

```
curl -fsSL https://github.com/seka19/docker-proxy/archive/0.5.tar.gz -o docker-proxy.tar.gz
sudo mkdir -p /var/www/docker-proxy && sudo chown -R $USER:$(id -gn) /var/www
tar xfz docker-proxy.tar.gz --strip-components=1 -C /var/www/docker-proxy
cd /var/www/docker-proxy
docker login registry.gitlab.com
docker-compose up -d
```