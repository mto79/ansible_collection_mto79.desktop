Ansible Role desktop.tmux
=========

This is an Ansible role to install and configure tmux.


Table of Contents
-----------------

- [Ansible role - mto79.desktop.tmux](#ansible-role---mto79desktoptmux)
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
| ------------------------------ | ------- | ------- | ----------- |
| `desktop_tmux_tmuxinator_enable` | Boolean | `false` | Enable tmuxinator |


### Upstream

| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |

## [Example Playbook](#example-playbook)

```yaml
    - hosts: servers
      roles:
        - role: "mto79.desktop.tmux"
          vars:
            __role_action:
              - "setup"
          tags: ['desktop', 'tmux']

```

Author Information
------------------

- MTO79 (@mto79)

Role Testing
------------

This repository comes with Molecule tests for Docker on the supported platforms.
Install Molecule by running

```bash
pip3 install -r requirements.txt
```

Run the tests with

```bash
molecule test
```

These tests are automatically ran by GitHub Actions on push. If the tests are successful, the role is automatically published to Ansible Galaxy.

