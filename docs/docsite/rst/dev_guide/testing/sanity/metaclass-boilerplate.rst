..
  SPDX-FileCopyrightText: The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-only
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-only.txt

:orphan:

metaclass-boilerplate
=====================

Most Python files should include the following boilerplate at the top of the file, right after the
comment header and ``from __future__ import``:

.. code-block:: python

    __metaclass__ = type


Python 2 has "new-style classes" and "old-style classes" whereas Python 3 only has new-style classes.
Adding the ``__metaclass__ = type`` boilerplate makes every class defined in that file into
a new-style class as well.

.. code-block:: python

    from __future__ import absolute_import, division, print_function
    __metaclass__ = type

    class Foo:
        # This is a new-style class even on Python 2 because of the __metaclass__
        pass
