# JusDrive — Landing Page

Organizador de arquivos ultra-simples para advogados autônomos: "é como o Google Drive, mas jurídico". A unidade central é o **processo** — o advogado guarda PDFs, fotos, prints e vídeos dentro de cada processo e compartilha com o cliente por link público com QR code.

Este repositório reúne o **protótipo visual da landing page**, os **ativos de marca** e os **prompts de especificação** usados para construir o site institucional (`jusdrive.com.br`), que é separado do app do produto (`app.jusdrive.com.br`).

## Estrutura

```
design/     Protótipos interativos (Design Canvas — precisam de support.js para rodar)
brand/      Identidade visual: logos (svg) e exports (png)
docs/       Prompts de especificação e referências visuais
```

### `design/`

| Arquivo | Descrição |
|---|---|
| `landing-page.dc.html` | Protótipo da LP institucional, mobile-first, 9 seções (hero → CTA final) |
| `brand-comparison.dc.html` | Estudo comparativo de identidade visual (duas propostas de marca lado a lado) |
| `logo-export.dc.html` | Artboard de exportação do logo em variações |
| `support.js` | Runtime do Design Canvas — obrigatório e compartilhado pelos três `.dc.html` acima |

Para visualizar: abra qualquer `.dc.html` desta pasta num navegador (ou sirva a pasta com um servidor estático local). Os três arquivos dependem do `support.js` ao lado — não mova um sem o outro.

### `brand/`

- `logo/` — logo e ícone em SVG (fundo claro, fundo marinho, transparente, invertido)
- `png/` — exports em PNG (favicon/ícone 512px, logo em fundo branco/claro/marinho, referência completa da LP em `jusdrive-lp-referencia-final.png`)

### `docs/`

- `lp-prompt-horizons.md` — especificação completa da landing page (paleta, tipografia, copy, seções, animações, responsivo) para gerar o site no Hostinger Horizons
- `app-prompt-horizons.md` — especificação equivalente para o app
- `reference/app-planos-atual.png` — captura de tela da tela de planos do app em produção, usada como referência de copy/estados ao desenhar a seção Planos da LP

## Identidade visual

| Token | Valor |
|---|---|
| Fundo (papel) | `#F6F3EC` |
| Cards / superfícies | `#FFFFFF` |
| Texto principal | `#17233B` |
| Primária (botões, faixas) | `#1C2E4A` — hover `#17233B` |
| Acento (logo, rótulos) | `#B0862F` |
| Texto secundário | `#5A6472` |
| Bordas | `#E4E7EC` |

Fontes: **Source Serif 4** (600) em títulos, **IBM Plex Sans** no restante.

## Arquitetura de domínio

- `jusdrive.com.br` → landing page (este projeto)
- `app.jusdrive.com.br` → aplicação do produto (projeto separado)

Todo CTA da landing page aponta para `https://app.jusdrive.com.br`.
