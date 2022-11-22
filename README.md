# Comandos Git mais frequentes #

> Olá para você que chegou até aqui, seja bem-vindo para tirar as suas dúvidas de forma rápida, direta e fácil sobre os comandos GIT mais utilizados 
no dia a dia. Seguem abaixo os comandos Git mais frequentes, sua forma de aplicação e a sua descrição, então 
se sinta livre para aplicar cada um deles em seus projetos.
<br></br>
<br> **so enjoy** :blush: </br>
<br></br>

# GIT LOG #

Este comando permite visualizar todo o histórico de commits ou um commit espcífico.
<br><br/>

Para visualizar todas as alterações do projeto: 
```
git log
```

Para visualizar todas as alterações no projeto em uma linha:
```
git log --oneline
````

Para visualizar em vez de menos informações, visualizar todas as alterações do commit:
```
git log -p
```

Para pesquisar as informações do autor daquele commit com o comando:
```
git log --author="user_name"
```

Para pesquisar informações por data
```
git log --since=1.month.ago --until=1.day.ago
```

O comando <code>git log</code> Permite  opções e personalização para deixar a visualização mais amigável ao profissional. 
Para personalizar utilize o parâmetro <code>-prety=format: <parâmetro> </code> para personalização.

<br></br>**Parâmetros**:

<br></br><code>%h</code>: o percentual com a letra h minúscula irá apresentar o hash reduzido do commit;
<br></br><code>%d</code>: o percentual com a letra d minúscula irá mostrar a branch e também a tag do commit (caso exista);
<br></br><code>%s</code>: o percentual coma letra s minúscula (de subject) irá demonstrar a mensagem do commit;
<br></br><code>%cn</code>: nome da pessoa que realizou o commit;
<br></br><code>%cr</code>: a data relativa do commit.
    
<br></br>Para alterar as cores de cada coluna se adiciona o parâmetro <code>%C</code> seguido da cor entre parênteses (blue).
<br></br>**Exemplo**:
```
git log --pretty=format:'%C(blue)%h%C(red)%d %C(white)%s - %C(cyan)%cn, %C(green)%cr'
```
<br></br>

# GIT CLONE #

Para baixar o código-fonte de um repositório original remoto para o repositório local da máquina:
```
git clone <url>
```

Faz o clone do repositório para uma pasta específica. O repositório localizado em repositorio é clonado para uma pasta chamada meu-projeto-clone:
```
git clone <repositorio> <meu-projeto-clone>
```

Faz o clone do repositório a partir de uma branch específica, diferente da original. Faz o clone apenas da branch new_feature de repositorio
```
git clone -branch new_feature <repositorio>
```

Faz a desvinculação do código cópia do código do repositório original
```
git remote rm origin
```

Puxar todas as alterações do projeto do repositório remoto para a máquina local e ver as alterações feitas na máquina local que ainda não foram comitadas
```
git pull <url>
```
<br></br>

**Diferenças** entre os comandos <code>git clone</code> e o <code>git pull</code>
Eles fazem coisas diferentes em relação ao repositório remoto:

<br></br>
**git clone**:

- Faz uma **"copia"** todo um **repositório remoto** para um outro **repositório local**;
- Faz a **configuração** da **conexão remota** entre o **repositório local** e o **repositório remoto**;
- Faz inicialmente uma **copia** da **branch "default"** do repositório (geralmente **"master"**, **"main"**, etc) do **repositório remoto**;
- Fazemos isso **uma vez**.

<br></br>

**git pull**:

- Ele **"atualiza"** a sua **branch local** com os dados do **repositório remoto**;
- Ele **atualiza** uma **branch específica**;
- É necessário já ter o **respositório local** e **configurado**;
- É feito sempre que precisa **atualizar** o **repositório local**.

<br></br>

# GIT STATUS #

Faz a verificação das condições do diretório de trabalho e da área de staging, ele serve para fornecer algumas informações importantes sobre a branch em que você estiver no momento, incluindo se ela está atualizada em relação à master e quais arquivos foram alterados
```
git status
```

Faz a verificação de status de forma resumida
```
git status -s
```
# GIT COMMIT #

Este comando faz uma versão de um conjunto de alterações provisórias, define um ponto de verificação no processo de desenvolvimento, 
permitindo que se retorne posteriormente se necessário.

Forma mais frequente de fazer o commit com uma mensagem
```
git commit -m "nome-do-commit"
```

Para fazer o commit em um arquivo específico:
```
git commit <nome-do-arquivo-sem-maior-que-ou-menor-que> 
```

Para fazer o commit em todos os arquivos:
```
git commit .
```
# GIT PUSH #


Este comando faz o envio do repositório local para o Github.

Forma mais frequente de utilização do comando:

```
git push origin main
```

Fazer o push de um arquivo específico:
```
git push <nome-do-arquivo>
```

Fazer o push de um branch específica:
```
git push -u <nome-da-branch>
```
# GIT DIFF #

Faz informar as exatas alterações feitas e não apenas quais arquivos foram alterados. 
Faz a comparação entre as bases de dados git e informa quais linhas foram adicionadas e removidas.

```
git diff
```

> **DIFF** - Mostra as diferenças entre as versões do projeto

# GIT RESTORE #

Este comando é utilizado para alterar a aplicação para um momento temporal de uma alteração, e esta alteração é feita apenas localmente, 
para fazer de forma global necessita que seja dado um git push.

Este comando é frenquentemente usado desta forma:
```
git restore --source <numero-da-hash-do-commit>
```
ou 
```
git restore --source <numero-da-hash>
```
Para deixar todo o arquivo no momento daquele estado:
```
git restore .
```

# GIT CHECKOUT #

Esse comando permite mudar de branch.

Para mudar de branch:
```
git checkout <nome-da-branch>
```

Para criar e mudar de branch em um único comando:
```
git checkout -b <nome-da-branch>
```

# GIT BRANCH #

Para mostrar todas as branchs disponíveis:

```
git branch
```

Para criar uma branch local:
```
git branch <nome-da-branch>
```

# GIT MERGE #

Faz a cópia de todos os arquivos da branch especificada para a branch em que está rodando o git. 
Fazer após concluir o projeto e estiver funcionando.
```
git merge <nome-da-branch>
```

# GIT ADD #


Esse comando é utilizado para fazer a inclusão das alterações dos arquivos para o próximo commit.

Forma mais frequente para incluir todos os arquivos para o commit:
```
git add .
```

Para incluir um arquivo específico para commit:
```
git add <nome-do-arquivo>
```

Para incluir todos os arquivos:
```
git add -A
```

# GIT INIT #

Faz criar um repositório vazio ou faz a criação de uma pasta já existente e que não está em controle de versão.

```
git init
```

# GIT REVERT #

Para desfazer as alterações no projeto localmente ou remotamente:
```
git revert <'numero-do-hash'>
```

# GIT STASH #

Fazer a mudança de uma branch para a outra sem a necessidade de se fazer o commit:
```
git stash
```
Fazer a verificação de todas as stashes feitas:
```
git stash list
```
Fazer o apply de stashes antigos:
```
git stash apply stash@{2}.
```

# REFERÊNCIAS #

<br></br>[PIPZ ACADEMY](https://docs.pipz.com/central-de-ajuda/learning-center/guia-basico-de-markdown#open)
<br></br>[GITHUB](https://gist.github.com/rxaviers/7360908)
<br></br>[GEEKHUNTER](https://blog.geekhunter.com.br/comandos-git-mais-utilizados/#Git_checkout)
<br></br>[FORMATAÇÃO DO GIT LOG](https://devhints.io/git-log-format)
<br></br>[GITLOG DATASHEET](https://devhints.io/git-log)

<br></br> :brazil:<code>Matheus Reis - Cloud Security Engineer at Infinity Cybersecurity Solutions - BR</code>:brazil:
