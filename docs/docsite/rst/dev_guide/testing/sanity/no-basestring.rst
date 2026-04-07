..
  Copyright (c) The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-or-later
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-or-later.txt

no-basestring
=============

Do not use ``isinstance(s, basestring)`` as basestring has been removed in
Python3.  You can import ``string_types``, ``binary_type``, or ``text_type``
from ``ansible.module_utils.six`` and then use ``isinstance(s, string_types)``
or ``isinstance(s, (binary_type, text_type))`` instead.

If this is part of code to convert a string to a particular type,
``ansible.module_utils.common.text.converters`` contains several functions
that may be even better for you: ``to_text``, ``to_bytes``, and ``to_native``.
