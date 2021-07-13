FROM node:14-buster-slim
ENV DEBIAN_FRONTEND noninteractive
RUN apt update && apt upgrade -y && apt install -y curl gitdocker
RUN [ ! -f "package.json" ] && npm init -y
RUN npm i -D semantic-release@17 @semantic-release/commit-analyzer @semantic-release/release-notes-generator @semantic-release/gitlab @semantic-release/git @semantic-release/changelog
ADD files/.releaserc /
