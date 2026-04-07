..
  SPDX-FileCopyrightText: The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-or-later
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-or-later.txt

no-main-display
===============

As of Ansible 2.8, ``Display`` should no longer be imported from ``__main__``.

``Display`` is now a singleton and should be utilized like the following:

.. code-block:: python

   from ansible.utils.display import Display
   display = Display()

There is no longer a need to attempt ``from __main__ import display`` inside
a ``try/except`` block.
