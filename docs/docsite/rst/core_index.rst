..
  Copyright (c) The Ansible project contributors.

  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/ansible/ansible-documentation/blob/-/COPYING

  source_url: https://github.com/ansible/ansible-documentation/blob/stable-2.20/docs/docsite/rst/core_index.rst
  revision: 0bc0a653c5b6af0e5452d4be8ac28d5d186e789d
  status: ready

.. _ansible_core_documentation:

..
  Este é o arquivo index para o ansible-core.
  Ele é vinculado simbolicamente ao index.rst pelo Makefile.

****************************
Documentação do Ansible Core
****************************

O Ansible Core, ou ``ansible-core``, é o principal bloco de construção e
arquitetura do Ansible e inclui:

* Ferramentas de CLI, como ``ansible-playbook``, ``ansible-doc`` e outras para
  conduzir e interagir com a automação;
* A linguagem Ansible que usa YAML para criar um conjunto de regras para o
  desenvolvimento de playbooks Ansible e inclui funções como condicionais,
  blocos, inclusões, laços e outros imperativos do Ansible;
* Um framework arquitetural que permite extensões por meio de coleções do
  Ansible.

Esta documentação abrange a versão do ``ansible-core`` indicada no canto
superior esquerdo desta página.
Mantemos várias versões do ``ansible-core`` e da documentação, portanto,
certifique-se de usar a versão da documentação que abrange a versão do Ansible
que você está usando.
Para recursos recentes, indicamos a versão do Ansible em que o recurso foi
adicionado.

O ``ansible-core`` lança uma nova versão principal aproximadamente duas vezes
por ano.
A aplicação principal evolui de forma um tanto conservadora, valorizando a
simplicidade no design e na configuração da linguagem.
As pessoas colaboradores desenvolvem e alteram módulos e plugins, hospedados em
coleções, com muito mais rapidez.

.. toctree::
  :maxdepth: 2
  :caption: Introdução ao Ansible

  getting_started/index

.. toctree::
  :maxdepth: 2
  :caption: Instalação, atualização e configuração

  installation_guide/index
  porting_guides/core_porting_guides

.. toctree::
  :maxdepth: 2
  :caption: Usando o Ansible Core

  inventory_guide/index
  command_guide/index
  playbook_guide/index
  vault_guide/index
  module_plugin_guide/index
  collections_guide/index
  os_guide/index
  tips_tricks/index

.. toctree::
  :maxdepth: 2
  :caption: Contribuindo para o Ansible Core

  community/index
  community/contributions
  community/advanced_index
  dev_guide/style_guide/index

.. toctree::
  :maxdepth: 2
  :caption: Estendendo o Ansible

  dev_guide/index

.. toctree::
  :maxdepth: 2
  :caption: Ansible Galaxy

  galaxy/user_guide.rst
  galaxy/dev_guide.rst

.. toctree::
  :maxdepth: 1
  :caption: Referências e apêndices

  collections/index
  collections/all_plugins
  reference_appendices/playbooks_keywords
  reference_appendices/common_return_values
  reference_appendices/config
  reference_appendices/general_precedence
  reference_appendices/YAMLSyntax
  reference_appendices/python_3_support
  reference_appendices/interpreter_discovery
  reference_appendices/release_and_maintenance
  reference_appendices/test_strategies
  dev_guide/testing/sanity/index
  reference_appendices/faq
  reference_appendices/glossary
  reference_appendices/module_utils
  reference_appendices/special_variables
  reference_appendices/tower
  reference_appendices/automationhub
  reference_appendices/logging

.. toctree::
  :maxdepth: 2
  :caption: Roadmaps

  roadmap/ansible_core_roadmap_index.rst
