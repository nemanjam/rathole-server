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
