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