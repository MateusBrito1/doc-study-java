## O que é REST?

Rest significa *Transfêrencia de Estado Representacional.* É um estilo arquitetural para projetar redes de comunicação.

## O que é uma API REST?

Uma **API REST** é uma interface de programação de aplicação que segue os princípios da arquitetura *Rest*. Isso significa que ela utiliza um conjunto de padrões de comunicação bem definidos para permitir que diferentes sistemas se comuniquem de maneira eficiente e previsível.

## Princípios de uma API REST

1. **Arquitetura Cliente-Servidor**: A separação de preocupações entre cliente e servidor. O cliente envia solicitações para o servidor, que processa e retorna uma resposta.
2. **Stateless (Sem Estado)**: Cada solicitação do cliente para o servidor deve conter todas as informações necessárias para que o servidor compreenda e processe a solicitação. Isso significa o que? significa que o servidor não mantém nenhum estado da sessão do cliente entre as solicitações. Cada solicitação é independente.
3. **Mensagem com Protocolo HTTP**: As solicitações e respostas são trocadas utilizando métodos HTTP como: **GET, POST, PUT, DELETE**, etc. Isso permite que as APIs REST seja compatíveis com a infraestrutura da web existente.
4. **Recursos Identificáveis**: Os recursos (dados) acessíveis através da API devem ser identificados de forma única por meio de URLs (Uniform Resource Identifiers). Por exemplo, */cliente*, */produtos*, */pedidos*.
5. **Operações bem definidas nos recursos**: As operações *CRUD* (Created, Read, Update, Delete) são mapeadas para as operações HTTP: *POST, GET, PUT/PATCH, DELETE*, respectivamente.
6. **Representação de Recursos**: Os recursos devem ser representados em algum formato como *JSON, XML, HTML*, etc. Normalmente, o *JSON* é o mais utilizado devido à sua simplicidade e facilidade de uso.

## Exemplo prático:

Suponha que você tenha um serviço online que fornece informações sobre livros. Sua **API REST** poderia ter URLs como:

- */livros*: Para listar todos os livros disponíveis.
- */livros/123*: Para obter as informações sobre o livro com ID 123.
- */livros/123/comentários*: Para obter os comentários sobre o livro com o ID 123
- */autores*: Para listar todos os autores disponíveis.

## E as operações HTTP correspondem: 

- **GET** */livros*: Retorna todos os livros.
- **GET** */livros/123*: Retorna informações sobre o livro com ID 123.
- **POST** */livros*: Adiciona um novo livro.
- **PUT** */livros/123*: Atualiza a informação do livro com ID 123.
- **DELETE** */livros/123*: Remove o livro com ID 123.







