# Ansible Role: Python Developer

[![CI](https://github.com/staticdev/ansible-role-python-developer/workflows/CI/badge.svg?event=push)](https://github.com/staticdev/ansible-role-python-developer/actions?query=workflow%3ACI)

This install packages for developing in Python on multiple versions for people using [Cookiecutter Hypermodern Python](https://github.com/cjolowicz/cookiecutter-hypermodern-python).

## Requirements

None.

## Role Variables

None.

## Dependencies

- [avanov.pyenv](https://galaxy.ansible.com/avanov/pyenv)

## Example Playbook

```yaml
- hosts: all
  roles:
    - role: staticdev.python-developer
```

## License

MIT / BSD

## Author Information

[staticdev](http://github.com/staticdev)
