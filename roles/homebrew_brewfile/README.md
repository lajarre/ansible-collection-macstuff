# Ansible Role: Homebrew Brewfile

Installs Brewfile taps, formulas and cask in a step-by-step fashion.

## Requirements

None.

## Role Variables

[TODO] The following is taken from geerlingguy's homebrew role, but should be adapted.

The path where Homebrew will be installed (`homebrew_prefix` is the parent directory). It is recommended you stick to the default, otherwise Homebrew might have some weird issues. If you change this variable, you should also manually create a symlink back to /usr/local so things work as Homebrew expects.

    homebrew_brew_bin_path: /usr/local/bin

The path where `brew` will be installed.

    ansible_become_password: ""

Set this to your account password if casks you want installed need elevated privileges while installing (like `microsoft-office`), preferably [encrypted via `ansible-vault`][link-vault-doc].

    homebrew_use_brewfile: true

Whether to install via a Brewfile. If so, you will need to install the `homebrew/bundle` tap, which could be done within `homebrew_taps`.

    homebrew_brewfile_dir: '~'

The directory where your Brewfile is located.

## Dependencies

  - [geerlingguy.mac.homebrew](https://galaxy.ansible.com/geerlingguy/mac/)

## Example Playbook

    - hosts: localhost
      vars:
        homebrew_installed_packages:
          - mysql
      roles:
        - lajarre.mac.homebrew

See the `tests/local-testing` directory for an example of running this role over
Ansible's `local` connection. See also:
[Mac Development Ansible Playbook][mac-dev-playbook].

## License

[MIT][link-license]

## Author Information

This role was created in 2021 by [A Hajjar](https://github.com/lajarre) largely based off prior work
by Jeff Geerling.
