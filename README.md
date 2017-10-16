# Ansible sudo role

This is an [Ansible](http://www.ansible.com) role to setup tftpd.

## Requirements

- Ansible >= 2.4

## Role Variables

A list of all the default variables for this role is available in `defaults/main.yml`.

## Dependencies

- xinetd_service role.

## Example Playbook

This is an example playbook:

```yaml
---

- hosts: all
  roles:
    - tftpd
```

## Testing

Test are based on docker containers. You can run the tests with the following commands:

```shell
$ cd tfptd/test
$ ansible-playbook main.yml
```

If you have docker engine configured you can avoid running dependant 'docker_engine' role (that usually requries root privileges) with the following commands:

```shell
$ cd tfptd/test
$ ansible-playbook --skip-tags "role::docker_engine" main.yml
```

## License

Not defined.

## Author Information

- Juan Antonio Valiño García ([juanval@edu.xunta.es](mailto:juanval@edu.xunta.es)). Amtega - Xunta de Galicia
- This role is based on [bertvv.tftp](https://galaxy.ansible.com/bertvv/tftp).
