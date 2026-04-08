..
  Copyright (c) The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-only
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-only.txt

.. _testing_compile:

compile
=======

All Python source files must successfully compile using all supported Python versions.

.. note::

   The list of supported Python versions is dependent on the version of ``ansible-core`` that you are using.
   Make sure you consult the version of the documentation which matches your ``ansible-core`` version.
   You can find an overview for this and previous versions in :ref:`ansible_core_support_matrix`.

Control node code, including plugins in Ansible Collections, must support the following Python versions:

- 3.14
- 3.13
- 3.12

Code which runs on targets (``modules`` and ``module_utils``) must support all control node supported Python versions,
as well as the additional Python versions supported only on targets:

- 3.14
- 3.13
- 3.12
- 3.11
- 3.10
- 3.9

.. note::

   Ansible Collections can be
   `configured <https://github.com/ansible/ansible/blob/devel/test/lib/ansible_test/config/config.yml>`_
   to support a subset of the target-only Python versions.
