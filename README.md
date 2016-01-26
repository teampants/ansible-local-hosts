# ansible-local-hosts
Adds hosts to local /etc/hosts file

## Adding hosts to /etc/hosts on your local workstastion
To add the created host(s) to your local /etc/hosts set ~add_to_local_etc_hosts~ to true.

**Warning: You must set serial=1 on the play that includes this role to use this feature, due to concurrency issues when
editing files. This requirement will go away in the future. See https://github.com/ansible/ansible-modules-core/pull/1902**

## Example Playbook

~~~
- hosts: local-vagrant
  serial: 1
  sudo: yes
  roles:
    - role: teampants.local-hosts
~~~
