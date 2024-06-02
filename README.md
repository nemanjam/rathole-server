# Rathole server

- https://nitinja.in/tech/

- Generate keys:

```bash
docker run -it --rm rapiz1/rathole --genkey

# Private Key:
# <private_key>

# Public Key:
# <public_key>
```

- copy `rathole.server.toml` with keys:

```
scp ./rathole.server.toml ubuntu@amd2:~/rathole-server/rathole.server.toml
```

