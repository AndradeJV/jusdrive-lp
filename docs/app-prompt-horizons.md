# JusDrive — pacote para colar no Hostinger Horizons

## 1. PROMPT PRINCIPAL (cole isso no Horizons)

Crie um web app chamado **JusDrive** — um organizador de arquivos ultra-simples para advogados autônomos, mais velhos e pouco familiarizados com tecnologia. Posicionamento: "é como o Google Drive, mas jurídico". A unidade central é o PROCESSO: o advogado cria um processo e guarda dentro dele arquivos (PDFs, fotos, prints, vídeos), e compartilha por link público com QR code.

Sensação: sóbrio, confiável e elegante — como uma pasta de dossiê, mas moderna, leve e arejada. Nada de gradientes coloridos, nada de emoji, nada de visual "startup genérica".

### Sistema visual (use exatamente estes valores)
- Fundo da página (papel): #F6F3EC
- Cards e superfícies: #FFFFFF
- Texto principal (tinta): #17233B
- Cor primária (botões, cabeçalho): #1C2E4A — hover #17233B
- Acento premium (logo, detalhes, ícones): #B0862F
- Texto secundário: #5A6472
- Bordas: #E4E7EC / divisórias #EEF1F4
- Fundo de chip/badge: #EEF1F6
- Fontes (Google Fonts): **Inter** para marca, títulos e interface (400/500/600/700); **Spectral** apenas para números de processo e citações.
- Raio de canto: 8px em inputs, botões e cards; 10–14px em contêineres grandes.
- Sombras muito sutis: 0 1px 2px rgba(23,35,59,.05) em cards; 0 6px 24px rgba(23,35,59,.07) em contêineres.
- Muito espaço em branco: padding de 32px nas seções, gap de 16–24px entre cards.

### Regras de UI (público pouco técnico)
- Uma ação principal por tela, em botão grande de largura total, 20px, peso 600.
- Nenhum texto abaixo de 17px (exceto rótulos maiúsculos de 15px).
- Alto contraste, linguagem simples e direta, sem jargão de tecnologia ("arquivos", não "assets"; "link", não "URL").
- Alvos de toque com no mínimo 44px de altura.

### Telas
**1. Meus Processos (privada)**
- Cabeçalho marinho #1C2E4A com o logo JusDrive à esquerda e avatar quadrado dourado (#B0862F, raio 10px, iniciais em #1C2E4A) à direita.
- Campo de busca branco, largura total, com ícone de lupa: "Buscar por processo ou cliente".
- Botão principal grande: "+ Novo processo" (#1C2E4A, texto branco, largura total).
- Título "Meus processos" com contagem à direita ("4 processos").
- Lista de cards grandes, um por linha, cada um com: barra lateral esquerda de 4px em #1C2E4A (vira #B0862F no hover), nome do processo (20px, peso 600), nome do cliente (17px, #5A6472), um chip "12 arquivos" (#EEF1F6, texto #1C2E4A) ao lado de "atualizado em 14 de agosto", e uma seta › dourada à direita.

**2. Página de link compartilhado (pública, somente leitura)**
- Topo branco com o logo JusDrive e, à direita, o texto discreto "Somente leitura".
- Rótulo dourado em maiúsculas: "PROCESSO COMPARTILHADO".
- Nome do processo em 30px peso 700, e abaixo "Cliente: … · 12 arquivos".
- Bloco destacado em #1C2E4A com o QR code em cartão branco à esquerda, e à direita "Aponte a câmera do celular" + o endereço curto (ex.: jusdrive.com.br/p/4f2a) em dourado, fonte monoespaçada.
- Grade de arquivos em 2 colunas: cards brancos com miniatura no topo (110px) e, abaixo, nome do arquivo (17px, peso 600) e metadados ("PDF · 1,2 MB").
- Botão grande no rodapé: "Baixar todos os arquivos".

Sem cadastro para quem abre o link. A página pública não mostra nenhum controle de edição.

## 2. LOGO

Arquivos SVG nesta pasta:
- `jusdrive-logo-fundo-claro.svg` — logo completo sobre papel #F6F3EC
- `jusdrive-logo-fundo-marinho.svg` — logo completo sobre #1C2E4A
- `jusdrive-logo-transparente.svg` — logo completo sem fundo
- `jusdrive-icone.svg` — só o ícone (marinho com pasta+nuvem dourada) — use como favicon
- `jusdrive-icone-invertido.svg` — ícone dourado com desenho marinho

### Código do ícone (cole direto no HTML se precisar)

```html
<svg viewBox="0 0 48 48" width="40" height="40">
  <rect x="2" y="2" width="44" height="44" rx="12" fill="#1C2E4A"/>
  <circle cx="20" cy="17" r="4.6" fill="#B0862F"/>
  <circle cx="27.5" cy="16" r="6" fill="#B0862F"/>
  <path d="M11 20.5a3 3 0 0 1 3-3h5.6l2.2 2.6H34a3 3 0 0 1 3 3v9.4a3 3 0 0 1-3 3H14a3 3 0 0 1-3-3z" fill="#B0862F"/>
</svg>
```

### Wordmark em HTML

```html
<span style="font-family:Inter,sans-serif;font-size:24px;font-weight:700;letter-spacing:-0.02em;color:#17233B">Jus<span style="color:#B0862F">Drive</span></span>
```

Regras: "Jus" na cor da tinta (ou branco sobre marinho), "Drive" sempre em #B0862F. Nunca separar as duas palavras nem inserir espaço. Espaço livre em volta do logo = altura do ícone ÷ 2.

## 3. TOKENS PRONTOS (CSS)

```css
:root{
  --papel:#F6F3EC; --superficie:#FFFFFF;
  --tinta:#17233B; --primaria:#1C2E4A; --primaria-hover:#17233B;
  --acento:#B0862F; --secundario:#5A6472;
  --borda:#E4E7EC; --divisoria:#EEF1F4; --chip:#EEF1F6;
  --raio:8px; --raio-lg:14px;
  --sombra-card:0 1px 2px rgba(23,35,59,.05);
  --sombra-painel:0 6px 24px rgba(23,35,59,.07);
  --fonte-ui:'Inter',system-ui,sans-serif;
  --fonte-serif:'Spectral',Georgia,serif;
}
```

```html
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Spectral:wght@400;600&display=swap" rel="stylesheet">
```

## 4. TEXTOS DA INTERFACE (verbatim)

- Botão principal: `+ Novo processo`
- Busca: `Buscar por processo ou cliente`
- Título da lista: `Meus processos`
- Card: `12 arquivos` · `atualizado em 14 de agosto`
- Página pública: `Somente leitura` · `PROCESSO COMPARTILHADO` · `Aponte a câmera do celular` · `Baixar todos os arquivos`
- Estado vazio: `Você ainda não tem processos. Toque em "+ Novo processo" para começar.`
