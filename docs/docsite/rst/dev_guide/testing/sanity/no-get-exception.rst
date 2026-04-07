..
  Copyright (c) The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-or-later
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-or-later.txt

no-get-exception
================

We created a function, ``ansible.module_utils.pycompat24.get_exception`` to
help retrieve exceptions in a manner compatible with Python 2.4 through
Python 3.6.  We no longer support Python 2.4 and Python 2.5 so this is
extraneous and we want to deprecate the function.  Porting code should look
something like this:

.. code-block:: python

    # Unfixed code:
    try:
        raise IOError('test')
    except IOError:
        e = get_exception()
        do_something(e)
    except:
        e = get_exception()
        do_something_else(e)

    # After fixing:
    try:
        raise IOError('test')
    except IOErrors as e:
        do_something(e)
    except Exception as e:
        do_something_else(e)
