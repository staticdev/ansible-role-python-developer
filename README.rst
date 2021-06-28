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


Requirements
------------

None.


Role Variables
--------------

Here is the list of all variables and their default values:

- `install_pycharm`: `false`
- `pycharm_flavor`: `community`. You can use also `professional` or `edu`
- `pycharm_version`: `2021.1.2`
- `install_vscode`: `false`
- `vscode_extensions`: optional list of name_ids of extensions. eg.: ms-python.python (Python Official Extension)
- `pyenv_global`: optional Python global version for pyenv (from `staticdev.pyenv`_)
- `pyenv_python_versions`: optional list of Python versions installed (from `staticdev.pyenv`_)


Dependencies
------------

- `staticdev.pyenv`_
- `gantsign.visual-studio-code`_ (optional)


Example Playbook
----------------

.. code:: yaml

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
            pycharm_flavor: edu

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

    # role with pyenv attributes
    - hosts: all
      roles:
        - role: staticdev.python-developer
          vars:
            pyenv_global: "3.9.6"
            vscode_extensions:
              - "3.9.6"
              - "3.8.11"


License
-------

MIT


Author Information
------------------

`staticdev`_

.. _Cookiecutter Hypermodern Python: https://github.com/cjolowicz/cookiecutter-hypermodern-python
.. _gantsign.visual-studio-code: https://galaxy.ansible.com/gantsign/visual-studio-code
.. _staticdev: https://github.com/staticdev
.. _staticdev.pyenv: https://galaxy.ansible.com/staticdev/pyenv
