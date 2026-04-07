..
  Copyright (c) The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-or-later
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-or-later.txt

shebang
=======

Most executable files should only use one of the following shebangs:

- ``#!/bin/sh``
- ``#!/bin/bash -eu``
- ``#!/bin/bash -eux``
- ``#!/usr/bin/make``
- ``#!/usr/bin/env python``
- ``#!/usr/bin/env bash``

This does not apply to Ansible modules, which should not be executable and must always use ``#!/usr/bin/python``.

Some exceptions are permitted. Ask if you have questions.
