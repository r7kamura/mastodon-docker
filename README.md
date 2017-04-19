# mastodon-docker

Build assets precompiled [mastodon](https://github.com/tootsuite/mastodon) docker image to docker image repository.

## Usage

1. Fork this repository
1. Enable CircleCI integration
1. Set environment variables on CircleCI
1. Build CircleCI to build and push docker image

## Supported Repository

Currently we support only AWS ECR.

## Environment variables

- `AWS_ACCESS_KEY_ID`
- `AWS_ECR_URL`
- `AWS_REGION`
- `AWS_SECRET_ACCESS_KEY`
- `MASTODON_GIT_URL` (default: `https://github.com/tootsuite/mastodon.git`)
