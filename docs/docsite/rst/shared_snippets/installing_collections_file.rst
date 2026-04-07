..
  SPDX-FileCopyrightText: The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-or-later
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-or-later.txt

Ansible can also install from a source directory in several ways:

.. code-block:: yaml

    collections:
      # directory containing the collection
      - name: ./my_namespace/my_collection/
        type: dir

      # directory containing a namespace, with collections as subdirectories
      - name: ./my_namespace/
        type: subdirs

Ansible can also install a collection collected with ``ansible-galaxy collection build`` or downloaded from Galaxy for offline use by specifying the output file directly:

.. code-block:: yaml

    collections:
      - name: /tmp/my_namespace-my_collection-1.0.0.tar.gz
        type: file

.. note::

    Relative paths are calculated from the current working directory (where you are invoking ``ansible-galaxy install -r`` from). They are not taken relative to the ``requirements.yml`` file.
