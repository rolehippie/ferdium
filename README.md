# ferdium

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&amp;logoColor=white)](https://github.com/rolehippie/ferdium)
[![General Workflow](https://github.com/rolehippie/ferdium/actions/workflows/general.yml/badge.svg)](https://github.com/rolehippie/ferdium/actions/workflows/general.yml)
[![Readme Workflow](https://github.com/rolehippie/ferdium/actions/workflows/readme.yml/badge.svg)](https://github.com/rolehippie/ferdium/actions/workflows/readme.yml)
[![Galaxy Workflow](https://github.com/rolehippie/ferdium/actions/workflows/galaxy.yml/badge.svg)](https://github.com/rolehippie/ferdium/actions/workflows/galaxy.yml)
[![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/ferdium)](https://github.com/rolehippie/ferdium/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/badge/role-rolehippie.ferdium-blue)](https://galaxy.ansible.com/rolehippie/ferdium)

Ansible role to install ferdium multi messenger.

## Sponsor

Building and improving this Ansible role have been sponsored by my current and previous employers like **[Cloudpunks GmbH](https://cloudpunks.de)** and **[Proact Deutschland GmbH](https://www.proact.eu)**.

## Table of content

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [ferdium_arch](#ferdium_arch)
  - [ferdium_package](#ferdium_package)
  - [ferdium_version](#ferdium_version)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.10`


## Default Variables

### ferdium_arch

Architecture for the package

#### Default value

```YAML
ferdium_arch: "{{ 'arm64' if ansible_architecture == 'aarch64' else 'amd64' }}"
```

### ferdium_package

Download URL for the package to install

#### Default value

```YAML
ferdium_package: https://github.com/ferdium/ferdium-app/releases/download/v{{ ferdium_version
  }}/Ferdium-linux-{{ ferdium_version }}-{{ ferdium_arch }}.deb
```

### ferdium_version

Version for the package

#### Default value

```YAML
ferdium_version: 6.4.1
```

## Discovered Tags

**_ferdium_**


## Dependencies

- None

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
