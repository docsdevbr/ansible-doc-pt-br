..
  SPDX-FileCopyrightText: The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-only
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-only.txt

  source_url: https://github.com/ansible/ansible-documentation/blob/stable-2.20/docs/docsite/rst/getting_started/get_started_inventory.rst
  revision: c95f2e09f67ffd4db957eda33e809fedfdad22ec
  status: ready

.. _get_started_inventory:

*********************
Criando um inventário
*********************

Os inventários organizam os nós gerenciados em arquivos centralizados que
fornecem ao Ansible informações do sistema e locais de rede.
Usando um arquivo de inventário, o Ansible pode gerenciar um grande número de
hosts com um único comando.

Para concluir as etapas a seguir, você precisará do endereço IP ou do nome de
domínio totalmente qualificado (FQDN) de pelo menos um sistema host.
Para fins de demonstração, o host pode estar sendo executado localmente em um
contêiner ou em uma máquina virtual.
Você também deve garantir que sua chave SSH pública seja adicionada ao arquivo
``authorized_keys`` em cada host.

Continue com os primeiros passos com o Ansible e crie um inventário da seguinte
forma:

#. Crie um arquivo chamado ``inventory.ini`` no diretório ``ansible_quickstart``
   que você criou no :ref:`passo anterior<get_started_ansible>`.
#. Adicione um novo grupo ``[myhosts]`` ao arquivo ``inventory.ini`` e
   especifique o endereço IP ou o nome de domínio totalmente qualificado (FQDN)
   de cada sistema host.

   .. code-block:: ini

      [myhosts]
      192.0.2.50
      192.0.2.51
      192.0.2.52

#. Verifique seu inventário.

   .. code-block:: bash

      ansible-inventory -i inventory.ini --list

#. Faça o ping no grupo ``myhosts`` no seu inventário.

   .. code-block:: bash

      ansible myhosts -m ping -i inventory.ini

   .. note::
      Passe a opção ``-u`` com o comando ``ansible`` se o nome de usuário for
      diferente no nó de controle e nos nós gerenciados.

   .. literalinclude:: ansible_output/ping_inventory_output.txt
      :language: text

Parabéns, você criou um inventário com sucesso.
Continue aprendendo com o Ansible :ref:`criando um playbook<get_started_playbook>`.

Inventários em formato INI ou YAML
==================================

Você pode criar inventários em arquivos ``INI`` ou ``YAML``.
Na maioria dos casos, como no exemplo das etapas anteriores, os arquivos ``INI``
são simples e fáceis de ler para um pequeno número de nós gerenciados.

Criar um inventário em formato ``YAML`` torna-se uma opção sensata à medida que
o número de nós gerenciados aumenta.
Por exemplo, o seguinte é um equivalente ao arquivo ``inventory.ini`` que
declara nomes exclusivos para os nós gerenciados e usa o campo ``ansible_host``:

.. literalinclude:: yaml/inventory_example_vms.yaml
      :language: yaml

Dicas para criar inventários
============================

* Certifique-se de que os nomes dos grupos sejam significativos e únicos.
  Os nomes dos grupos também diferenciam maiúsculas de minúsculas.
* Evite espaços, hífens e números antes dos nomes dos grupos (use ``andar_19``,
  não ``19_andar``) nos nomes dos grupos.
* Agrupe os hosts em seu inventário logicamente de acordo com o **O quê**,
  **Onde** e **Quando**.

  O quê
    Agrupe os hosts de acordo com a topologia, por exemplo: banco de dados, web,
    leaf, spine.

  Onde
    Agrupe os hosts por localização geográfica, por exemplo: datacenter, região,
    andar, prédio.

  Quando
    Agrupe os hosts por estágio, por exemplo: desenvolvimento, teste,
    homologação, produção.

Use metagrupos
--------------

Crie um metagrupo que organize vários grupos em seu inventário com a seguinte
sintaxe:

.. code-block:: yaml

   metagroupname:
     children:

O inventário a seguir ilustra uma estrutura básica para um centro de dados.
Este exemplo de inventário contém um metagrupo ``network`` que inclui todos os
dispositivos de rede e um metagrupo ``datacenter`` que inclui o grupo
``network`` e todos os servidores web.

.. literalinclude:: yaml/inventory_group_structure.yaml
   :language: yaml

Crie variáveis
--------------

As variáveis definem valores para nós gerenciados, como endereço IP, FQDN,
sistema operacional e usuário SSH, para que você não precise especificá-los ao
executar comandos Ansible.

As variáveis podem ser aplicadas a hosts específicos.

.. literalinclude:: yaml/inventory_variables_host.yaml
   :language: yaml

As variáveis também podem ser aplicadas a todos os hosts em um grupo.

.. literalinclude:: yaml/inventory_variables_group.yaml
   :language: yaml

.. seealso::

   :ref:`intro_inventory`
       Saiba mais sobre inventários nos formatos ``YAML`` ou ``INI``.
   :ref:`variables_in_inventory`
       Saiba mais sobre variáveis de inventário e sua sintaxe.
   :ref:`vault`
       Descubra como criptografar conteúdo sensível em seu inventário, como
       senhas e chaves.
