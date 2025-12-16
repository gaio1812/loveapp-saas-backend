# 🚀 LoveApp SaaS – Backend em FastAPI

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)](https://postgresql.org)
[![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=JSON%20web%20tokens&logoColor=white)](https://jwt.io)

## 📚 Sobre o Projeto

**LoveApp SaaS Backend** é uma API REST completa desenvolvida em FastAPI para um aplicativo romântico multi-usuário. O sistema permite que casais criem contas, compartilhem memórias e sincronizem dados entre múltiplos dispositivos de forma segura e eficiente.

### ✨ Principais Funcionalidades

- 🔐 **Autenticação JWT** – Sistema seguro de login com tokens de acesso e refresh
- 👥 **Gestão de Usuários** – CRUD completo com validações e hash de senhas
- 💑 **Gestão de Casais** – Vinculação de perfis e compartilhamento de conteúdo
- 📖 **Memórias e Mensagens** – Endpoints para criar, ler, atualizar e deletar conteúdos
- 📄 **Paginação** – Sistema de paginação para grandes volumes de dados
- 🔍 **Filtros Avançados** – Busca e filtragem de conteúdo por data, tipo, etc.
- 📝 **Documentação Automática** – Swagger/OpenAPI interativa
- 🔄 **Sincronização Multi-dispositivos** – Dados acessíveis em tempo real
- 🛡️ **Segurança** – Validações, CORS, rate limiting e proteção contra injeções

## 🛠️ Tecnologias Utilizadas

- **FastAPI** – Framework web moderno e de alta performance
- **Python 3.11+** – Linguagem de programação
- **PostgreSQL** – Banco de dados relacional (SQLite para desenvolvimento)
- **SQLAlchemy** – ORM para manipulação de banco de dados
- **Pydantic** – Validação de dados e serialização
- **JWT (PyJWT)** – Autenticação baseada em tokens
- **Uvicorn** – Servidor ASGI de alta performance
- **Alembic** – Migrações de banco de dados

## 🚀 Como Executar o Projeto

### Pré-requisitos

- Python 3.11 ou superior
- PostgreSQL (ou SQLite para desenvolvimento local)
- pip ou poetry para gerenciamento de dependências

### Instalação

```bash
# Clone o repositório
git clone https://github.com/gaio1812/loveapp-saas-backend.git

# Entre no diretório
cd loveapp-saas-backend

# Crie um ambiente virtual
python -m venv venv

# Ative o ambiente virtual
# Linux/Mac:
source venv/bin/activate
# Windows:
venv\Scripts\activate

# Instale as dependências
pip install -r requirements.txt
```

### Configuração

Crie um arquivo `.env` na raiz do projeto:

```env
DATABASE_URL=postgresql://user:password@localhost:5432/loveapp
SECRET_KEY=sua-chave-secreta-super-segura
ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=30
```

### Executar o Servidor

```bash
# Rodar em modo de desenvolvimento
uvicorn main:app --reload

# Rodar em produção
uvicorn main:app --host 0.0.0.0 --port 8000
```

A API estará disponível em: `http://localhost:8000`

Documentação interativa: `http://localhost:8000/docs`

## 📚 Documentação da API

### Endpoints Principais

#### Autenticação
- `POST /auth/register` – Criar nova conta
- `POST /auth/login` – Fazer login e receber token JWT
- `POST /auth/refresh` – Renovar token de acesso

#### Usuários
- `GET /users/me` – Obter dados do usuário logado
- `PUT /users/me` – Atualizar perfil
- `DELETE /users/me` – Deletar conta

#### Casais
- `POST /couples` – Criar vínculo de casal
- `GET /couples/me` – Obter dados do casal
- `PUT /couples/{id}` – Atualizar informações do casal

#### Memórias
- `POST /memories` – Criar nova memória
- `GET /memories` – Listar memórias (com paginação)
- `GET /memories/{id}` – Obter memória específica
- `PUT /memories/{id}` – Atualizar memória
- `DELETE /memories/{id}` – Deletar memória

#### Mensagens
- `POST /messages` – Enviar mensagem
- `GET /messages` – Listar mensagens do casal
- `DELETE /messages/{id}` – Deletar mensagem

## 📂 Estrutura do Projeto

```
.
├── app/
│   ├── api/
│   │   ├── routes/       # Endpoints da API
│   │   └── dependencies/ # Dependências (autenticação, etc.)
│   ├── models/          # Modelos do banco de dados
│   ├── schemas/         # Schemas Pydantic (validação)
│   ├── services/        # Lógica de negócio
│   ├── core/            # Configurações e segurança
│   └── db/              # Conexão com banco de dados
├── alembic/            # Migrações
├── tests/              # Testes automatizados
├── main.py             # Arquivo principal
├── requirements.txt    # Dependências
└── .env                # Variáveis de ambiente
```

## 🔬 Testes

```bash
# Rodar todos os testes
pytest

# Rodar com cobertura
pytest --cov=app tests/
```

## 🚀 Deploy

### Render / Railway / Fly.io

1. Conecte seu repositório GitHub
2. Configure as variáveis de ambiente
3. Deploy automático a cada push na main

### Docker

```bash
# Build da imagem
docker build -t loveapp-backend .

# Executar container
docker run -p 8000:8000 loveapp-backend
```

## 💼 Uso Profissional

Este projeto demonstra:
- Arquitetura RESTful com FastAPI
- Sistema de autenticação JWT completo
- Integração com banco de dados PostgreSQL/SQLite
- Validação robusta com Pydantic
- Documentação automática com OpenAPI/Swagger
- Boas práticas de segurança e organização de código
- Preparação para produção e escalabilidade

Ideal para demonstrar habilidades em desenvolvimento backend Python, APIs REST e arquitetura de software SaaS.

## 📄 Licença

Este projeto está sob a licença MIT.

## 👨‍💻 Desenvolvedor

Desenvolvido por **Gabriel Gaio**

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/gaio1812)

---

⭐ Se este projeto foi útil, deixe uma estrela!