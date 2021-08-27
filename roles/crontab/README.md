# Ansible Role: Homebrew Brewfile

Load and dump crontab.

## Requirements

None.

## Role Variables

- `crontab_mode`: should be one of `"dump"` or `"load"`

## Example Playbook

    - hosts: localhost
      vars:
        crontab_mode: load
      roles:
        - lajarre.macstuff.crontab

## License

[MIT][link-license]

## Author Information

This role was created in 2021 by [A Hajjar](https://github.com/lajarre).
