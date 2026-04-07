..
  SPDX-FileCopyrightText: The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-or-later
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-or-later.txt

no-dict-itervalues
==================

The ``dict.itervalues`` method has been removed in Python 3. There are two recommended alternatives:

.. code-block:: python

    for VALUE in DICT.values():
       pass

.. code-block:: python

    from ansible.module_utils.six import itervalues

    for VALUE in itervalues(DICT):
        pass
