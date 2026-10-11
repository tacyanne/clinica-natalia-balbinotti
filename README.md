# Clínica Natalia Balbinotti

Site estático com dois documentos para a clínica **Natalia Balbinotti Estética Integrativa** (Londrina/PR):

- **`/` (index.html)**: plano do projeto, com visão geral, evolução (incluindo cronograma em gantt), pendências e investimento do sistema web da clínica. Organizado em abas.
- **`/sistema/` (sistema/index.html)**: prévia em construção do site da clínica.

As duas páginas usam `noindex` e não aparecem em buscadores.

## Stack

- HTML + CSS + JavaScript puro, cada página em um único arquivo autocontido (sem framework, sem build, sem dependências npm)
- Fontes do Google Fonts (Playfair Display e Montserrat)
- Imagens (logo, fotos, produtos) referenciadas via `raw.githubusercontent.com` deste repositório, branch `main`

## Rodar localmente

Não há instalação nem build. Sirva a pasta raiz com qualquer servidor estático, por exemplo:

```bash
npx serve .
# ou
python -m http.server 8000
```

Depois abra `http://localhost:8000/` (plano) e `http://localhost:8000/sistema/` (prévia).

> Use um servidor em vez de abrir o arquivo direto: o link "ver prévia" usa o caminho absoluto `/sistema/`.

## Deploy

Hospedado na Vercel, projeto `plano-natalia-balbinotti`:
https://plano-natalia-balbinotti.vercel.app

Não há `vercel.json`; a Vercel serve os arquivos estáticos como estão.

## Estrutura

```
index.html          # plano do projeto
sistema/index.html  # prévia do site da clínica
logo-nb.png         # logo
fotos/              # fotos institucionais
produtos/           # imagens de produtos
```
