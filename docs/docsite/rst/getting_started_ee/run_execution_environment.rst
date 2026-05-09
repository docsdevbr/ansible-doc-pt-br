..
  SPDX-FileCopyrightText: The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-only
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-only.txt

  source_url: https://github.com/ansible/ansible-documentation/blob/devel/docs/docsite/rst/getting_started_ee/run_execution_environment.rst
  revision: 5569b25c51289bb67a4d60150c1c281612588fa3
  status: ready

.. _running_custom_execution_environment:

*****************
Executando seu EE
*****************

Você pode executar seu EE (Execution Environment, ou Ambiente de Execução) na
linha de comando contra o ``localhost`` ou um alvo remoto usando o
``ansible-navigator``.

.. note::

   Existem outras ferramentas além do ``ansible-navigator`` com as quais você
   pode executar EEs.

Executar no localhost
=====================

#. Crie um playbook ``test_localhost.yml``.

   .. literalinclude:: yaml/test_localhost.yml
      :language: yaml

#. Execute o playbook dentro do Ambiente de Execução ``postgresql_ee``.

   .. code-block:: bash

      ansible-navigator run test_localhost.yml --execution-environment-image postgresql_ee --mode stdout --pull-policy missing --container-options='--user=0'

Você pode notar que os fatos coletados são referentes ao contêiner e não à
máquina da pessoa desenvolvedora.
Isso ocorre porque o playbook do Ansible foi executado dentro do contêiner.

Executar em um alvo remoto
==========================

Antes de começar, certifique-se de ter o seguinte:

  * Pelo menos um endereço IP ou nome de host resolúvel para um alvo remoto.
  * Credenciais válidas para o host remoto.
  * Um usuário com permissões `sudo` no host remoto.

Execute um playbook dentro do Ambiente de Execução ``postgresql_ee`` em uma
máquina host remota, como no exemplo a seguir:

#. Crie um diretório para arquivos de inventário.

   .. code-block:: bash

      mkdir inventory

#. Crie o arquivo de inventário ``hosts.yml`` no diretório ``inventory``.

   .. literalinclude:: yaml/hosts.yml
      :language: yaml

#. Crie um playbook ``test_remote.yml``.

   .. literalinclude:: yaml/test_remote.yml
      :language: yaml

#. Execute o playbook dentro do EE ``postgresql_ee``.

   Substitua ``student`` pelo nome de usuário apropriado.
   Alguns argumentos no comando podem ser opcionais, dependendo do método de
   autenticação do host de destino.

   .. code-block:: bash

      ansible-navigator run test_remote.yml -i inventory --execution-environment-image postgresql_ee:latest --mode stdout --pull-policy missing --enable-prompts -u student -k -K

.. seealso::

   `Definição do Ambiente de Execução <https://ansible-builder.readthedocs.io/en/stable/definition/>`_
      Fornece informações sobre o arquivo de definição do Ambiente de Execução e
      as opções disponíveis.
   `Uso da CLI do Ansible Builder <https://ansible-builder.readthedocs.io/en/stable/usage/>`_
      Fornece detalhes sobre como usar o Ansible Builder.
   `Documentação do Ansible Navigator <https://ansible-navigator.readthedocs.io/>`_
      Fornece detalhes sobre como usar o Ansible Navigator.
   `Executando um registro de contêineres local para EEs <https://forum.ansible.com/t/running-local-container-registry-for-execution-environments/206>`_
      Este guia no fórum da comunidade Ansible explica como configurar um
      registro local para suas imagens de Ambiente de Execução.
