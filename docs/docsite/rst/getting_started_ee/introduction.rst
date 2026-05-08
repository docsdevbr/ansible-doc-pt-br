..
  SPDX-FileCopyrightText: The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-only
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-only.txt

  source_url: https://github.com/ansible/ansible-documentation/blob/stable-2.20/docs/docsite/rst/getting_started_ee/introduction.rst
  revision: 2043e2efa0de69f39edee2829934ca141fd1f254
  status: ready

.. _introduction_execution_environment:

************************************
Introdução aos Ambientes de Execução
************************************

Os Execution Environments (EE, ou Ambientes de Execução) do Ansible visam
resolver problemas de complexidade e proporcionar todos os benefícios que você
pode obter com a conteinerização.

Reduzindo a complexidade
========================

Existem três áreas principais onde os EEs podem reduzir a complexidade:

* dependências de software
* portabilidade
* separação de conteúdo

Dependências
------------

As aplicações de software normalmente têm dependências, e o Ansible não é
exceção.
Essas dependências podem incluir bibliotecas de software, arquivos de
configuração ou outros serviços, entre outros.

Tradicionalmente, as pessoas administradoras instalam as dependências da
aplicação no sistema operacional usando ferramentas de gerenciamento de pacotes,
como RPM ou Python-pip.
A principal desvantagem dessa abordagem é que uma aplicação pode exigir versões
de dependências diferentes das fornecidas por padrão.
Para o Ansible, uma instalação típica consiste no `ansible-core` e um conjunto
de coleções do Ansible.
Muitas delas têm dependências para os plugins, módulos, funções e playbooks que
fornecem.

As coleções do Ansible podem depender dos seguintes softwares e suas versões:

* ``ansible-core``
* Python
* Pacotes Python
* Pacotes do sistema
* Outras coleções do Ansible

As dependências precisam ser instaladas e, às vezes, podem entrar em conflito
entre si.

Uma maneira de resolver **parcialmente** o problema de dependência é usar
ambientes virtuais Python nos nós de controle do Ansible.
No entanto, quando aplicados ao Ansible, os ambientes virtuais têm desvantagens
e limitações inerentes.

Portabilidade
-------------

Uma pessoa usuária do Ansible escreve conteúdo para o Ansible localmente e
deseja aproveitar a tecnologia de contêineres para tornar seus ambientes de
automação portáteis, compartilháveis e facilmente implantáveis em ambientes de
teste e produção.

Separação de conteúdo
---------------------

Em situações em que um nó de controle Ansible ou uma ferramenta como o Ansible
AWX/Controller é utilizada por várias pessoas usuárias, elas podem querer
separar seu conteúdo para evitar conflitos de configuração e dependência.

Ferramentas Ansible para EEs
============================

Projetos no ecossistema Ansible também fornecem diversas ferramentas que você
pode usar com Ambientes de Execução, como:

* `Ansible Builder <https://ansible-builder.readthedocs.io/en/stable/>`_
* `Ansible Navigator <https://ansible-navigator.readthedocs.io/>`_
* `Ansible AWX <https://ansible.readthedocs.io/projects/awx/en/latest/userguide/execution_environments.html#use-an-execution-environment-in-jobs>`_
* `Ansible Runner <https://ansible-runner.readthedocs.io/en/stable/>`_
* `VS Code Ansible <https://marketplace.visualstudio.com/items?itemName=redhat.ansible>`_
* `Extensões de contêineres de desenvolvimento <https://code.visualstudio.com/docs/devcontainers/containers>`_

Quer começar a usar EEs? Consulte :ref:`setting_up_ee_environment`.
