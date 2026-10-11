# CLAUDE.md

Guia para agentes que trabalham neste repositório.

## O que é

Site estático da clínica Natalia Balbinotti Estética Integrativa (Londrina/PR):
- `index.html`: plano do projeto (abas Visão, Evolução, Pendências, Investimento; cronograma gantt dos entregáveis).
- `sistema/index.html`: prévia do site da clínica.

## Stack

- HTML/CSS/JS puro. Cada página é um único arquivo com `<style>` e `<script>` inline.
- Sem package.json, sem build, sem testes automatizados, sem dependências.
- Fontes: Google Fonts (Playfair Display, Montserrat).

## Comandos

- Dev: `npx serve .` ou `python -m http.server 8000` na raiz e abra `/` e `/sistema/`.
- Build: não existe.
- Testes: não existem. Valide abrindo as páginas no navegador (desktop e mobile).

## Estrutura

```
index.html          # plano do projeto
sistema/index.html  # prévia do site
logo-nb.png
fotos/              # fotos institucionais
produtos/           # imagens de produtos
```

## Convenções

- Conteúdo, textos e commits em português do Brasil.
- Paleta em variáveis CSS no `:root` (preto, dourado, champagne, marfim etc.). Reutilize as variáveis em vez de cores soltas.
- Imagens são referenciadas por URL absoluta `https://raw.githubusercontent.com/tacyanne/clinica-natalia-balbinotti/main/...`. Se renomear o repo ou mover arquivos, atualize essas URLs.
- Link da prévia usa caminho absoluto `/sistema/`.
- Páginas usam `<meta name="robots" content="noindex">`. Mantenha.
- Mensagens de commit seguem o histórico: `vX.Y: descrição` para entregas de conteúdo, `fix:`/`docs:` para o resto.
- Feche bem as tags HTML: já houve regressão por `div` não fechada.

## Deploy e ambientes

- Vercel, projeto `plano-natalia-balbinotti`, produção em https://plano-natalia-balbinotti.vercel.app
- Sem `vercel.json`: arquivos estáticos servidos como estão.
- Variáveis de ambiente: nenhuma.
