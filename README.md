# NLW Agents

Este projeto foi desenvolvido durante o evento NLW da Rocketseat.

## Descrição

O NLW Agents é um backend construído em Node.js utilizando TypeScript, Fastify e Drizzle ORM, com foco em performance, tipagem segura e boas práticas de desenvolvimento.

## Tecnologias e Bibliotecas Principais

- **Node.js**: Ambiente de execução JavaScript.
- **TypeScript**: Superset do JavaScript com tipagem estática.
- **Fastify**: Framework web focado em alta performance.
- **Drizzle ORM**: ORM para TypeScript moderno e seguro.
- **Postgres**: Banco de dados relacional utilizado.
- **Zod**: Validação de schemas e tipagem.
- **fastify-type-provider-zod**: Integração do Zod com Fastify para validação de rotas.
- **@fastify/cors**: Middleware para habilitar CORS.
- **@fastify/swagger**: Documentação automática das rotas.
- **OpenAI**: Integração para geração de sugestões e áudios.
- **Outras libs auxiliares**: conforme necessidades do projeto.

## Padrões de Projeto

- **Type-safe**: Uso extensivo de TypeScript e validação com Zod.
- **Modularização**: Separação de responsabilidades em módulos para rotas, banco de dados e validação.
- **.env**: Configuração via variáveis de ambiente.

## Setup e Configuração

1. **Clone o repositório:**
   ```bash
   git clone <url-do-repo>
   cd server
   ```

2. **Instale as dependências:**
   ```bash
   npm install
   ```

3. **Configure o banco de dados:**
   - Renomeie o arquivo `.env.example` para `.env` e preencha as variáveis necessárias.

4. **Rode as migrations e seeds:**
   ```bash
   npm run db:migrate    # Executa as migrations do banco
   npm run db:generate   # Gera as entidades a partir do banco
   npm run db:seed       # (Opcional) Popula o banco com dados iniciais
   ```

5. **Inicie o servidor em modo desenvolvimento:**
   ```bash
   npm run dev
   ```

O servidor estará disponível conforme configuração da porta no arquivo `.env`.

## Novas Funcionalidades e Rotas

- **Criação de salas (rooms):**
  - `POST /rooms` – Cria uma nova sala
  - `GET /rooms/:id` – Busca detalhes de uma sala
  - `GET /rooms/:id/questions` – Lista perguntas de uma sala

- **Criação e listagem de perguntas (questions):**
  - `POST /questions` – Cria uma nova pergunta
  - `GET /questions/:id` – Busca detalhes de uma pergunta

- **Sugestões e áudios:**
  - `POST /audio` – Cria um áudio a partir de um texto
  - `POST /suggestions` – Gera sugestões de respostas por chunks

- **Retornos aprimorados:**
  - Retorno do count de perguntas em salas
  - Inclusão da coluna `createdAt` nas entidades

- **Scripts de banco:**
  - `npm run db:migrate`, `npm run db:generate`, `npm run db:seed`

## Exemplo de Request para Criar Sala
```http
POST /rooms
Content-Type: application/json

{
  "name": "Sala Exemplo"
}
```

## Exemplo de Request para Criar Pergunta
```http
POST /questions
Content-Type: application/json

{
  "roomId": "uuid-da-sala",
  "content": "Qual a sua dúvida?"
}
```

## Exemplo de Request para Geração de Áudio
```http
POST /audio
Content-Type: application/json

{
  "text": "Texto para sintetizar em áudio."
}
```

## Exemplo de Request para Sugestão de Resposta
```http
POST /suggestions
Content-Type: application/json

{
  "questionId": "uuid-da-pergunta"
}
```

---

Desenvolvido durante o evento NLW da Rocketseat.
