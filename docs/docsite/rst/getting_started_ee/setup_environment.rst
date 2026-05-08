..
  SPDX-FileCopyrightText: The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-only
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-only.txt

  source_url: https://github.com/ansible/ansible-documentation/blob/devel/docs/docsite/rst/getting_started_ee/setup_environment.rst
  revision: 770c89ce55c64502b471f2e6ec34939de238ec8c
  status: ready

.. _setting_up_ee_environment:

*************************
Configurando seu ambiente
*************************

Siga os passos abaixo para configurar um ambiente local para seu primeiro
Execution Environment (EE, ou Ambiente de Execução):

#. Certifique-se de que os seguintes pacotes estejam instalados em seu sistema:

    * ``podman`` ou ``docker``
    * ``python3``
    * ``python3-pip``

    Se você utiliza o gerenciador de pacotes DNF, instale os pré-requisitos da
    seguinte forma:

    .. code-block:: bash

       sudo dnf install -y podman python3 python3-pip

#. Instale o ``ansible-navigator``:

    .. code-block:: bash

       pip3 install ansible-navigator

    A instalação do ``ansible-navigator`` permite executar EEs na linha de
    comando.
    Ele inclui o pacote ``ansible-builder`` para compilar EEs.

    Se você quiser compilar EEs sem realizar testes, instale apenas o
    ``ansible-builder``:

    .. code-block:: bash

       pip3 install ansible-builder

#. Verifique seu ambiente com os seguintes comandos:

    .. code-block:: bash

       ansible-navigator --version
       ansible-builder --version

Pronta para criar um EE em poucos passos?
Acesse :ref:`building_execution_environment`.

Quer experimentar um EE sem precisar criá-lo?
Acesse :ref:`running_community_execution_environment`.
