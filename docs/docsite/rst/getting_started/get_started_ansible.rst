..
  Copyright (c) The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-or-later
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-or-later.txt

  source_url: https://github.com/ansible/ansible-documentation/blob/devel/docs/docsite/rst/getting_started/get_started_ansible.rst
  revision: 5c0dd1f520aea2b7a000023841f212fdd06dcd57
  status: ready

.. _get_started_ansible:

**********************************
Comece a automatizar com o Ansible
**********************************

Comece a usar o Ansible criando um projeto de automação, construindo um
inventário e criando um playbook "Olá, Mundo!".

#. Instale o Ansible.

   .. code-block:: bash

     pip install ansible

#. Crie uma pasta para o projeto no seu sistema de arquivos.

   .. code-block:: bash

     mkdir ansible_quickstart && cd ansible_quickstart

  Usar uma estrutura de diretórios única facilita a adição ao controle de
  versão, bem como a reutilização e o compartilhamento de conteúdo de
  automação.

Continue seus primeiros passos com o Ansible
:ref:`construindo um inventário<get_started_inventory>`.

.. seealso::

  :ref:`installation_guide`
    Guia de instalação com instruções para instalar o Ansible em diversos
    sistemas operacionais.
  `Ansible Demos <https://github.com/ansible/product-demos>`_
    Demonstrações de diferentes casos de uso do Ansible.
  `Ansible Labs <https://www.ansible.com/products/ansible-training>`_
    Laboratórios para aprofundar o conhecimento sobre diferentes tópicos.
  :ref:`Guia de Comunicação Ansible<communication>`
    Dúvidas? Ajuda? Ideias? Pergunte à comunidade.
