# Truco dos Amigos

Jogo de **Truco Paulista** feito com React, TypeScript e Vite. A ideia é jogar no navegador e, mais para frente, também como app de celular.

## Status

Projeto em fase inicial. O foco atual é o **MVP**:

- Login e senha
- Partida completa de Truco Paulista contra um bot

## Tecnologias

- [React](https://react.dev) + [TypeScript](https://www.typescriptlang.org)
- [Vite](https://vite.dev) (ambiente de desenvolvimento e build)
- [ESLint](https://eslint.org) (análise de código)
- Planejado: [Supabase](https://supabase.com) (login e banco de dados), servidor Node para o modo online e [Capacitor](https://capacitorjs.com) para o app mobile

## Como rodar o projeto

Pré-requisito: [Node.js](https://nodejs.org) instalado (versão recente, o projeto foi iniciado com a v24).

```bash
git clone https://github.com/TrucoDosAmigos/TrucoDosAmigos
cd TrucoDosAmigos
npm install
npm run dev
```

O terminal mostra o endereço local (algo como `http://localhost:5173`). Abra no navegador.

## Scripts

| Comando | O que faz |
|---|---|
| `npm run dev` | Roda o jogo em modo de desenvolvimento, com atualização automática ao salvar |
| `npm run build` | Confere os tipos e gera a versão final para publicar |
| `npm run preview` | Abre a versão gerada pelo `build` para testar |
| `npm run lint` | Aponta problemas e más práticas no código |

## Organização do código (planejada)

```
src/
  regras/     lógica do truco (baralho, manilha, pontos, apostas), TypeScript puro, sem React
  bot/        decisões do bot
  ui/         componentes React (mesa, cartas, botões)
  servicos/   acesso ao Supabase (login, perfis, partidas)
```

A lógica do jogo fica separada da interface para poder ser reaproveitada no servidor do modo online e em um eventual app mobile.

## Como contribuir

1. Crie uma branch a partir da `main` (por exemplo `feat/baralho`).
2. Faça commits pequenos e com mensagens claras.
3. Abra um Pull Request para a `main`.
