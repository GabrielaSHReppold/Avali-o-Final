# GrowTwitter

Projeto de API para uma rede social estilo Twitter, desenvolvida com Node.js, Express e Prisma ORM, conectada a um banco de dados PostgreSQL.

## Objetivo
Avaliar os conhecimentos adquiridos sobre a conexão de bancos de dados no backend usando Prisma e Express, com implementação de CRUD para funcionalidades principais.

## Funcionalidades Principais
- **Usuários**: Cadastro, autenticação (login) e gerenciamento.
- **Tweets**: Criação, leitura, atualização e exclusão de tweets.
- **Likes**: Curtidas em tweets específicos.
- **Autenticação**: Acesso às rotas de Tweets e Likes restrito a usuários autenticados.

## Estrutura de Dados
### Usuário
- ID, Nome, E-mail, Username, Senha

### Tweet
- ID, Conteúdo, Tipo (Tweet ou Reply), Usuário (ID)

### Like
- Usuário (ID), Tweet (ID)

### Follower
- Usuário (ID), Seguidor (ID)

### Reply
- ID, Conteúdo, Tipo (R), Referência ao Tweet original, Usuário (ID)

## Regras de Negócio
- **Tweets**: Cada tweet tem um ID único, tipo (Tweet ou Reply) e pertence a um único usuário.
- **Likes**: Um usuário pode curtir um tweet apenas uma vez.
- **Followers**: Usuário pode seguir outros, mas não a si mesmo.
- **Replies**: Um reply é considerado um tweet com referência ao tweet original.

## Tecnologias Utilizadas
- **Node.js**
- **Express**
- **Prisma ORM**
- **PostgreSQL**

## Configuração do Projeto
1. Instalar dependências: `npm install`
2. Configurar o Prisma e conectar ao PostgreSQL.
3. Executar as migrações do Prisma para criação das tabelas.

## Boas Práticas
- Código limpo e organizado
- Utilização dos recursos da linguagem e boas práticas de desenvolvimento
