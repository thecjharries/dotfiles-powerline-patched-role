# `dotfiles-powerline-patched-role`

[![Build Status](https://travis-ci.org/thecjharries/dotfiles-powerline-patched-role.svg?branch=master)](https://travis-ci.org/thecjharries/dotfiles-powerline-patched-role)

## Requirements

Fedora 27 is recommended.

## Role Variables

Defaults are below.

```yml
---
owning_user: "{{ ansible_user }}"
owning_group: "{{ ansible_user }}"
root_dir: "/home/{{ ansible_user }}"
config_dir: "{{ root_dir }}/.config"

powerline_font_src_path: /opt/powerline-fonts

local_font_cache: "{{ root_dir }}/.local/share/fonts"

local_fontconfig: "{{ config_dir }}/fontconfig/conf.d"
```

## Dependencies

```yml
---
- src: git+https://github.com/thecjharries/dotfiles-common-software-role.git
- src: git+https://github.com/thecjharries/dotfiles-package-installer-role.git
- src: git+https://github.com/thecjharries/dotfiles-git-role.git
- src: git+https://github.com/thecjharries/dotfiles-repo-installer-role.git
```

## Example Playbook

```yml
---
- hosts: all

  roles:
    - role: dotfiles-powerline-patched-role
```

## License

ISC
