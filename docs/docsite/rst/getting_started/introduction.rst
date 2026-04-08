..
  SPDX-FileCopyrightText: The Ansible project contributors.

  SPDX-License-Identifier: GPL-3.0-only
  Documentation licensed under the GNU General Public License Version 3.
  The original work was translated from English into Brazilian Portuguese.
  https://github.com/docsdevbr/ansible-doc-pt-br/blob/-/LICENSES/GPL-3.0-only.txt

  source_url: https://github.com/ansible/ansible-documentation/blob/stable-2.20/docs/docsite/rst/getting_started/introduction.rst
  revision: a5dc13d28411001a39ebbfec1eb49575397b78c7
  status: ready

.. _introduction_to_ansible:

*********************
Introdução ao Ansible
*********************

O Ansible oferece automação de código aberto que reduz a complexidade e funciona
em qualquer lugar.
Usar o Ansible permite automatizar praticamente qualquer tarefa.
Aqui estão alguns casos de uso comuns para o Ansible:

* Eliminar repetições e simplificar fluxos de trabalho.
* Gerenciar e manter a configuração do sistema.
* Implantar continuamente softwares complexos.
* Realizar atualizações contínuas sem tempo de inatividade.

O Ansible usa scripts simples e legíveis por pessoas, chamados playbooks, para
automatizar suas tarefas.
Você declara o estado desejado de um sistema local ou remoto em seu playbook.
O Ansible garante que o sistema permaneça nesse estado.

Como tecnologia de automação, o Ansible foi projetado com base nos seguintes
princípios:

Arquitetura sem agentes
  Baixa sobrecarga de manutenção, evitando a instalação de software adicional
  na infraestrutura de TI.

Simplicidade
  Os playbooks de automação usam uma sintaxe YAML direta no código, que se lê
  como documentação.
  O Ansible também é descentralizado, usando SSH com credenciais de sistema
  operacional existentes para acessar máquinas remotas.

Escalabilidade e flexibilidade
  Escalar os sistemas que você automatiza de forma fácil e rápida, graças a um
  design modular que suporta uma ampla gama de sistemas operacionais,
  plataformas em nuvem e dispositivos de rede.

Idempotência e previsibilidade
  Quando o sistema está no estado descrito pelo seu playbook, o Ansible não
  altera nada, mesmo que o playbook seja executado várias vezes.

Já pode começar a usar o Ansible?
:ref:`Comece em poucos passos<get_started_ansible>`.
