# Merge

Mesclar alterações significa misturar dois branches, fazendo com que todas as alterações de um branch sejam propagadas para o outro. Um exemplo prático seria utilizar o modelo acima.

Imaginamos que fizemos uma alteração no nosso `master` depois mudamos para um novo branch que criamos chamado `dev` e fizemos outras alterações em arquivos separados. O uso de branches é encorajado para ser descartável, ou seja, a criação de um branch pode ser realizada apenas para criar uma alteração sem impactar o trabalho de outros desenvolvedores, o branch pode então ser mesclado no final do trabalho fazendo com que as alterações de um sejam propagadas para o outro e no final do processo ele pode ser excluído sem maiores preocupações.

Em nosso exemplo temos dois branches que estão diferentes do original, como na imagem:

![Mesclando branches](https://git-scm.com/figures/18333fig0315-tn.png)

Ao realizar o `merge` o Git procurará pelo ancestral comum mais próximo dos commits da ponta (C4 e C5), que neste caso é o C2, e criará um novo commit (chamado de merge commit) no branch de escolha do usuário apontando para este ancestral comum:

![Mesclando branches](https://git-scm.com/figures/18333fig0317-tn.png)

O comando merge pode ser realizado trocando para o repositório de destino (o C4 no caso) e rodando o seguinte comando:

```sh
git merge <nome do branch>
```

Isto fará com que o branch especificado seja mesclado no branch atual, se especificarmos como no nosso exemplo usando `git merge iss53` estando no branch master, isto criará o que é chamado de _fast-forwarding_ aonde o sistema apenas vai apontar o novo commit a frente dos demais como se ele fosse parte inerente do branch master. Isto é bom pois:

- Mantém o histórico limpo
- Faz com que seja de fácil leitura

Porém você perderia o controle dos merges ao longo do tempo. Para poder ignorar isto, e usar a chamada estratégia recursiva, aonde o sistema irá criar um novo commit que poderá ser nomeado e descrito a frente dos demais, use a flag `--no-ff` como em `git merge --no-ff iss53`, isto te levará para a tela de edição de mensagens do commit.