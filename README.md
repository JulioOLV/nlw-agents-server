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

4. **Rode as migrations/seeds (se necessário):**
   ```bash
   npm run db:seed
   ```

5. **Inicie o servidor em modo desenvolvimento:**
   ```bash
   npm run dev
   ```

O servidor estará disponível conforme configuração da porta no arquivo `.env`.

---

Desenvolvido durante o evento NLW da Rocketseat.
