..
  SPDX-FileCopyrightText: The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-only
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-only.txt

  source_url: https://github.com/ansible/ansible-documentation/blob/devel/docs/docsite/rst/getting_started_ee/run_community_ee_image.rst
  revision: 2043e2efa0de69f39edee2829934ca141fd1f254
  status: ready

.. _running_community_execution_environment:

**************************************************
Executando o Ansible com a imagem EE da comunidade
**************************************************

Você pode executar o Ansible sem precisar criar uma EE personalizada usando
imagens da comunidade.

Use a imagem ``community-ee-minimal``, que inclui apenas o ``ansible-core``, ou
a imagem ``community-ee-base``, que também inclui diversas coleções básicas.
Execute o seguinte comando para ver as coleções incluídas na imagem
``community-ee-base``:

.. code-block:: bash

   ansible-navigator collections --execution-environment-image ghcr.io/ansible-community/community-ee-base:latest

Execute o seguinte comando Ansible ad-hoc no localhost dentro do contêiner
``community-ee-minimal``:

.. code-block:: bash

   ansible-navigator exec "ansible localhost -m setup" --execution-environment-image ghcr.io/ansible-community/community-ee-minimal:latest --mode stdout

Agora, crie um playbook de teste simples e execute-o em ``localhost`` dentro do
contêiner:

.. literalinclude:: yaml/test_localhost.yml
   :language: yaml

.. code-block:: bash

   ansible-navigator run test_localhost.yml --execution-environment-image ghcr.io/ansible-community/community-ee-minimal:latest --mode stdout

.. seealso::

   * :ref:`building_execution_environment`
   * :ref:`running_custom_execution_environment`
   * `Documentação do Ansible Navigator <https://ansible-navigator.readthedocs.io/>`_
