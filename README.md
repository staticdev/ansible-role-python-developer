# Ansible role: Python developer

[![Tests](https://github.com/staticdev/ansible-role-python-developer/workflows/Tests/badge.svg)][tests]

**DEPRECATED: this project is not maintained anymore in favor of [Nixpkgs](https://github.com/NixOS/nixpkgs), [Devenv](https://devenv.sh/) and [linux-workstation-playbook](https://github.com/staticdev/linux-workstation-playbook).**

[tests]: https://github.com/staticdev/ansible-role-python-developer/actions?workflow=Tests

Ansible role to install packages for developing in Python using [Cookiecutter Hypermodern Python].

## Features

Installs:

- [Cookiecutter]
- [Hatch]
- [Nox]
- [Pipx]
- [Poetry]
- [pre-commit]
- [Tox]

Note: for a playbook that installs IDEs, try [Linux workstation playbook].

## Requirements

- [pyenv] (can be installed with [staticdev.pyenv])

## Example Playbook

Here are some common usages of this role.

1. Role using defaults:

```yaml
- hosts: all
  roles:
    - role: staticdev.python-developer
```

2. Role defining Python versions:

```yaml
- hosts: all
  roles:
    - role: staticdev.pyenv
    - role: staticdev.python-developer
```

## License

Distributed under the terms of the [MIT] license,
_Ansible role Python developer_ is free and open source software.

## Author Information

[staticdev]

[cookiecutter]: https://github.com/audreyr/cookiecutter
[cookiecutter hypermodern python]: https://github.com/cjolowicz/cookiecutter-hypermodern-python
[hatch]: https://hatch.pypa.io
[linux workstation playbook]: https://github.com/staticdev/linux-workstation-playbook
[mit]: https://opensource.org/licenses/MIT
[nox]: https://nox.thea.codes/
[pipx]: https://pypa.github.io/pipx/
[poetry]: https://python-poetry.org/
[pre-commit]: https://pre-commit.com/
[pyenv]: https://github.com/pyenv/pyenv
[staticdev]: https://github.com/staticdev
[staticdev.pyenv]: https://galaxy.ansible.com/staticdev/pyenv
[tox]: https://tox.wiki/en/latest/
