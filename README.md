# Ansible Role: Docker

[![CI](https://github.com/pluggero/ansible-role-docker/actions/workflows/ci.yml/badge.svg)](https://github.com/pluggero/ansible-role-docker/actions/workflows/ci.yml) [![Ansible Galaxy downloads](https://img.shields.io/ansible/role/d/pluggero/docker?label=Galaxy%20downloads&logo=ansible&color=%23096598)](https://galaxy.ansible.com/ui/standalone/roles/pluggero/docker)

An Ansible Role that installs a basic configuration of docker.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

| Variable | Default | Description |
|---|---|---|
| `docker_daemon_json_path` | `/etc/docker/daemon.json` | Path to the Docker daemon config file. |
| `docker_daemon_options` | `{log-opts: {max-size: "10m", max-file: "3"}}` | Dict merged into `daemon.json`. Set to `{}` to opt out. |

Note: requires `docker_service_manage: true` for daemon changes to restart Docker.

## Dependencies

None.

## Example Playbook

```yaml
- hosts: all
  roles:
    - pluggero.docker
```

## License

MIT / BSD

## Author Information

This role was created in 2025 by Robin Plugge.
