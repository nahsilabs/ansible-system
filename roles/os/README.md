# os

Setup Ubuntu server.

## Role Variables

#### `os_docker_config`

- docker configuration file (see
  [docs](https://docs.docker.com/engine/reference/commandline/dockerd/#daemon-configuration-file))
- type: map

#### `os_groups`

- groups to create, see group module
  [doc](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/group_module.html)
  for options
- type: list of maps

#### `os_users`

- users to create, see users module
  [doc](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/user_module.html)
  for options. Users previously created with this role and no longer present in
  `os_users` will be deleted automaticaly
- type: list of maps

#### `os_packages`

- list of apt packages to install
- type: list

#### `os_sysctl`

- `/proc/sys` values with sysctl
- type: list of maps

#### `os_limits`

- manage `limits.conf`
- type: list of maps

## Tags

- `sysctl` configure sysctl entries
- `limits` manage `/etc/security/limits.conf`
- `users` - manage users and groups
- `packages` install packages
- `docker` - configure docker

## Author

- **Anatolios Laskaris** - [nahsi](https://github.com/nahsi)
