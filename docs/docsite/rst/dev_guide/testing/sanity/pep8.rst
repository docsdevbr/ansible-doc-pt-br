..
  SPDX-FileCopyrightText: The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-only
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-only.txt

.. _testing_pep8:

pep8
====

Python static analysis for PEP 8 style guideline compliance.

`PEP 8`_ style guidelines are enforced by `pycodestyle`_ on all python files in the repository by default.

Running locally
-----------------

The `PEP 8`_ check can be run locally as follows:

.. code-block:: shell

    ansible-test sanity --test pep8 [file-or-directory-path-to-check] ...



.. _PEP 8: https://www.python.org/dev/peps/pep-0008/
.. _pycodestyle: https://pypi.org/project/pycodestyle/


