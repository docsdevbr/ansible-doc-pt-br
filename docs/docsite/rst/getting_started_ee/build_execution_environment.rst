..
  SPDX-FileCopyrightText: The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-only
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-only.txt

  source_url: https://github.com/ansible/ansible-documentation/blob/devel/docs/docsite/rst/getting_started_ee/build_execution_environment.rst
  revision: f109b783e5704abbdfb52d4e024e5ff45697b19b
  status: ready

.. _building_execution_environment:

*****************************************
Criando seu primeiro Ambiente de Execução
*****************************************

Vamos criar um EE (Execution Environment, ou Ambiente de Execução) que
representa um nó de controle do Ansible contendo pacotes padrão como
``ansible-core`` e Python, além de uma coleção do Ansible
(``community.postgresql``) e sua dependência (o conector Python
``psycopg2-binary``).

Para criar seu primeiro EE:

#. Crie uma pasta de projeto em seu sistema de arquivos.

   .. code-block:: bash

      mkdir my_first_ee && cd my_first_ee

#. Crie um arquivo ``execution-environment.yml`` que especifica as dependências
   a serem incluídas na imagem.

   .. literalinclude:: yaml/execution-environment.yml
      :language: yaml

   .. note::

      O pacote Python `psycopg2-binary` está incluído no arquivo
      `requirements.txt` da coleção.
      Para coleções que não incluem arquivos `requirements.txt`, você precisa
      especificar as dependências do Python explicitamente.
      Consulte a
      `documentação do Ansible Builder <https://ansible-builder.readthedocs.io/en/stable/definition/>`_
      para obter detalhes.

#. Crie uma imagem de contêiner EE chamada ``postgresql_ee``.

   Se você usar o Docker, adicione o argumento ``--container-runtime docker``.

   .. code-block:: bash

      ansible-builder build --tag postgresql_ee

#. Liste as imagens de contêiner para verificar se você a construiu com sucesso.

   .. code-block:: bash

      podman image list

      localhost/postgresql_ee          latest      2e866777269b  6 minutes ago  1.11 GB

Você pode verificar a imagem que criou inspecionando o arquivo ``Containerfile``
ou ``Dockerfile`` no diretório ``context`` para visualizar sua configuração.

.. code-block:: bash

   less context/Containerfile

Você também pode usar o Ansible Navigator para visualizar informações detalhadas
sobre a imagem.

Execute o comando `ansible-navigator`, digite ``:images`` na interface de texto
e selecione ``postgresql_ee``.

Prossiga para :ref:`running_custom_execution_environment` e teste o EE que você
acabou de criar.

.. seealso::

   `Executando um registro de contêineres local para Ambientes de Execução <https://forum.ansible.com/t/running-a-local-container-registry-for-execution-environments/206>`_
      Este guia no fórum da comunidade Ansible explica como configurar um
      registro local para suas imagens de Ambiente de Execução.
