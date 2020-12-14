# tobias_richter.docker

[![Build Status](https://github.com/tobias-richter/ansible-docker/workflows/CI/badge.svg)](https://github.com/tobias-richter/ansible-docker/actions)

This role installs docker-ce and docker-ce-cli from the official docker
repos.

## Requirements

This role requires Ansible 2.7 or higher.

## Role Variables

See [defaults/main.yml](defaults/main.yml) for the documented role variables.

## Example Playbook

This playbook installs docker and ensures that the service is started
after mariadb.

    - hosts: docker
	  roles:
	    - role: tobias_richter.docker
          docker_unit_after: 
          - mariadb.service
