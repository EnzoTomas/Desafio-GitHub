# Desafio de projeto Git/Github
#### Projeto voltado ao desafio de Git/Github

## Links Úteis

[O que é markdown?](https://www.markdownguide.org/getting-started/) 

[Sintaxe Básica sobre Markdown.](https://www.markdownguide.org/basic-syntax/)

## Sha1 

É interessante começarmos com esse incrível algoritmo de hash criptográfico. Usado para garantir a integridade e autenticidade de dados digitais, como senhas, arquivos e mensagens, através de uma criação sobre "impressão digital". A saída de encriptação deste algoritmo se torna único, pois ela gera um conjunto de characteres identificadores de quarenta dígitos. Independente do que seja alterado o sistema de segurança capta e gera um novo hash criptográfico. 

Por fora do conteúdo pude analisar que devido a vulnerabilidades descobertas na sua estrutura de criptografia ele foi gradualmente sendo substituído por algoritmos de hash mais robustos, como o SHA-256 e SHA-3.

## Objetos do Git

- Um **Blob** é um objeto que representa o conteúdo de um arquivo em um determinado ponto no tempo. Ele armazena o conteúdo bruto do arquivo, juntamente com um cabeçalho que especifica o tipo de arquivo e o tamanho do conteúdo.

- **Tree** é um objeto que representa um diretório ou uma pasta em um repositório Git. Ele contém uma lista de entradas que descrevem os arquivos e subdiretórios que estão contidos nesse diretório, juntamente com um hash único para cada um desses arquivos e subdiretórios. Cada entrada no tree é um par de nome e hash, onde o hash aponta para o blob ou tree que representa o conteúdo do arquivo ou subdiretório.

- Um **commit** é um objeto que representa um conjunto específico de mudanças feitas em um repositório Git em um determinado ponto no tempo. Ele contém um hash para o tree que representa o estado do repositório após as mudanças, bem como informações adicionais, como o autor do commit e uma mensagem de log.

  >  Em resumo, **blobs** representam o conteúdo bruto dos arquivos, **trees** representam a estrutura de diretórios e arquivos em um repositório e **commits** representam um conjunto específico de mudanças feitas em um repositório em um determinado ponto no tempo.

## Chave SSH

A chave **SSH** é uma forma de autenticação criptografada usada em conexões seguras de rede, como acesso remoto a servidores ou para operações de controle de versão em sistemas de gerenciamento de código-fonte distribuído, como Git. 

> A chave **SSH** é composta de duas partes, uma pública e uma privada, que são usadas em conjunto para autenticar a conexão.

Ao usar a chave **SSH**, um usuário pode se conectar a um servidor ou a um serviço remoto sem precisar digitar uma senha. Em vez disso, o usuário usa a chave privada para autenticar a conexão, que é validada pelo servidor usando a chave pública correspondente.

> As chaves **SSH** são amplamente usadas por administradores de sistemas, desenvolvedores e usuários que precisam acessar serviços remotos de forma segura e eficiente.

## Criação de um repositório 

A criação de um repositório é essencial para o gerenciamento eficiente de projetos de software e outros arquivos digitais, permitindo que as equipes trabalhem juntas de maneira colaborativa, mantendo um histórico completo de todas as alterações e garantindo a integridade e segurança do projeto.

#### Comandos

> Comandos básicos para um processo de criação de repositórios. Iniciação, movimentação de arquivos e inicio de versionamento e criação de um commit.

- **Git init**

  Podemos utiliza-lo para a criação de repositórios Git em um diretório existente. Quando executado em um diretório vazio, o comando cria um novo diretório .git, que é o diretório principal do repositório Git. 

  >Sendo assim, após o comando dado ele faz uma liberação para que eu possa fazer commits das alterrações.
  >
  >>É importante lembrar que um novo repositório iniciado com "git init" não possui nenhum commit ou branch definido, e é necessário fazer o primeiro commit para salvar o estado inicial do projeto no repositório.

- **Git add**

  É usado para adicionar arquivos ao índice do Git, preparando-os para serem commitados no repositório Git.

  > Quando você faz um "git add", você está efetivamente dizendo ao Git quais arquivos você deseja incluir na próxima alteração de estado do repositório (commit).
  >
  > >- Adicionar um arquivo específico ao índice
  > >
  > >  > $ git add nome-do-arquivo
  > >
  > >- Adicionar todos os arquivos modificados, removidos ou adicionados ao índice:
  > >
  > >  > $ git add .
  > >
  > >- Adicionar todos os arquivos em um diretório ao índice:
  > >
  > >  >$ git add nome-do-diretório

  *É importante lembrar que o "git add" apenas adiciona os arquivos ao índice e não os commita no repositório.*

- **Git commit**

  O Git commit serva para salvar alterações feitas em um ou mais arquivos adicionados ao índice do Git. 

  > Quando você executa o "git commit", você está criando uma nova alteração no histórico do repositório Git, que é armazenada como um novo commit.
  >
  > >- Com uma mensagem de commit:
  > >
  > >  > $ git commit -m "mensagem do commit"
  > >
  > >- Abrindo um editor de texto para inserir uma mensagem de commit mais longa:
  > >
  > >  > $ git commit

  Depois que um commit é criado, ele é adicionado ao histórico do repositório Git e pode ser visto usando o comando "git log". 

  *É importante lembrar que, embora o "git commit" salve as alterações no repositório, ele não as envia para um repositório remoto.*
