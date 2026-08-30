# Painel ERER Tema 3 — Escravização, Resistência e Liberdade

Painel único 16:9 espetacular em **Slidev** (Markdown + Vue) — pronto para apresentar e exportar.

## O que já está pronto (nessa pasta)
- `slides.md` → painel único com **os 8 itens obrigatórios** (título, pergunta, resposta norteadora, 3 fatos, exemplo capoeira, 2 conceitos Raça/Cultura, conexão atual, pergunta provocadora, 6 referências)
- `style.css` → overrides globais
- `painel-erer-tema3.pdf` → **PDF exportado** (1 slide 16:9, pronto para enviar/imprimir)
- `painel-erer-tema3.png` → imagem do painel
- `dist/` → site estático buildado (`index.html`)

## Rodar local (preview ao vivo com hot-reload)

> **Atenção Windows + acentos**: o caminho `H:\My Drive\11º Período\…` quebra symlinks do npm. Use a cópia sem acentos em `C:\temp-painel-erer` (já criada) para `npm run dev`/`export`.

```bash
# opção 1 — usar a cópia sem acentos (recomendado)
cd C:\temp-painel-erer
npm install        # já feito
npm run dev        # abre http://localhost:3030

# opção 2 — se mover a pasta para um caminho sem acentos
npm run dev
```

## Build e export

```bash
cd C:\temp-painel-erer
npm run build              # gera dist/
npm run export             # slidev export --format pdf  → painel-erer-tema3.pdf
npm run export:pptx        # slidev export --format pptx → imagens (texto não editável)
```

Pré-requisito PPTX/PDF: `npm install -D playwright-chromium` (já instalado em C:\temp-painel-erer).

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
