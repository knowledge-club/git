# add

O comando `add` é muito simples! Ele prepara os arquivos para serem comitados

Usando o comando com `-A` prepara todos os arquivos novos e modificados da branch atual

```sh
$ git add -A
```

Se você quiser adicionar apenas alguns arquivos, você pode espedificar

```sh
$ git add arquivo_um.rb arquivo_dois.js arquivo_tres.html
```

Ou especificar um sufixo ou um prefixo:

- Adiciona todos os arquivos com `.rb` como sufixo

```sh
$ git add *.rb
```

- Adiciona todos os arquivos com `test` como prefixo

```sh
$ git add test*
```
