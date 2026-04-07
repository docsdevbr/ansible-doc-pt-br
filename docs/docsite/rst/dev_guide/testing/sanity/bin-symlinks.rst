..
  Copyright (c) The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-or-later
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-or-later.txt

bin-symlinks
============

The ``bin/`` directory in Ansible must contain only symbolic links to executable files.
These files must reside in the ``lib/ansible/`` or ``test/lib/ansible_test/`` directories.

This is required to allow ``ansible-test`` to work with containers and remote hosts when running from an installed version of Ansible.

Symlinks for each entry point in ``bin/`` must also be present in ``test/lib/ansible_test/_util/target/injector/``.
Each symlink should point to the ``python.py`` script in the same directory.
This facilitates running with the correct Python interpreter and enabling code coverage.
