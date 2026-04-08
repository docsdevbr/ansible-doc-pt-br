..
  SPDX-FileCopyrightText: The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-only
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-only.txt

:orphan:

no-underscore-variable
======================

In the future, Ansible may use the identifier ``_`` to internationalize its
message strings.  To be ready for that, we need to make sure that there are
no conflicting identifiers defined in the code base.

In common practice, ``_`` is frequently used as a dummy variable (a variable
to receive a value from a function where the value is useless and never used).
In Ansible, we're using the identifier ``dummy`` for this purpose instead.

Example of unfixed code:

.. code-block:: python

    for _ in range(0, retries):
        success = retry_thing()
        if success:
            break

Example of fixed code:

.. code-block:: python

    for dummy in range(0, retries):
        success = retry_thing()
        if success:
            break
