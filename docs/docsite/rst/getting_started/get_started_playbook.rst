..
  SPDX-FileCopyrightText: The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-only
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-only.txt

  source_url: https://github.com/ansible/ansible-documentation/blob/devel/docs/docsite/rst/getting_started/get_started_playbook.rst
  revision: d0ee17ece91c6ecd61f3adfc573e3884e72df5ae
  status: ready

.. _get_started_playbook:

*******************
Criando um playbook
*******************

Playbooks são modelos de automação, em formato ``YAML``, que o Ansible usa para
implantar e configurar nós gerenciados.

Playbook
  Uma lista de plays que define a ordem em que o Ansible executa operações, de
  cima para baixo, para atingir um objetivo geral.

Play
  Uma lista ordenada de tarefas que mapeia nós gerenciados em um inventário.

Task
  Uma referência a um único módulo que define as operações que o Ansible
  executa.

Módulo
  Uma unidade de código ou binário que o Ansible executa em nós gerenciados.
  Os módulos do Ansible são agrupados em coleções com um
  :term:`Nome de Coleção Totalmente Qualificado (FQCN)` para cada módulo.

Complete os seguintes passos para criar um playbook que envia pings para seus
hosts e imprime uma mensagem "Hello world":

#. Crie um arquivo chamado ``playbook.yaml`` no diretório ``ansible_quickstart``
   que você criou anteriormente, com o seguinte conteúdo:

   .. literalinclude:: yaml/first_playbook.yaml
      :language: yaml

#. Execute seu playbook.

   .. code-block:: bash

      ansible-playbook -i inventory.ini playbook.yaml

O Ansible retorna a seguinte saída:

.. literalinclude:: ansible_output/first_playbook_output.txt
      :language: text

Nesta saída, você pode ver:

* Os nomes que você deu ao playbook e a cada tarefa.
  Você deve sempre usar nomes descritivos que facilitem a verificação e a
  solução de problemas dos playbooks.

* A tarefa "Gathering Facts" é executada implicitamente.
  Por padrão, o Ansible coleta informações sobre seu inventário que podem ser
  usadas no playbook.

* O status de cada tarefa.
  Cada tarefa tem o status ``ok``, o que significa que foi executada com
  sucesso.

* O resumo da execução, que sintetiza os resultados de todas as tarefas do
  playbook por host.
  Neste exemplo, há três tarefas, então ``ok=3`` indica que cada tarefa foi
  executada com sucesso.

Parabéns, você começou a usar o Ansible!

.. seealso::

   :ref:`playbooks_intro`
     Comece a criar playbooks para cenários do mundo real.
   :ref:`working_with_playbooks`
     Saiba mais sobre os playbooks do Ansible.
   :ref:`playbooks_best_practices`
     Obtenha dicas e truques para usar playbooks.
   :ref:`vars_and_facts`
     Saiba mais sobre a palavra-chave ``gather_facts`` em playbooks.
