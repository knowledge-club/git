# checkout

Quando iniciamos um projeto com o comando [init](content/pt-br/init.md), todo nosso projeto vai para a branch `master`. Branch é o nome que nós damos a cada modificação de um mesmo projeto

Por convenção, nunca fazemos modificações direto na branch `master`, dentro dela, deixamos sempre a ultima versão testada e validada do nosso projeto. Para trabalharmos numa nova funcionalidade ou para corrigirmos algum problema, criamos uma nova branch, uma cópia da branch `master`. Geralmente nomeamos essa nova branch com o que vamos fazer com ela, como, por exemplo `adicionar_campo_ao_banco_de_dados` ou então `corrigir_bug_login`

Para criar uma nova branch a partir da `master` use o comando

```bash
$ git checkout -b nome_da_branch
```

Esse comando faz duas coisas:

- O `-b` é um atalho que cria uma nova branch com o nome especificado
- E o `git checkout` "nos move" para essa nova branch

Sim, é possível criar branch e não utiliza-las no mesmo momento

E, caso você queira mover para uma branch já existente. Use o comando sem o `-b`:

```bash
$ git checkout nome_da_branch_ja_criada
```
