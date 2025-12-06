# Make sure you replace SERVICE.

# SERVICE with Tailscale Sidecar Configuration

This Docker Compose configuration sets up [chartdb](https://github.com/chartdb/chartdb) with Tailscale as a sidecar container.

## SERVICE

[chartdb](https://github.com/chartdb/chartdb)

## Configuration Overview

In this setup, the `tailscale-SERVICE` service runs Tailscale, which manages secure networking for the SERVICE. The `SERVICE` service utilizes the Tailscale network stack via Docker's `network_mode: service:` configuration. This setup ensures that SERVICE's service is only accessible through the Tailscale network (or locally, if preferred), providing an extra layer of security and privacy for your SERVICE.

## Files to check

Please check the following contents for validity as some variables need to be defined upfront.

- `.env` // This files hold the main parts
- `./config/serve.json` // This file requires a service port of the app to be defined
