# Branch

Um branch é composto de um ou mais commits, o branch padrão é chamado de __master__, esté é o conjunto de todas as alterações "de produção".

A cada commit realizado, o Git realiza um armazenamento em árvore de todos os objetos que foram alterados bem também como seus metadados (autor, arquivos, data, hora) em outros commits separados, como abaixo:

![Arquivos de commit](https://git-scm.com/figures/18333fig0301-tn.png)

Se novas alterações forem feitas e enviadas novamente, o Git manterá um ponteiro pai para o seu novo commit, indicando que ele veio depois do commit que foi feito imediatamente antes, desta forma criando uma linha do tempo de snapshots, mantendo uma estrutura de multiplos commits conectados:

![Ciclo de commits](https://git-scm.com/figures/18333fig0302-tn.png)

Um branch é basicamente um ponteiro para cada um destes commits, ou seja, cada snapshot contém uma "foto" do que foi realizado até aquele momento, o branch simplesmente aponta qual snapshot estará sendo utilizado como pai.

![Branches](https://git-scm.com/figures/18333fig0303-tn.png)

Ao criar um novo branch, você está criando um novo ponteiro para um snapshot, digamos que ao invés de trabalhar com a versão mais recente, você prefira trabalhar em um local separado, uma vez que as alterações feitas por um branch não refletem nas alterações de outro:

![Branches novos](https://git-scm.com/figures/18333fig0304-tn.png)

Para criar um branch usamos:

```sh
git branch <nome do branch>
```

Para saber em qual branch você está, o Git armazena um ponteiro especial chamado `HEAD`, que nada mais é do que uma indicação:

![HEAD](https://git-scm.com/figures/18333fig0305-tn.png)

Se trocarmos de branch, o `HEAD` sairá do `master` e irá para o branch de nossa escolha, desta forma, todos os commits realizados naquele branch serão criados com o ponteiro para o mesmo, assim podemos voltar para um estado anterior do arquivo apenas movendo os ponteiros para as posições aonde o `master` se encontrava:

![Movendo branches](https://git-scm.com/figures/18333fig0307-tn.png)

Assim podemos voltar para o estado do nosso programa no momento que paramos o branch `master`:

![Revertendo](https://git-scm.com/figures/18333fig0308-tn.png)

Para remover um branch usamos:

```sh
git branch -d <nome do branch>
```

Ou, para forçar a remoção caso haja alterações pendentes:

```sh
git branch -D <nome do branch>
```
