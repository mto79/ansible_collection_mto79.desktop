# Ansible Collection - mto79.desktop

This ansible collection includes a number of roles for installing and configuring tools for my personal desktop setup .

**Author:** Marc Ouwerkerk, [marc@mto.nu](mailto:marc@mto.nu)

**Repo:** [ansible_collection_mto79.desktop](https://github.com/mto79/ansible_collection_mto79.desktop)


## Table of Contents

- [Ansible collection - mto79.desktop](#ansible-collection---mto79desktop)
  - [Table of Contents](#table-of-contents)
  - [Requirements](#requirements)
  - [Collection Structure](#collection-structure)
    - [Plugins](#plugins)
    - [Modules](#modules)
    - [Roles](#roles)
  - [Pre-commit](#pre-commit)
  - [Changelogs](#changelogs)
    - [Generating changelogs](#generating-changelogs)
    - [Release notes](#release-notes)
  - [Getting Involved](#getting-involved)
  - [Licensing](#licensing)

## [Requirements](#requirements)

| Name             | Minimum Version |
|------------------|:---------------:|
| ansible          | 2.11.0          |
| ansible-lint     | 5.1.3           |
| jinja2           | 2.11.3          |
| ansible.posix    | 1.0.0           |

## [Collection Structure](#collection-structure)

### [Plugins](#plugins)

 Plugin | Description | Tests |
| --- | --- | --- |

### [Modules](#modules)

 Module | Description | Tests |
| --- | --- | --- |

### [Roles](#roles)

| Role | Description | Tests |
| --- | --- | --- |
| [mto79.desktop.tmux](https://github.com/mto79/ansible_collection_mto79.desktop/roles/tmux/README.md) | Ansible role for setting up tmux on your desktop. |


Click on the role to see the README for that role.

Usage:

```bash
export NEW_ROLE_NAME="new_role"
./add-role.sh ${NEW_ROLE_NAME}
# Or run the script and it will prompt you for the name
```

## [Pre-commit](#pre-commit)

Install pre-commit

```bash
pip install pre-commit
```

Set hooks in .pre-commit-config.yaml

```bash
repos:
- repo: https://github.com/ansible/ansible-lint.git
  rev: v4.2.0
  hooks:
    - id: ansible-lint
      files: \.(yaml|yml)$
```

Enable pre-commit for your git repository

```bash
$ pre-commit install
pre-commit installed at .git/hooks/pre-commit
```

Testing pre-commit

```bash
pre-commit run --all-files
Ansible-lint.............................................................Passed
```

or just type:

```bash
git commit
```

## [Changelogs](#changelogs)

This collection follows [Semantic Versioning](https://semver.org/). More details on versioning can be found [in the Ansible docs](https://docs.ansible.com/ansible/latest/dev_guide/developing_collections.html#collection-versions).

We plan to regularly release new minor or bugfix versions once new features or bugfixes have been implemented.

Releasing the current major version happens from the `devel` branch.

### Generating changelogs

Install antsibull-changelog:

```bash
pip install antsibull-changelog
```

Initialize changelogs for your repository

```bash
antsibull-changelog init <path/to/your/collection>
```

Validate your changelog fragments

```bash
antsibull-changelog lint
```

Generate the changelog for your release

Create an entry of changelog in changelogs/changelog.yaml

Run antsibull-changelog release command (install antsibull tool before)

```bash
antsibull-changelog release --update-existing --version 1.0.0
```

Check changelogs/changelog.yaml file and generated changelog in CHANGELOG.rst and fix if need

Change version in galaxy.yaml file to the new one.

Commit and merge changes in changelog or/and docs

Git tag <version_tag> where <version_tag> is tag of the new version - for example 2.3.4
Push tags to upstream - git push upstream <version_tag>

wait until check and release jobs finish and check in galaxy that new version is uploaded: https://galaxy.ansible.com/containers/podman

### Release notes

See [CHANGELOG.rst](CHANGELOG.rst).

## [Getting Involved](#getting-involved)

See [CONTRIBUTING](CONTRIBUTING.md).

## [Licensing](#licensing)

See [LICENSE](LICENSE).
