# docker-ansible-ubuntu

[![Build docker images](https://github.com/agoloncser/docker-ansible-ubuntu/actions/workflows/ci.yml/badge.svg)](https://github.com/agoloncser/docker-ansible-ubuntu/actions/workflows/ci.yml)
[![Generate tag](https://github.com/agoloncser/docker-ansible-ubuntu/actions/workflows/bump.yml/badge.svg)](https://github.com/agoloncser/docker-ansible-ubuntu/actions/workflows/bump.yml)
[![Lint Code Base](https://github.com/agoloncser/docker-ansible-ubuntu/actions/workflows/linter.yml/badge.svg)](https://github.com/agoloncser/docker-ansible-ubuntu/actions/workflows/linter.yml)

Ubuntu-based docker images for testing Ansible code.

Includes systemd and python3 and sudo.

## Running this image

    docker run --privileged -ti -v /sys/fs/cgroup:/sys/fs/cgroup:ro $(basename $(pwd) | sed 's/\.git//'):$(cat VERSION) /bin/bash

## Building this image manually

    docker build --tag $(basename $(pwd) | sed 's/\.git//'):$(cat VERSION) .
