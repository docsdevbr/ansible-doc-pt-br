..
  SPDX-FileCopyrightText: The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0.txt

empty-init
==========

The ``__init__.py`` files under the following directories must be empty.  For some of these (modules
and tests), ``__init__.py`` files with code won't be used.  For others (module_utils), we want the
possibility of using Python namespaces which an empty ``__init__.py`` will allow for.

- ``lib/ansible/modules/``
- ``lib/ansible/module_utils/``
- ``test/units/``
