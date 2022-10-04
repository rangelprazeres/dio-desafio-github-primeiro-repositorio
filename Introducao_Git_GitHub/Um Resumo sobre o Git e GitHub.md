**Um Resumo sobre o Git e GitHub**

**https://www.markdownguide.org/basic-syntax/**



 **#GitHub#Git**

O que é Git? Criado em 2005 por Linus Torvalds (Criador do Linux), o git é um sistema de versionamento de código distribuído que facilita o desenvolvimento de software colaborativo.

 

Git é uma tecnologia (Software - *For tracking changes in any set of files, usually used for coordinating work among programmers collaboratively developing source code during software development*) complementar ao GitHub (Site - *A provider of Internet hosting for software development and version control using Git)*

 

Os benefícios do uso do Git/GitHub são:

- Controle de versão facilitado

- Segurança através da encryptação e tracking de commits

- Armazenamento em nuvem

- Trabalho em equipe

- Possibilidade de melhorar do seu código através de contribuição por Forks

 

Tópicos fundamentais para entendimento do Git:

 

O que é o SHA1? É um algoritmo de encriptação (Secure Hash Algorithm) desenvolvido pela NSA (Agência de Segurança Nacional dos EUA) e que é usado pelo Git. Funciona tanto para arquivos quando para objetos internos. Os dados encriptados geram um conjunto de caracteres únicos de 40 dígitos, que serve como identificação.

 

Git gera a encriptação, mas também armazena metadados no objeto, nesse caso o objeto blob armazena metadados das strings, possui SHA1.

 

Quais são os objetos internos do Git? 

- Blobs

- Trees

- Commits

 

**Blobs**: Bloco básico de composição contendo uma instância compactada do conteúdo do arquivo quando o commit aconteceu (blob é a abreviação de objeto grande binário, que é um termo de banco de dados SQL para "pode conter dados de qualquer tipo")

 

**Trees**: Armazena Blobs, com os nomes dos arquivos.

 

Ø Uma árvore pode conter outra árvore ou blobs. As árvores apontam para as blobs e tem um SHA1 dos metadados das árvores.

Ø Se mudar um caracter num arquivo, muda a encriptação da bolha, e consequentemente das árvores.

 

**Commit**: Objeto mais importante de todos, o objeto que vai dar sentido a alteração que está sendo realizada. Aponta para uma árvore, parente, autor, mensagem.

 

Ø Usa os parentes para criar uma linha do tempo e demonstrar que não houve adulteração nos commits.

 

Estados de um arquivo no git:

 

Git tem três estados principais de arquivos: committed, modified e staged. Committed: significa que os dados estão armazenados de forma segura em seu banco de dados local. Modified: significa que você alterou o arquivo, mas ainda não fez o commit no seu banco de dados. Staged: significa que você marcou a versão atual de um arquivo modificado para fazer parte de seu próximo commit.

 

Existem ainda os estados Tracked e Untracked: Arquivos rastreados são arquivos que estavam na última instância, bem como quaisquer arquivos recém-estabelecidos; eles podem ser modificados ou não modificados. Arquivos não rastreados são qualquer arquivo em seu diretório de trabalho que não estava na última instância e não está em sua área de teste.

 

Comandos essenciais usando git:

 

- Iniciar o GIT (git init)

- Adicionar arquivos a área de staged (git add *)

- Criar um commit (git commit -m "exemplomensagem")

 

Simple Work Flow:

 

1. git init (Inicializa um repositório do GIT dentro da pasta atual)

2. git config –-global user.nickname "someone" (Seta o nickname no repositório GIT local)

3. git config –-global user.email "someone@someplace.com" (Seta o email no repositório GIT local)

4. git add * (Adiciona os arquivos untracked e unmodified para staged)

5. git commit -m "some init msg" (Comita a alteração com uma mensagem "some msg")

git config --list (Exibe as configurações do repositório local)

git config --global --unset user.nickname (Remove o usuário em Git)

git config --global --unset user.email (Remove o e-mail do usuário)

 

Requisição de sincronização remota de repositório:

 

- git remote add origin https://github.com/Gultes/Gultes (Aponta o repositório local para o repositório no github, seta um apelido origin para esse repositório)

- git remote -v (Lista os repositórios remotos cadastrados)

- git pull origin master (Puxa as atualizações do repositório do GitHub para o repositório local)

- git push origin master (Empurra as atualizações do repositório local para o repositório do GitHub na branch master)

 

Disponível também em: https://www.linkedin.com/pulse/git-e-github-gustavo-sena/

 Referências:

Download -> https://github.com/git-guides/install-git

 GIT. Git Basics - Recording Changes to the Repository. Disponível em: https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository. Acesso em: 06 jul. 2022.

DATACAMP. How does Git store information? Disponível em: https://campus.datacamp.com/courses/introduction-to-git/repositories?ex=1. Acesso em: 05 jul. 2022. 