# Oficina_DevOps

O projeto consiste em uma aplicação Python básica (main.py) e um Dockerfile para containerizá-la. O principal objetivo é usar um GitHub Action para validar a qualidade do código Python automaticamente em cada Pull Request.

1. Onde Criar o Arquivo do GitHub Action

Para que o GitHub reconheça nossa automação, precisamos clicar no botão 'Actions' na barra superior da guia do repositório, e clicar em  'set up a workflow yourself':

    Nele seremos redirecionados para uma aba para criação do nosso código.

2. Como Configurar o Repositório (Proteção de Branch)

Depois de criar o Action, precisamos "dizer" ao GitHub que ele é obrigatório. Vamos configurar o repositório para que nenhum código possa ser mesclado ao branch main se o nosso Action falhar.

Isso é chamado de "Regra de Proteção de Branch":

    No seu repositório GitHub, vá em Settings (Configurações).

    No menu lateral, clique em Branches (Branches).

    Clique em Add rule (Adicionar regra).

    Em Branch name pattern (Padrão do nome do branch), digite: main

    Marque a caixa: Require a pull request before merging (Exigir um pull request antes de mesclar).

    Marque a caixa: Require status checks to pass before merging (Exigir que as verificações de status passem antes de mesclar).

Quando você marcar esta última caixa, o GitHub vai pedir que você escolha quais "status checks" são obrigatórios. Assim que rodarmos nosso Action pela primeira vez, o nome dele aparecerá nessa lista para selecionarmos.

Com isso, o repositório estará configurado para nosso fluxo de CI.
