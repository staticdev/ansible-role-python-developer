# Ansible Role: Python Developer

[![CI](https://github.com/staticdev/ansible-role-python-developer/workflows/CI/badge.svg?event=push)](https://github.com/staticdev/ansible-role-python-developer/actions?query=workflow%3ACI)

This install packages for developing in Python on multiple versions using [Cookiecutter Hypermodern Python](https://github.com/cjolowicz/cookiecutter-hypermodern-python).

## Features

Installs:

- pre-commit
- pipx
- nox
- pyenv
- poetry
- cookiecutter

## Requirements

None.

## Role Variables

Here is the list of all variables and their default values:

- `install_pycharm`: `false`
- `install_vscode`: `false`
- `vscode_extensions`: optional list of name_ids of extensions. eg.: ms-python.python (Python Official Extension)

## Dependencies

- [avanov.pyenv](https://galaxy.ansible.com/avanov/pyenv)
- [oefenweb.pycharm](https://galaxy.ansible.com/oefenweb/pycharm) (optional)
- [ngetchell.vscode](https://galaxy.ansible.com/ngetchell/vscode) (optional)

## Example Playbook

```yaml
# role without IDE
- hosts: all
  roles:
    - role: staticdev.python-developer

# role with pycharm
- hosts: all
  roles:
    - role: staticdev.python-developer
      vars:
        install_pycharm: true

# role with vscode and extensions
- hosts: all
  roles:
    - role: staticdev.python-developer
      vars:
        install_vscode: true
        vscode_extensions:
          - ms-python.python
          - ms-python.vscode-pylance
          - shan.code-settings-sync
```

## License

MIT / BSD

## Author Information

[staticdev](http://github.com/staticdev)
