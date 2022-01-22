Ansible role: Python developer
==============================

|pre-commit| |Tests|

.. |pre-commit| image:: https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white
   :target: https://github.com/pre-commit/pre-commit
   :alt: pre-commit
.. |Tests| image:: https://github.com/staticdev/ansible-role-python-developer/workflows/Tests/badge.svg
   :target: https://github.com/staticdev/ansible-role-python-developer/actions?workflow=Tests
   :alt: Tests

Ansible role to install packages for developing in Python using `Cookiecutter Hypermodern Python`_.


Features
--------

Installs:

- Cookiecutter_
- Nox_
- Pipx_
- Poetry_
- pre-commit_
- pyenv_


Note:

This role does not install PyCharm_ and `Visual Studio Code`_ anymore. For a playbook that installs IDEs, try `Linux workstation playbook`_.

Requirements
------------

None.


Role Variables
--------------

Here is the list of all variables and their default values:

- `pyenv_global`: optional list of Python global versions for pyenv (from `staticdev.pyenv`_)
- `pyenv_python_versions`: optional list of Python versions installed (from `staticdev.pyenv`_)


Dependencies
------------

- `staticdev.pyenv`_


Example Playbook
----------------

Here are some common usages of this role.

1. Role using defaults:

.. code:: yaml

    - hosts: all
      roles:
        - role: staticdev.python-developer

2. Role defining Python versions:

.. code:: yaml

    - hosts: all
      roles:
        - role: staticdev.python-developer
          vars:
            pyenv_global:
              - "3.10.0"
            pyenv_python_versions:
              - "3.10.0"
              - "3.9.9"


Contributing
------------

Contributions are very welcome.
To learn more, see the `Contributor Guide`_.


License
-------

Distributed under the terms of the MIT_ license,
*Ansible role Python developer* is free and open source software.


Author Information
------------------

`staticdev`_


.. _Contributor Guide: CONTRIBUTING.rst
.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _Cookiecutter Hypermodern Python: https://github.com/cjolowicz/cookiecutter-hypermodern-python
.. _Linux workstation playbook: https://github.com/staticdev/linux-workstation-playbook
.. _Nox: https://nox.thea.codes/
.. _Pipx: https://pypa.github.io/pipx/
.. _Poetry: https://python-poetry.org/
.. _gantsign.visual-studio-code: https://galaxy.ansible.com/gantsign/visual-studio-code
.. _pre-commit: https://pre-commit.com/
.. _PyCharm: https://www.jetbrains.com/pycharm/
.. _pyenv: https://github.com/pyenv/pyenv
.. _staticdev: https://github.com/staticdev
.. _staticdev.pyenv: https://galaxy.ansible.com/staticdev/pyenv
.. _MIT: https://opensource.org/licenses/MIT
.. _Visual Studio Code: https://code.visualstudio.com/
