..
  SPDX-FileCopyrightText: The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-or-later
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-or-later.txt

obsolete-files
==============

Directories in the Ansible source tree are sometimes made obsolete.
Files should not exist in these directories.
The new location (if any) is dependent on which directory has been made obsolete.

Below are some of the obsolete directories and their new locations:

- All of ``test/runner/`` is now under ``test/lib/ansible_test/`` instead. The organization of files in the new directory has changed.
- Most subdirectories of ``test/sanity/`` (with some exceptions) are now under ``test/lib/ansible_test/_util/controller/sanity/`` instead.

This error occurs most frequently for open pull requests which add or modify files in directories which are now obsolete.
Make sure the branch you are working from is current so that changes can be made in the correct location.
