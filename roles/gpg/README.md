# Ansible Role: Homebrew Brewfile

Load and dump gpg key ring.

## Requirements

None.

## Role Variables

- `gpg_mode`: should be one of `"dump"` or `"load"`

## Example Playbook

    - hosts: localhost
      vars:
        gpg_mode: load
      roles:
        - lajarre.macstuff.gpg

## License

[MIT][link-license]

## Author Information

This role was created in 2021 by [A Hajjar](https://github.com/lajarre).
