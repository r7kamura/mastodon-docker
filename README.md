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

## Required environment variables

### AWS_ACCESS_KEY_ID

For `aws ecr get-login`.

### AWS_DEFAULT_REGION

For `aws ecr get-login`.

### AWS_SECRET_ACCESS_KEY

For `aws ecr get-login`.

### AWS_ECR_URL

For `docker push ${AWS_ECR_URL}:${CIRCLE_BUILD_NUM}`.

## Optional environment variables

### MASTODON_GIT_URL

For `git clone ${MASTODON_GIT_URL:-https://github.com/tootsuite/mastodon.git}`.
Set this variable if you want to your build Docker image from another Mastodon Git repository.
