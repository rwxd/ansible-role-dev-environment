ansbible-role-dev-environment
=========

Setups needed things

Requirements
------------

Ansible would be nice.

Role Variables
--------------

```yaml
update: true
packages: true
dotfiles: true
zsh: true
tmux: true
pacman_packages: []
aur_packages: []
snap_packages: []
flatpak_packages: []
```

Dependencies
------------

```yaml
collections:
  - community.general
  - kewlfft.aur
```

Example Playbook
----------------

```yaml
- name: Apply dev-environment
  hosts: localhost

  tasks:
    - name: Apply dev-environment role
      include_role:
        name: ansible-role-dev-environment
      vars:
        update: true
        packages: true
        dotfiles: true
        zsh: true
        tmux: true
        pacman_packages:
          - stow
          - git
          - zsh
          - tmux
          - vim
          - neovim
        aur_packages: []
        flatpak_packages:
         - md.obsidian.Obsidian
```
