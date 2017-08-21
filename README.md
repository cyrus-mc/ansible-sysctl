# Ansible Role : Configure kernel parameters at runtime

An Ansible Role that manages kernel parameters at runtime via sysctl

## Role Variables:

Available variables are listed below, along with the default values (see `defaults/main.yml`):

    sysctl:
      key:
        value:
        state

    ie: sysctl:
          vm.swappiness:
            value: 1
            state: present

## Dependencies

None.

## Example Playbook

    - hosts: kubernetes-nodes
      var_files:
      - vars/main.yaml
      roles:
      - 'sysctl'
