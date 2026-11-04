# caddy-docker-proxy-r53-dns

`Dockerfile` and images that combines the [caddy-docker-proxy plugin](https://github.com/lucaslorentz/caddy-docker-proxy) with the [Route53 plugin](https://github.com/caddy-dns/route53) for DNS challenges.

## Publishing new versions

A push to `main` with a new Caddy version publishes an image to GitHub's [container registry](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry) at `ghcr.io/richid/caddy-docker-proxy-r53-dns:<version>` and `:latest`, and creates a git tag and a GitHub release with that version.
The version is the Caddy version in the `FROM caddy:<version>-alpine` line of the `Dockerfile`.
A push to `main` without a new Caddy version only builds the image, so a published tag never changes.
Pull requests build the image but do not publish it.

Renovate updates the Caddy base images and the plugin versions in the `Dockerfile`.
Minor and patch updates merge automatically when the build passes.
