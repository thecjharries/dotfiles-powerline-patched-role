# `dotfiles-role-powerline-patched`
# `dotfiles-role-powerline-patched`

[![Build Status](https://travis-ci.org/thecjharries/dotfiles-role-powerline-patched.svg?branch=master)](https://travis-ci.org/thecjharries/dotfiles-role-powerline-patched)
[![Build Status](https://travis-ci.org/thecjharries/dotfiles-role-powerline-patched.svg?branch=master)](https://travis-ci.org/thecjharries/dotfiles-role-powerline-patched)

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
- src: git+https://github.com/thecjharries/dotfiles-role-common-software.git
- src: git+https://github.com/thecjharries/dotfiles-role-common-software.git
- src: git+https://github.com/thecjharries/dotfiles-role-package-installer.git
- src: git+https://github.com/thecjharries/dotfiles-role-package-installer.git
- src: git+https://github.com/thecjharries/dotfiles-role-git.git
- src: git+https://github.com/thecjharries/dotfiles-role-git.git
- src: git+https://github.com/thecjharries/dotfiles-role-repo-installer.git
- src: git+https://github.com/thecjharries/dotfiles-role-repo-installer.git
```

## Example Playbook

```yml
---
- hosts: all

  roles:
    - role: dotfiles-role-powerline-patched
    - role: dotfiles-role-powerline-patched
```

## License

ISC
