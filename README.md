# mastodon-docker

Build and push assets-precompiled [Mastodon](https://github.com/tootsuite/mastodon) Docker image using [CircleCI](http://circleci.com/).

Currently we support only AWS ECR as Docker image repository.
Contributions are welcome to support other repositories. (e.g. Docker Hub, Quay.io, etc.)

## Usage

1. Fork this repository
1. Enable CircleCI integration
1. Set environment variables on CircleCI
1. Run CircleCI job to build and push Docker image

Note: We use CircleCI build number for each built Docker image tag.

## Environment variables

### Required

- `AWS_ACCESS_KEY_ID`
- `AWS_ECR_URL`
- `AWS_REGION`
- `AWS_SECRET_ACCESS_KEY`

### Optional

- `MASTODON_GIT_URL` (default: `https://github.com/tootsuite/mastodon.git`)
