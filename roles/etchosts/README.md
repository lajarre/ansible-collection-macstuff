# Ansible Role: Homebrew Brewfile

Load and dump /etc/hosts.

## Requirements

None.

## Role Variables

- `etchosts_mode`: should be one of `"dump"` or `"load"`

## Example Playbook

    - hosts: localhost
      vars:
        etchosts_mode: load
      roles:
        - lajarre.macstuff.etchosts

## License

[MIT][link-license]

## Author Information

This role was created in 2021 by [A Hajjar](https://github.com/lajarre).
