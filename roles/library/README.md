# Ansible Role: Homebrew Brewfile

Load and dump files from ~/Library: plists, library folders, application support folders.

## Requirements

None.

## Role Variables

- `library_mode`: should be one of `"dump"` or `"load"`
- `library_dest_folder` (by default `~/Library`)
- `library_plists_dest_folder` (by default `~/Library/Preferences`)
- `library_appsupport_dest_folder` (by default `~/Library/Application Support`)
- `library_src_folder` (by default `~/Library`)
- `library_plists_src_folder` (by default `~/Library/Preferences`)
- `library_appsupport_src_folder` (by default `~/Library/Application Support`)
- `library_plists_new` in dump mode, paths to new plists to dump
- `library_files_new` in dump mode, paths to new `~/Library` files (usually directories) to dump
- `library_appsupport_new` in dump mode, paths to new `~/Library/Application Support` files (usually directories) to dump

## Example Playbook

    - hosts: localhost
      vars:
        library_mode: load
      roles:
        - lajarre.macstuff.library

## License

[MIT][link-license]

## Author Information

This role was created in 2021 by [A Hajjar](https://github.com/lajarre).
