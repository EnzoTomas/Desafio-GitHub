# Desafio de projeto Git/Github
#### Projeto voltado ao desafio de Git/Github

## Links Úteis

[O que é markdown?](https://www.markdownguide.org/getting-started/) 

[Sintaxe Básica sobre Markdown.](https://www.markdownguide.org/basic-syntax/)

## Sha1 

É interessante começarmos esse incrível algoritmo de hash criptográfico. Usado para garantir a integridade e autenticidade de dados digitais, como senhas, arquivos e mensagens, através de uma criação sobre "impressão digital".   A saída de encriptação deste algoritmo se torna único, pois ela gera um conjunto de characteres identificadores de quarenta dígitos. Independente do que seja alterado o sistema de segurança capta e gera um novo hash criptográfico. 

Por fora do conteúdo pude analisar que devido a vulnerabilidades descobertas na sua estrutura de criptografia ele foi gradualmente sendo substituído por algoritmos de hash mais robustos, como o SHA-256 e SHA-3.

## Objetos do Git

- Um Blob é um objeto que representa o conteúdo de um arquivo em um determinado ponto no tempo. Ele armazena o conteúdo bruto do arquivo, juntamente com um cabeçalho que especifica o tipo de arquivo e o tamanho do conteúdo.

- Tree é um objeto que representa um diretório ou uma pasta em um repositório Git. Ele contém uma lista de entradas que descrevem os arquivos e subdiretórios que estão contidos nesse diretório, juntamente com um hash único para cada um desses arquivos e subdiretórios. Cada entrada no tree é um par de nome e hash, onde o hash aponta para o blob ou tree que representa o conteúdo do arquivo ou subdiretório.

- Um commit é um objeto que representa um conjunto específico de mudanças feitas em um repositório Git em um determinado ponto no tempo. Ele contém um hash para o tree que representa o estado do repositório após as mudanças, bem como informações adicionais, como o autor do commit e uma mensagem de log.

  >  Em resumo, blobs representam o conteúdo bruto dos arquivos, trees representam a estrutura de diretórios e arquivos em um repositório e commits representam um conjunto específico de mudanças feitas em um repositório em um determinado ponto no tempo.
