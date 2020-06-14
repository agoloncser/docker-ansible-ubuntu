# docker-ansible-ubuntu2004

[![Build Status](https://travis-ci.com/agoloncser/docker-ansible-ubuntu2004.svg?branch=master)](https://travis-ci.com/agoloncser/docker-ansible-ubuntu2004)

Docker image for testing ansible code.

Includes:
- ansible
- ansible-lint
- Molecule
- YAMLlint
- Prettier.js

## Running this image

    docker run --privileged -ti -v /sys/fs/cgroup:/sys/fs/cgroup:ro $(basename $(pwd) | sed 's/\.git//'):$(cat VERSION) /bin/bash

## Building this image manually

    docker build --tag $(basename $(pwd) | sed 's/\.git//'):$(cat VERSION) .
