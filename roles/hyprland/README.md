# Ansible role -  mto79.workstation.hyprland

This is an Ansible role to install and configure hyprland.
Include more information about hyprland in this section.

## Table of Contents

- [Ansible role -  mto79.workstation.hyprland](#ansible-role----mto79workstationhyprland)
  - [Table of Contents](#table-of-contents)
  - [Requirements](#requirements)
  - [Role variables](#role-variables)
    - [Setup](#setup)
    - [Upstream](#upstream)
  - [Example Playbook](#example-playbook)

## [Requirements](#requirements)

- The minimum version of Ansible required is 2.12.0.
- The minimum version of Jinja template 2.11.3

## [Role variables](#role-variables)

### Setup

| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |

### Upstream

| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |

## [Example Playbook](#example-playbook)

```yaml
    - hosts: "servers"
      roles:
        - role: "mto79.workstation.hyprland"
          vars:
            __role_action: "setup"
          tags: ['workstation', 'hyprland']

```
