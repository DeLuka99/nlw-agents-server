# NLW Agents

Este projeto foi desenvolvido durante o evento NLW da Rocketseat.

## Tecnologias e Bibliotecas Utilizadas

- **Node.js** + **TypeScript**
- **Fastify**: Framework web para Node.js
- **Drizzle ORM**: ORM para banco de dados relacional
- **PostgreSQL**: Banco de dados relacional (com extensão pgvector)
- **Zod**: Validação de esquemas e tipos
- **drizzle-kit**: Migrations e geração de schemas
- **drizzle-seed**: Seed de dados para o banco
- **Biome**: Linter e formatter

## Padrões de Projeto e Arquitetura

- Organização por módulos (rotas, banco, schemas)
- Separação de responsabilidades (rotas, validação, conexão, seed)
- Uso de validação de ambiente e dados com Zod
- Migrations e seeds versionados

## Setup e Configuração

### 1. Clone o repositório

```bash
git clone <repo-url>
cd server
```

### 2. Instale as dependências

```bash
npm install
```

### 3. Configure o banco de dados

- É necessário ter Docker instalado.
- Suba o banco com:

```bash
docker-compose up -d
```

### 4. Configure as variáveis de ambiente

Crie um arquivo `.env` na raiz com:

```
DATABASE_URL=postgresql://docker:docker@localhost:5432/agents
PORT=3333
```

### 5. Rode as migrations e o seed

```bash
npm run db:seed
```

### 6. Inicie o servidor em modo desenvolvimento

```bash
npm run dev
```

O servidor estará disponível em `http://localhost:3333`.

## Exemplos de uso

- Health check: `GET /health`
- Listar salas: `GET /rooms`

---

Desenvolvido durante o NLW da Rocketseat 🚀
