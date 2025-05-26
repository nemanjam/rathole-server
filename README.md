# Rathole server

- https://nitinja.in/tech/

### Generate keys:

```bash
docker run -it --rm rapiz1/rathole --genkey

# Private Key:
# <private_key>

# Public Key:
# <public_key>
```


```bash
# copy `rathole.server.toml` with keys:

scp ./rathole.server.toml ubuntu@amd2:~/rathole-server/rathole.server.toml
```

### Generate base64 token

```bash
openssl rand -base64 32
```

### With Traefik TCP router for 80 and 443

```
git checkout feat/traefik-tcp-router
```

#### Create proxy network

```bash
docker network create proxy
```

### Traefik dashboard for debugging

```bash
sudo apt install apache2-utils

htpasswd -nb admin yourpassword

# starts with admin:...
# escape $ with single \
```