# Painel ERER Tema 3 — Escravização, Resistência e Liberdade

Painel único 16:9 espetacular em **Slidev** (Markdown + Vue) — pronto para apresentar e exportar.

## O que já está pronto (nessa pasta)
- `slides.md` → painel único com **os 8 itens obrigatórios** (título, pergunta, resposta norteadora, 3 fatos, exemplo capoeira, 2 conceitos Raça/Cultura, conexão atual, pergunta provocadora, 6 referências)
- `style.css` → tema custom (paleta ocre/dourado, grid hero + bento 3 colunas)
- `painel-erer-tema3.pdf` → **PDF exportado** (1 slide 16:9, pronto para enviar/imprimir)
- `painel-erer-tema3.pptx` → **PPTX exportado** (imagem por slide, para apresentação)
- `public/images/` → imagens locais (vazio, usa Unsplash CDN atualmente)

## Rodar local (preview ao vivo com hot-reload)

```bash
cd apt-1
npm install        # já feito, vite 5.4.21 pinado
npm run dev        # abre http://localhost:3030
```

> Nota Windows + acentos: se `npm run dev` falhar por caminho com acentos, copie `apt-1/` para `C:\temp\apt-1` e rode lá.

## Build e export

```bash
cd apt-1
npm run build              # gera dist/ (ignorado no git, para GitHub Pages)
npm run export             # npx slidev export --format pdf  → painel-erer-tema3.pdf
npm run export:pptx        # npx slidev export --format pptx → painel-erer-tema3.pptx (imagem)
```

Pré-requisito: `playwright-chromium` e `vite@5.4.21` já instalados (fix `ERR_MODULE_NOT_FOUND`).

## Trocar imagens

Imagens atuais são CDN Unsplash (funcionam no PDF). Para usar locais:

1. Coloque em `public/images/` (ex: `public/images/capoeira.jpg`)
2. No `slides.md`, troque `https://images.unsplash.com/...` por `/images/capoeira.jpg`
3. `npm run dev` e `npm run export` já resolvem `/images/...`

## Design system

- Paleta: `#1a1207` (fundo), `#D4A017` dourado, `#C17A3B` ocre, `#8D2F2B` vermelho-terra, `#FFF8E1` creme
- Tipografia: Playfair Display (títulos) + Inter (corpo) via Google Fonts
- Grid: hero 2-col + bento 3-col (resposta/conceitos | fatos/capoeira | atual/provocação/refs)

## Checklist dos 8 itens (conferido no slide)

- [x] 1. Título + pergunta investigada (hero)
- [x] 2. Resposta à pergunta norteadora (card 02)
- [x] 3. 3 fatos históricos (tráfico, Palmares, Lei Áurea)
- [x] 4. Exemplo concreto (Capoeira + UNESCO)
- [x] 5. 2 conceitos (Raça e Cultura)
- [x] 6. Conexão atual (desigualdade + cotas/Lei 10.639)
- [x] 7. Pergunta provocadora
- [x] 8. Referências (6, sem IA)
