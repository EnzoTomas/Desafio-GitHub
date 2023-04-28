## Sha1 

É interessante começarmos esse incrível algoritmo de hash criptográfico. Usado para garantir a integridade e autenticidade de dados digitais, como senhas, arquivos e mensagens, através de uma criação sobre "impressão digital".   A saída de encriptação deste algoritmo se torna único, pois ela gera um conjunto de characteres identificadores de quarenta dígitos. Independente do que seja alterado o sistema de segurança capta e gera um novo hash criptográfico. 

Por fora do conteúdo pude analisar que devido a vulnerabilidades descobertas na sua estrutura de criptografia ele foi gradualmente sendo substituído por algoritmos de hash mais robustos, como o SHA-256 e SHA-3.

## Objetos do Git

- Um Blob é um objeto que representa o conteúdo de um arquivo em um determinado ponto no tempo. Ele armazena o conteúdo bruto do arquivo, juntamente com um cabeçalho que especifica o tipo de arquivo e o tamanho do conteúdo.

- Tree é um objeto que representa um diretório ou uma pasta em um repositório Git. Ele contém uma lista de entradas que descrevem os arquivos e subdiretórios que estão contidos nesse diretório, juntamente com um hash único para cada um desses arquivos e subdiretórios. Cada entrada no tree é um par de nome e hash, onde o hash aponta para o blob ou tree que representa o conteúdo do arquivo ou subdiretório.

- Um commit é um objeto que representa um conjunto específico de mudanças feitas em um repositório Git em um determinado ponto no tempo. Ele contém um hash para o tree que representa o estado do repositório após as mudanças, bem como informações adicionais, como o autor do commit e uma mensagem de log.

  >  Em resumo, blobs representam o conteúdo bruto dos arquivos, trees representam a estrutura de diretórios e arquivos em um repositório e commits representam um conjunto específico de mudanças feitas em um repositório em um determinado ponto no tempo.

## Chave SSH

A chave **SSH** é uma forma de autenticação criptografada usada em conexões seguras de rede, como acesso remoto a servidores ou para operações de controle de versão em sistemas de gerenciamento de código-fonte distribuído, como Git. 

> A chave SSH é composta de duas partes, uma pública e uma privada, que são usadas em conjunto para autenticar a conexão.

Ao usar a chave SSH, um usuário pode se conectar a um servidor ou a um serviço remoto sem precisar digitar uma senha. Em vez disso, o usuário usa a chave privada para autenticar a conexão, que é validada pelo servidor usando a chave pública correspondente.

> As chaves SSH são amplamente usadas por administradores de sistemas, desenvolvedores e usuários que precisam acessar serviços remotos de forma segura e eficiente.



## Criação de um repositório 

A criação de um repositório é essencial para o gerenciamento eficiente de projetos de software e outros arquivos digitais, permitindo que as equipes trabalhem juntas de maneira colaborativa, mantendo um histórico completo de todas as alterações e garantindo a integridade e segurança do projeto.

##### Comandos

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
  > > > $ git add nome-do-arquivo
  > >
  > >- Adicionar todos os arquivos modificados, removidos ou adicionados ao índice:
  > >
  > > > $ git add .
  > >
  > >- Adicionar todos os arquivos em um diretório ao índice:
  > >
  > > >$ git add nome-do-diretório

  *É importante lembrar que o "git add" apenas adiciona os arquivos ao índice e não os commita no repositório.*

- **Git commit**

  O Git commit serva para salvar alterações feitas em um ou mais arquivos adicionados ao índice do Git. 

  > Quando você executa o "git commit", você está criando uma nova alteração no histórico do repositório Git, que é armazenada como um novo commit.
  >
  > >- Com uma mensagem de commit:
  > >
  > > > $ git commit -m "mensagem do commit"
  > >
  > >- Abrindo um editor de texto para inserir uma mensagem de commit mais longa:
  > >
  > > > $ git commit

  Depois que um commit é criado, ele é adicionado ao histórico do repositório Git e pode ser visto usando o comando "git log". 

  *É importante lembrar que, embora o "git commit" salve as alterações no repositório, ele não as envia para um repositório remoto.*

  ## Sistema Tracked ou Untracked 

  A principal diferença entre um arquivo **untracked** e **tracked** é que os arquivos untracked não estão sendo monitorados pelo Git, enquanto os arquivos **tracked** são rastreados e o Git registra suas alterações.

