# Ansible Role: ClamAV

[![Build Status](https://travis-ci.org/geerlingguy/ansible-role-clamav.svg?branch=master)](https://travis-ci.org/geerlingguy/ansible-role-clamav)

Installs ClamAV on RedHat/CentOS and Debian/Ubuntu Linux servers.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    clamav_packages:
      - clamav
      - clamav-base
      - clamav-daemon

(Defaults for Debian/Ubuntu shown). List of packages to be installed for ClamAV operations.

## Dependencies

None.

## Example Playbook

    - hosts: servers
      sudo: yes
      roles:
        - geerlingguy.clamav

## License

MIT / BSD

## Author Information

This role was created in 2017 by [Jeff Geerling](https://www.jeffgeerling.com/), author of [Ansible for DevOps](https://www.ansiblefordevops.com/).
