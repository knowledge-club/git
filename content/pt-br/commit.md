# commit

Todo o trabalho realizado com o suporte do Git é identificado por commits. Cada commit é referente a uma ou mais alterações em um ou mais arquivos que estão sendo observados (_tracked_) pelo Git.

> Um commit é um objeto que contém alterações

Diferentemente de outros sistemas de controle de versão como o SVN, o Git não armazena uma cópia do arquivo anterior para manter o versionamento, mas sim um ponteiro para uma versão anterior daquela alteração. Em outras palavras, se uma linha for alterada em um arquivo de texto, o Git não vai armazenar uma cópia do antigo arquivo e uma cópia do novo, mas sim uma referência de ponteiro para aquela linha apenas, informando que ela possuia um conteúdo naquele determinado SHA-1 (Hash de identificação para commits). Isto faz com que o Git seja um dos sistemas de controle de versão mais eficientes que existem.

Este comado persiste os arquivos modificados na branch atual (para preparar os arquivos, use o comando `add`). Você precisa escrever uma mensagem sobre o que você fez nesses arquivos

```bash
$ git commit -m "mensagens sobre seus arquivos incríveis"
```
