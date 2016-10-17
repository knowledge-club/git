# O que é git

Git é um sistema de controle de versões, ou seja, ele tem o objetivo de controlar alterações em arquivos e armazenar estas alterações internamente com vários objetivos:

- Tornar possível a reversão de arquivos para vários estágios de desenvolvimento anteriores
- Manter um histórico de tudo que foi editado
- Manter um log de alterações, bem como identificar a pessoa que realizou estas alterações
- Provém uma maneira simples através de Tags para identificar um release ou uma versão

É importante destacar que o git é um sistema de controle de versões __distribuido__, ou seja, cada computador possui uma cópia completamente funcional de todo o projeto, como na imagem a seguir:

![Diagrama de sistemas de versão distribuidos](https://git-scm.com/figures/18333fig0103-tn.png)

## Ciclo de vida de um arquivo

O ciclo de vida de um arquivo passa por diversos estágios:

- Untracked: O arquivo não está sendo versionado (o git não vai controlar o histórico de alterações)
- Tracked: As alterações do arquivo estão sendo controladas pelo Git.

Uma vez no estado _tracked_ o arquivo pode ter mais três outros estados:

- Unmodified: O arquivo não sofreu modificações
- Modified: O arquivo sofreu modificações
- Staged: O arquivo sofreu modificações que já estão na fila para serem aceitas por um commit

Um commit reseta o estado do arquivo para _unmodified_ ou seja, sempre que um commit é realizado, a alteração é dada como aceita.

![Ciclo de vida do arquivo](https://git-scm.com/figures/18333fig0201-tn.png)
