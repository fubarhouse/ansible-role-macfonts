# Ansible Role: Fonts

[![Build Status](https://travis-ci.org/fubarhouse/ansible-role-macfonts.svg?branch=master)](https://travis-ci.org/fubarhouse/ansible-role-macfonts)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-fubarhouse--macfonts-13836.svg)](https://galaxy.ansible.com/fubarhouse/macfonts)

This role is intended to install specific fonts which support sigatures onto macOSX systems for use in JetBrains IDEs.

It is configurable to install many fonts from various locations, and it has been made available publicly despite the niche purpose for existing.

## Requirements

 - Homebrew

## Role Variables

By default, the following fonts will be installed when running the role:

````
  - FiraCode
  - Monoid
````

To configure alternative fonts, use the following format.
````
fonts:
  - name: Monoid
    archive: https://github.com/JB-Dmitry/monoid/archive/master.tar.gz
    version: master
    directory: Monoisome
    files:
      - Monoisome-Regular.ttf
````

Please note the version is critical to input correctly, as github archives structure contains the tag used when creating the release or `master`.

## Dependencies

None.

## Example Playbook

````
- hosts: localhost
  roles:
    - fubarhouse.macfonts
````

## License

MIT / BSD

## Author Information

This role was created in 2016 by [Karl Hepworth](twitter.com/fubarhouse).
