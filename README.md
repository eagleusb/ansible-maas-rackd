# ansible-maas-rackd

[![contributing][contributing-img]](CONTRIBUTING.md)

1. [Overview](#overview)
1. [Description](#description)
1. [Requirements](#requirements)
1. [Setup](#setup)
1. [Role Variables](#role-variables)
1. [Playbook Example](#playbook-example)
1. [Dependencies](#dependencies)
1. [Limitations](#limitations)
1. [Development](#development)

## Overview

[MAAS](https://maas.io/docs/what-is-maas) is Metal As A Service. It lets you treat physical servers like virtual machines (instances)
in the cloud. Rather than having to manage each server individually, MAAS turns your bare metal
into an elastic cloud-like resource.

## Description

This role install and configure [MAAS Rack Controller](https://maas.io/docs/rack-controller).

## Requirements

## Setup

Use `ansible-galaxy` or download the role in your `roles` directory.

## Role Variables

For now the MAAS Region Controller adress is defined in a dict.
We should leverage hostvars but clear inventory groups are needed for that.

```yaml
maas_regiond:
  api:
    scheme: "http"
    url: "1.2.3.4:5240/MAAS"
    secret: "randomSuperSecretString"
```

## Playbook Example

Use default configuration, means that nothing will be done.

```yaml
- hosts: localhost
  roles:
    - ansible-maas-rackd
```

## Dependencies

None.

## Limitations

So far, this is compatible with Debian and derivatives.

## Development

Please read carefully CONTRIBUTING.md before making a merge request.

[contributing-img]: https://img.shields.io/badge/contributing--grey.svg