- **Untracked** 

  Um arquivo **untracked** (não rastreado) em um repositório Git é um arquivo que existe no diretório de trabalho, mas ainda não foi adicionado ao Git.

  > é importante ressaltar que quando há uma  nova criação de arquivo no seu diretório ele será considerado untracked pelo Git até que você o adicione ao repositório usando o comando $ git add nome_do_arquivo.
  >
  > > Ressaltando que o Git nao rastreia automaticamente todos os arquivos em seu diretório, fazendo assim uma abertura de janela para selecionar arquivos específicos que deseje fazer commit.

- **Unmodified**

  Falamos sobre um arquivo **Unmodified** quando o arquivo se encontra rastreado pelo Git, mas não sofreu nenhuma modificação dede o último commit. Significando que há um conteúdo idêntico ao conteúdo registrado no último commit.

  

- **Modified** 

  Referimos um arquivo como **Modified** quando um arquivo rastreado pelo Git sofreu uma alteração desde o último commit registrado. Levando então a ideia de que o arquivo presente no seu diretório sofreu uma modificação em relação à versão registrada anteriormente. 

  > Os arquivos podem ser identificados pelo Git durante a execução do comando $ git status. São listados como alterados, geralmente são destacados para indicar que houve uma alteração no arquivo.
  >
  > > Para incluir uma alteração em um arquivos é preciso o uso do comando $ git add posteriormente já tendo colocado o mesmo no arquivo de preparação. Tendo a finalização deste comando já podemos utilizar um $ git commit.

- **Staged**

Um arquivo **Staged** é um arquivo que foi selecionado para uma área de preparação do Git, usando o $ git add. Uma área que coloca as alterações que deseja incluir no git a seguir. 

> Quando o comando for executado em um arquivo modificado, ele passará para o estado **staged** indicando que as alterações feitas naquele arquivo serão incluídas no próximo commit. 

A área **staged** é uma etapa intermediária que nos possibilita a escolha de quais arquivos desejamos incluir em um commit específico. Podendo assim, adicionar vários arquivos à área de preparação, usando o $ git add. E em seguida criar um commit que tenha todas as alterações preparadas. 

> Lembrando que ao executarmos o comando $ git status, os arquivos **staged** terão a sua lista separadamente dos arquivos modificados. Eles geralmente são destacados para indicar que estão prontos para serem confirmados.
>
> > Para confirmar as alterações dos arquivos **staged** em um novo commit, você pode usar o comando . Isso criará um novo ponto na história do seu repositório, contendo as alterações dos arquivos preparados.

*Em resumo, os arquivos **staged **são aqueles que foram adicionados à área de preparação usando $ git add e estão prontos para serem incluídos no próximo commit.*

## Resumo do Projeto 

O projeto aborda vários conceitos e comandos relacionados ao Git, um sistema de controle de versão amplamente utilizado no desenvolvimento de software. Alguns dos tópicos abordados são:

- Algoritmo SHA-1

  > Um algoritmo de hash criptográfico usado para garantir a integridade e autenticidade dos dados digitais. 

- Objetos do Git 

  > Utiliza três tipos principais de objetos para armazenar informações: blobs, trees e commits

- Chaves SSH

  >São usadas para autenticação criptografada em conexões seguras de rede. 

- Criação de um repositório 

  > O processo de criação de um repositório Git envolve a execução de comandos como git init, que inicia um repositório em um diretório existente, git add, que adiciona arquivos ao índice do Git, e git commit, que salva as alterações em um novo commit no histórico do repositório.

- Sistema Tracked e Untracked 

  > Um arquivo untracked (não rastreado) e tracked (rastreado) em um repositório Git está relacionada ao estado e ao monitoramento do Git em relação a esses arquivos.

  *Em resumo, o projeto abrange conceitos fundamentais do Git, como criação de repositório, adição de arquivos, criação de commits e diferenciação entre arquivos tracked e untracked. Esses conceitos são essenciais para o uso efetivo do Git no controle de versão de projetos de software.*

  
