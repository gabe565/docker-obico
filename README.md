# Obico Docker Images

[![Build](https://github.com/gabe565/docker-obico/actions/workflows/build.yml/badge.svg)](https://github.com/gabe565/docker-obico/actions/workflows/build.yml)

This repo builds Docker images for [TheSpaghettiDetective/obico-server](https://github.com/TheSpaghettiDetective/obico-server) to be used in hosting environments that do not support building a local image.

The Obico git ref is automatically updated by Renovate bot, so new Obico releases will be available within a few hours of a push to the Obico release branch.

## Images

- [ghcr.io/gabe565/obico/web](https://github.com/gabe565/docker-obico/pkgs/container/obico%2Fweb)
- [ghcr.io/gabe565/obico/ml-api](https://github.com/gabe565/docker-obico/pkgs/container/obico%2Fml-api)

## Deployment

### Docker

These images are built very similarly to the [`docker-compose.yml`](https://github.com/TheSpaghettiDetective/obico-server/blob/release/docker-compose.yml) provided by Obico.

The main difference is that the server container in this repo does not require a volume bind at `/frontend`. Those files are built directly into the container image.

### Kubernetes

I have built a Helm chart for Kubernetes deployments. See [gabe565/obico](https://github.com/gabe565/charts/tree/main/charts/obico) for details.
