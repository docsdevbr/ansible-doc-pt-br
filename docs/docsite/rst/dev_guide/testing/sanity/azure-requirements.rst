..
  Copyright (c) The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-only
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-only.txt

:orphan:

azure-requirements
==================

Update the Azure integration test requirements file when changes are made to the Azure packaging requirements file:

.. code-block:: bash

    cp packaging/requirements/requirements-azure.txt test/lib/ansible_test/_data/requirements/integration.cloud.azure.txt
