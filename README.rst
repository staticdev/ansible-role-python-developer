Ansible role: Python developer
==============================

|Status| |Tests|

.. |Status| image:: https://badgen.net/badge/status/beta/orange
   :target: https://badgen.net/badge/status/beta/orange
   :alt: Project Status
.. |Tests| image:: https://github.com/staticdev/ansible-role-python-developer/workflows/Tests/badge.svg
   :target: https://github.com/staticdev/ansible-role-python-developer/actions?workflow=Tests
   :alt: Tests

Ansible role to install packages for developing in Python using `Cookiecutter Hypermodern Python`_.


Features
--------

Installs:

- pre-commit
- pipx
- nox
- pyenv
- poetry
- cookiecutter
- pycharm (optional)
- vscode (optional)


Requirements
------------

None.


Role Variables
--------------

Here is the list of all variables and their default values:

- `pyenv_global`: optional list of Python global versions for pyenv (from `staticdev.pyenv`_)
- `pyenv_python_versions`: optional list of Python versions installed (from `staticdev.pyenv`_)
- `install_pycharm`: `false`
- `pycharm_flavor`: `community`. You can use also `professional` or `edu`
- `pycharm_version`: `2021.1.2`
- `install_vscode`: `false`
- `vscode_extensions`: optional list of name_ids of extensions. eg.: ms-python.python (Python Official Extension)


Dependencies
------------

- `staticdev.pyenv`_
- `gantsign.visual-studio-code`_ (optional)


Example Playbook
----------------

Here are some common usages of this role.

1. Role without IDE:

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
              - "3.9.6"
            pyenv_python_versions:
              - "3.9.6"
              - "3.8.11"

3. Role with Pycharm

.. code:: yaml

    - hosts: all
      roles:
        - role: staticdev.python-developer
          vars:
            install_pycharm: true
            pycharm_flavor: edu

4. Role with vscode and extensions

.. code:: yaml

    - hosts: all
      roles:
        - role: staticdev.python-developer
          vars:
            install_vscode: true
            vscode_extensions:
              - ms-python.python
              - ms-python.vscode-pylance
              - shan.code-settings-sync


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

.. _Cookiecutter Hypermodern Python: https://github.com/cjolowicz/cookiecutter-hypermodern-python
.. _gantsign.visual-studio-code: https://galaxy.ansible.com/gantsign/visual-studio-code
.. _staticdev: https://github.com/staticdev
.. _staticdev.pyenv: https://galaxy.ansible.com/staticdev/pyenv
