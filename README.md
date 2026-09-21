# caddy-custom-build

Custom Caddy builds for personal VPS deployments.

Built with [xcaddy](https://github.com/caddyserver/xcaddy) and these modules:

- `github.com/mholt/caddy-l4`
- `github.com/WeidiDeng/caddy-cloudflare-ip`
- `github.com/caddyserver/jsonc-adapter`

## Build and release

Run **Actions → Build Caddy → Run workflow** and enter an explicit upstream Caddy tag, for example `v2.11.4`.

The workflow builds and verifies:

- `caddy-linux-amd64`
- `caddy-linux-arm64`
- `SHA256SUMS`

It then publishes those files in a GitHub Release whose tag matches the Caddy version.

Production VPS hosts only need to download and verify the appropriate release binary; Go and xcaddy are not required on the VPS.
