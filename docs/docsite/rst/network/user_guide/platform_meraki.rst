..
  Copyright (c) The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-only
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-only.txt

.. _meraki_platform_options:

***************************************
Meraki Platform Options
***************************************

The `cisco.meraki <https://galaxy.ansible.com/ui/repo/published/cisco/meraki>`_ collection only supports the ``local`` connection type at this time.

.. contents::
  :local:

Connections available
================================================================================

.. table::
    :class: documentation-table

    ====================  ==========================================
    ..                    Dashboard API
    ====================  ==========================================
    Protocol              HTTP(S)

    Credentials           uses API key from Dashboard

    Connection Settings   ``ansible_connection: localhost``

    Returned Data Format  ``data.``
    ====================  ==========================================


Example Meraki task
-------------------

.. code-block:: yaml

  cisco.meraki.meraki_organization:
    auth_key: abc12345
    org_name: YourOrg
    state: present
  delegate_to: localhost

.. seealso::

         :ref:`timeout_options`
