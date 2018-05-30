# ansible-role-protonvpn

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-protonvpn.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-protonvpn)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-protonvpn-blue.svg?style=flat)](https://galaxy.ansible.com/linuxhq/protonvpn)
[![License](https://img.shields.io/badge/license-GPLv3-brightgreen.svg?style=flat)](COPYING)

macOS - Secure internet anywhere

## Requirements

This role requires homebrew and homebrew cask to be installed

## Role Variables

Available variables are listed below, along with default values:

    protonvpn_pkg: ProtonVPN
    protonvpn_domain: "ch.{{ protonvpn_pkg|lower }}.mac"
    protonvpn_defaults: {}

## Dependencies

None

## Example Playbook

    - hosts: localhost
      connection: local
      roles:
        - role: tkimball83.protonvpn
          protonvpn_defaults:
            AutoConnect:
              type: bool
              value: true
            ConnectOnDemand:
              type: bool
              value: true
            LaunchedBefore:
              type: bool
              value: true
            NeagentAppeared:
              type: bool
              value: true
            RememberLogin:
              type: bool
              value: true
            StartMinimized:
              type: bool
              value: false
            StartOnBoot:
              type: bool
              value: true
            SystemNotifications:
              type: bool
              value: true

## License

Copyright (C) 2018 Taylor Kimball <tkimball@linuxhq.org>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.
