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

    clamav_run_freshclam: yes

Run `freshclam` to update scanning definitions when the playbook is run. Note that this will always be run at least once after `clamav_packages` installs new packages.

    clamav_daemon_state: started
    clamav_daemon_enabled: yes

Control whether the `clamav-daemon` service is running and/or enabled on system boot.

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
