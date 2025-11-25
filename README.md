# caddy-opt-image

A customized Caddy web server Docker image with extended functionality through additional modules.

## Base Image

Built upon the official [Caddy Docker image](https://hub.docker.com/_/caddy), with versioning matching the upstream Caddy releases.

## Included Modules

This image includes the following Caddy modules:

- **[caddy-docker-proxy](https://github.com/lucaslorentz/caddy-docker-proxy)** - Automatic reverse proxy configuration via Docker labels
- **[caddy-l4](https://github.com/mholt/caddy-l4)** - Layer 4 (TCP/UDP) proxy support
- **[caddy-dns/cloudflare](https://github.com/caddy-dns/cloudflare)** - Cloudflare DNS provider for DNS-01 ACME challenges
- **[caddy-security](https://github.com/greenpau/caddy-security)** - Authentication portal and authorization middleware
- **[caddy-crowdsec-bouncer](https://github.com/hslatman/caddy-crowdsec-bouncer)** - CrowdSec integration for threat prevention
- **[caddy-maxmind-geolocation](https://github.com/porech/caddy-maxmind-geolocation)** - MaxMind GeoIP integration for geolocation-based routing

## Image Tags

Images are automatically built and tagged with:
- `latest` - Most recent build from main branch
- `<caddy-version>` - Specific Caddy version (e.g., `2.7.6`)
- `<caddy-version>-<git-sha>` - Caddy version with git commit hash
- `<git-sha>` - Short git commit hash

## Usage

Pull the image from Docker Hub:

```bash
docker pull markoria/caddy:latest
```

Or use a specific version:

```bash
docker pull markoria/caddy:2.10.2
```

See `docker-compose.yml` for a complete deployment example with caddy-docker-proxy.
