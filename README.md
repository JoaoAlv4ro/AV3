# AV3

## Submódulos

Este repositório usa dois submódulos Git:

- `frontend` -> [AEROCODE-FrontEnd](https://github.com/JoaoAlv4ro/AEROCODE-FrontEnd.git)
- `backend`  -> [AEROCODE-BackEnd](https://github.com/JoaoAlv4ro/AEROCODE-BackEnd.git)

## Clonando o repositório (já com submódulos)

Para clonar tudo de uma vez:

```bash
git clone --recurse-submodules https://github.com/JoaoAlv4ro/AV3.git
```

Caso já clonou sem `--recurse-submodules`:

```bash
git submodule update --init --recursive
```

## Atualizando os submódulos

Para puxar as últimas mudanças de cada submódulo (assumindo branch `main`):

```bash
git submodule foreach git pull origin main
```

## Setup Rápido

### Backend (`backend/`)
```bash
cd backend
cp .env.example .env   # editar valores
npm install
npx prisma migrate dev
npm run dev             # servidor em desenvolvimento
```

### Frontend (`frontend/`)
```bash
cd frontend
cp .env.example .env   # editar valores
npm install
npm run dev             # abre em http://localhost:5173
```
Adendo: faça login usando dev/dev

### Integração
- Ajuste `VITE_API_BASE_URL` (quando criado) para apontar para a porta do backend (ex.: `http://localhost:3001`).

## Estrutura Geral

- `backend/` – API Node/Express + Prisma (MySQL).
- `frontend/` – Interface React + Vite.

Detalhes de setup adicionais em cada `README.md` dos subprojetos.
