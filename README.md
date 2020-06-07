# tobias_richter.docker

[![Build Status](https://travis-ci.org/tobias-richter/ansible-docker.svg?branch=master)](https://travis-ci.org/tobias-richter/ansible-docker)

This roles installs docker-ce and docker-ce-cli from the official docker
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
