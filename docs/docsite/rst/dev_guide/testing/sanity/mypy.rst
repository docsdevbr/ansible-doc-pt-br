..
  Copyright (c) The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-only
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-only.txt

mypy
====

The ``mypy`` static type checker is used to check the following code against each Python version supported by the control node:

 * ``lib/ansible/``
 * ``test/lib/ansible_test/_internal/``

Additionally, the following code is checked against Python versions supported only on managed nodes:

 * ``lib/ansible/modules/``
 * ``lib/ansible/module_utils/``

See `the mypy documentation <https://mypy.readthedocs.io/en/stable/>`_
