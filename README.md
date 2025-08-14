# 🚀 Desafio Técnico – Jornada ENEM

Bem-vindo(a) ao desafio técnico do **Jornada ENEM**! 🎓  
Este teste tem como objetivo avaliar suas habilidades com **NestJS**, **Prisma**, **PostgreSQL**, **Docker** e autenticação **JWT**.

---

## 📌 Objetivo
Criar uma API REST para gerenciamento de usuários, incluindo autenticação JWT, seguindo boas práticas de arquitetura e organização de código.

---

## 🛠 Stack Obrigatória
- [NestJS](https://nestjs.com/) + TypeScript
- [Prisma ORM](https://www.prisma.io/)
- [PostgreSQL](https://www.postgresql.org/)
- [Docker](https://www.docker.com/)
- JWT + bcrypt

---

## 📋 Requisitos
### 1. Modelagem Prisma
Tabela `User` com os campos:
- `id` (string ou int)
- `nome` (string)
- `email` (string, único)
- `senha` (string, com hash usando bcrypt)
- `criadoEm` (DateTime, default now)

### 2. Endpoints obrigatórios
#### Autenticação
- `POST /auth/register` → cria novo usuário
- `POST /auth/login` → retorna JWT

#### Usuários (rotas protegidas por JWT)
- `GET /users` → lista todos os usuários
- `GET /users/:id` → retorna um usuário específico
- `PUT /users/:id` → atualiza usuário (somente o próprio ou admin)
- `DELETE /users/:id` → remove usuário (somente o próprio ou admin)

---

## 🐳 Docker
O projeto deve conter um `docker-compose.yml` que rode:
- API NestJS
- PostgreSQL
- Migrations automáticas (`npx prisma migrate deploy`)

---

## ✅ Boas práticas esperadas
- Uso de **DTOs** e `class-validator`
- Tratamento de erros com `HttpExceptionFilter`
- Módulos bem separados (`AuthModule`, `UserModule`, etc.)
- Variáveis de ambiente via `.env`


# Acessar API
http://localhost:3000
