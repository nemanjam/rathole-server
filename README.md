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

### Create `.env` and `rathole.server.toml` files

```bash
cp .env.example .env
cp rathole.server.toml.example rathole.server.toml
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
# escape $ with single \ AND QUOTES ""  <------ important
# example: TRAEFIK_AUTH="admin:\$asd1\$E3lsdAo\$3Mertp50JJ4LVU.HRR0"
```