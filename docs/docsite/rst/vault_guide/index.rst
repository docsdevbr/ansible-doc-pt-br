..
  SPDX-FileCopyrightText: The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-or-later
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-or-later.txt

.. _vault_guide_index:

############################################
Protecting sensitive data with Ansible vault
############################################

.. note::

    **Making Open Source More Inclusive**

    Red Hat is committed to replacing problematic language in our code, documentation, and web properties. We are beginning with these four terms: master, slave, blacklist, and whitelist. We ask that you open an issue or pull request if you come upon a term that we have missed. For more details, see `our CTO Chris Wright's message <https://www.redhat.com/en/blog/making-open-source-more-inclusive-eradicating-problematic-language>`_.

Welcome to the Ansible vault documentation.
Ansible vault provides a way to encrypt and manage sensitive data such as passwords.
This guide introduces you to Ansible vault and covers the following topics:

* Managing vault passwords.
* Encrypting content and files with Ansible vault.
* Using encrypted variables and files.

.. toctree::
   :maxdepth: 2

   vault
   vault_managing_passwords
   vault_encrypting_content
   vault_using_encrypted_content
