..
  SPDX-FileCopyrightText: The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-only
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-only.txt

  source_url: https://github.com/ansible/ansible-documentation/blob/stable-2.20/docs/docsite/rst/getting_started_ee/index.rst
  revision: 2043e2efa0de69f39edee2829934ca141fd1f254
  status: ready

.. _getting_started_ee_index:

**************************************
Começando com os Ambientes de Execução
**************************************

Você pode executar a automação do Ansible em contêineres, como qualquer outra
aplicação de software moderno.
O Ansible usa imagens de contêiner conhecidas como Execution Environments (EE,
ou Ambientes de Execução) que atuam como nós de controle.
Os EEs simplificam a escalabilidade de projetos de automação e tornam coisas
como operações de implantação muito mais fáceis.

Uma imagem de Ambiente de Execução contém os seguintes pacotes por padrão:

* ``ansible-core``
* ``ansible-runner``
* Python
* Dependências de conteúdo do Ansible

Além dos pacotes padrão, um EE também pode conter:

* uma ou mais coleções do Ansible e suas dependências
* outros componentes personalizados

Este guia de introdução mostra como criar e testar um Ambiente de Execução
simples.
A imagem do contêiner resultante representa um nó de controle do Ansible que
contém:

* pacotes padrão do EE
* a coleção ``community.postgresql``
* o pacote Python ``psycopg2-binary``

.. toctree::
   :maxdepth: 1

   introduction
   setup_environment
   build_execution_environment
   run_execution_environment
   run_community_ee_image
