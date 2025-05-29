

```ts
// this works on Rathole server, matches routes
// doesn't issue wildcard certificate, needs dnsChallenge, not httpChallenge on client
- 'traefik.http.routers.rathole-pi.rule=HostRegexp(`{subdomain:[a-z0-9-]+}.pi.${SITE_HOSTNAME}`, `www.{subdomain:[a-z0-9-]+}.pi.${SITE_HOSTNAME}`)'

// but can't confirm HTTP 5080 tunnel is working, 404 not found for HTTP without HTTPS redirect


// EDIT:

http tunnel works, confirmed 
just dont use HostRegexp() wildcard subdomain ON BOTH Rathole server and client
use HostRegexp() on server and Host() on client
// example client
SITE_HOSTNAME=hello7.pi.nemanjamitic.com
- 'traefik.http.routers.nginx-with-volume.rule=Host(`${SITE_HOSTNAME}`)'

```