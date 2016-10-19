# log

Este comando lista todos os [commits](commit.md) da branch atual

```bash
$ git log
```

Será exibido o hash do commit, nome do author, data e mensagem do commit
exemplo:

```
commit 5a540fdeaae05eca922a86171b94d11a33abf6de
Author: Usuario <usuario@email.com>
Date:   Tue Oct 18 18:11:14 2016 -0200

    Mensagem do commit
```

## Exibindo log de outro branch

```bash
$ git log <branch>
```

Onde ```<branch>``` será o nome de seu branch


## Exibindo log de um arquivo
Para listar as alterações de um arquivo é bem similar a listagem de log do branch.

```bash
$ git log <arquivo>
```

Onde ```<arquivo>``` será o nome de seu arquivo
