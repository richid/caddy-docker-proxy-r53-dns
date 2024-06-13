# caddy-docker-proxy-r53-dns

`Dockerfile` and images that combines the [caddy-docker-proxy plugin](https://github.com/lucaslorentz/caddy-docker-proxy) with the [Route53 plugin](https://github.com/caddy-dns/route53) for DNS challenges.

## Publishing new versions

This repository publishes new images to GitHub's [container registry](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry) automatically when a new tag is pushed.
These tags should be tied to the underlying version of Caddy being used.

Process:
1. Update `Dockerfile` with new Caddy version
2. Create a new tag/release using the version from above
3. GitHub Action kicks off and generates a new image available at `ghcr.io/richid/caddy-docker-proxy-r53-dns:(<version>:latest)`
