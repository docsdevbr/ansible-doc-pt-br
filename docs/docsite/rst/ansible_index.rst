..
  Copyright (c) The Ansible project contributors.

  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/ansible/ansible-documentation/blob/-/COPYING

  source_url: https://github.com/ansible/ansible-documentation/blob/devel/docs/docsite/rst/ansible_index.rst
  revision: dbae0ce87d8d2a89c6e3cf0651505e39c841b390
  status: ready

.. _ansible_documentation:

..
  Este é o arquivo index do pacote Ansible.
  Ele é vinculado simbolicamente ao index.rst pelo Makefile.

Documentação do Ansible
=======================

Bem-vinda à documentação da comunidade Ansible!
Esta documentação abrange a versão do Ansible indicada no canto superior
esquerdo desta página.
Mantemos diversas versões do Ansible e da documentação, portanto, certifique-se
de usar a versão da documentação que abrange a versão do Ansible que você está
usando.
Para recursos recentes, indicamos a versão do Ansible em que o recurso foi
adicionado.

O Ansible lança uma nova versão principal aproximadamente duas vezes por ano.
A aplicação principal evolui de forma um tanto conservadora, valorizando a
simplicidade no design e na configuração da linguagem.
As pessoas colaboradoras desenvolvem e alteram módulos e plugins, hospedados em
coleções, com muito mais rapidez.

.. toctree::
  :maxdepth: 2
  :caption: Introdução ao Ansible

  getting_started/index
  getting_started_ee/index

.. toctree::
  :maxdepth: 2
  :caption: Instalação, atualização e configuração

  installation_guide/index
  porting_guides/porting_guides

.. toctree::
  :maxdepth: 2
  :caption: Usando o Ansible

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
  :caption: Contribuindo para o Ansible

  community/index
  community/contributions_collections
  community/contributions
  community/advanced_index
  dev_guide/style_guide/index

.. toctree::
  :maxdepth: 2
  :caption: Estendendo o Ansible

  dev_guide/index

.. toctree::
  :glob:
  :maxdepth: 1
  :caption: Cenários comuns do Ansible

  scenario_guides/cloud_guides

.. toctree::
  :maxdepth: 2
  :caption: Automação de rede

  network/getting_started/index
  network/user_guide/index
  network/dev_guide/index

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

  roadmap/ansible_roadmap_index.rst
  roadmap/ansible_core_roadmap_index.rst
