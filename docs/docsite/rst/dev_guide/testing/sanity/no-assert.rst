..
  SPDX-FileCopyrightText: The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-or-later
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-or-later.txt

no-assert
=========

Do not use ``assert`` in production Ansible python code. When running Python
with optimizations, Python will remove ``assert`` statements, potentially
allowing for unexpected behavior throughout the Ansible code base.

Instead of using ``assert`` you should utilize simple ``if`` statements,
that result in raising an exception. There is a new exception called
``AnsibleAssertionError`` that inherits from ``AnsibleError`` and
``AssertionError``. When possible, utilize a more specific exception
than ``AnsibleAssertionError``.

Modules will not have access to ``AnsibleAssertionError`` and should instead
raise ``AssertionError``, a more specific exception, or just use
``module.fail_json`` at the failure point.
