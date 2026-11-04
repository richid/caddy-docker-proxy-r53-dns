# caddy-docker-proxy-r53-dns

`Dockerfile` and images that combines the [caddy-docker-proxy plugin](https://github.com/lucaslorentz/caddy-docker-proxy) with the [Route53 plugin](https://github.com/caddy-dns/route53) for DNS challenges.

## Publishing new versions

Each push to `main` publishes a new image to GitHub's [container registry](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry) at `ghcr.io/richid/caddy-docker-proxy-r53-dns:<version>` and `:latest`.
The tag is the Caddy version in the `FROM caddy:<version>-alpine` line of the `Dockerfile`.
The first publish of a new version also creates a git tag and a GitHub release with that version.
Pull requests build the image but do not publish it.

Renovate updates the Caddy base images and the plugin versions in the `Dockerfile`.
Minor and patch updates merge automatically when the build passes.
