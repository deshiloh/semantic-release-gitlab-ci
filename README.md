# Semantic Release Docker image for GitLab CI

A docker image to enforce Semantic Versioning with the help of [semantic-release](https://semantic-release.gitbook.io/semantic-release/).

## Usage

As the Docker image is automatically build on Docker Hub, you can use it right in your pipeline:

```yaml
publish:
  image: marcandreappel/semantic-release-gitlab-ci:latest
  stage: release
  script:
    - npx semantic-release --branches main
  only:
    - main
```

