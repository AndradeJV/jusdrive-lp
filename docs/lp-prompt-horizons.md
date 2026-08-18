# JusDrive — Landing page (prompt para o Hostinger Horizons)

Arquitetura: **landing page em `jusdrive.com.br`** · **app em `app.jusdrive.com.br`**.
Todo botão de ação da LP aponta para `https://app.jusdrive.com.br`.

---

## PROMPT — cole no Horizons

Crie uma **landing page institucional de uma página** para o **JusDrive**, um organizador de arquivos ultra-simples para advogados autônomos. Posicionamento: "é como o Google Drive, mas jurídico". A unidade central é o PROCESSO: o advogado guarda PDFs, fotos, prints e vídeos dentro de cada processo e compartilha por link público com QR code.

O app em si NÃO faz parte deste site — ele fica no subdomínio `app.jusdrive.com.br`. Todos os botões de ação ("Entrar", "Criar minha conta grátis", "Assinar o Profissional") devem apontar para `https://app.jusdrive.com.br`.

Público: advogado autônomo, mais velho, pouco familiarizado com tecnologia. Linguagem simples e direta, sem jargão de tecnologia. Nenhum texto abaixo de 17px. Muito espaço em branco. Sem emoji, sem gradientes coloridos, sem ilustrações genéricas de startup.

### Identidade visual (use exatamente estes valores)
- Fundo da página (papel): `#F6F3EC`
- Cards e superfícies: `#FFFFFF`
- Texto principal: `#17233B`
- Primária (botões, faixa escura): `#1C2E4A` — hover `#17233B`
- Acento (logo, rótulos, detalhes): `#B0862F`
- Texto secundário: `#5A6472`
- Bordas: `#E4E7EC` · fundo de chip: `#EEF1F6` · rodapé: `#17233B`
- Fontes (Google Fonts): **Source Serif 4** 600 nos títulos de seção e no H1 (serifa institucional e sóbria — não use Spectral, Playfair nem fontes arredondadas); **IBM Plex Sans** 400/500/600/700 em todo o resto e no wordmark. Títulos com letter-spacing de -0.018em.
- Cantos: 8px em botões e cards pequenos, 14px em cards grandes. Sombras sutis: `0 1px 2px rgba(23,35,59,.05)` em cards, `0 18px 48px rgba(23,35,59,.12)` no mockup do hero.
- Largura de conteúdo: 1120px centralizados, padding lateral de 40px, 88px de padding vertical por seção.

### Logo
Ícone: quadrado de canto arredondado (raio 12 em viewBox 48) em `#1C2E4A`, com uma pasta fundida com nuvem em `#B0862F` dentro. Wordmark ao lado: "Jus" em `#17233B` + "Drive" em `#B0862F`, Inter 700, letter-spacing -0.02em. Arquivos PNG e SVG fornecidos junto.

### Seções, nesta ordem

**1. Cabeçalho fixo** — fundo papel com leve transparência e borda inferior. Logo à esquerda; links "Como funciona", "Compartilhar", "Planos" à direita em `#5A6472`; botão "Entrar" em `#1C2E4A`.

**2. Hero** — duas colunas. À esquerda: rótulo dourado em maiúsculas "ORGANIZE SEUS PROCESSOS"; H1 em Source Serif 4 58px: "Todos os arquivos de cada processo, num só lugar."; parágrafo 21px: "Guarde PDFs, fotos, prints e vídeos dentro do processo a que pertencem. Quando precisar mostrar ao cliente, envie um link ou o QR code. Sem pastas confusas, sem cadastro para quem recebe."; botão grande "Criar minha conta grátis" com o texto "Leva 2 minutos. Sem cartão." e "Planos a partir de R$ 59,90/mês." ao lado; abaixo, separados por uma linha, "Feito para advogado autônomo" e "Funciona no celular e no computador". À direita: mockup da tela do app — cabeçalho marinho com o logo, campo de busca, botão "+ Novo processo" e três cards de processo com barra lateral marinho de 4px, nome do processo, cliente, chip "12 arquivos" e "atualizado em 14 de agosto".

**Animação do mockup (importante):** o campo de busca simula alguém digitando. Em laço infinito: espere 1,8s, digite "Silva" letra por letra (190ms cada) com um cursor piscando ao lado e filtre a lista em tempo real — sobra só "Ação Trabalhista — Silva x Transportes Ipê", cujo card entra com fade e ganha barra lateral dourada. Segure 2,6s, apague as letras (80ms cada), espere 1,6s e repita. Enquanto há texto, o campo mostra um halo suave (box-shadow 0 0 0 3px rgba(28,46,74,.12)).

**3. Faixa branca "Onde estão os documentos daquele processo?"** — título em Spectral 38px e três colunas com subtítulo dourado em Spectral:
- *Hoje* — "Prints no WhatsApp, PDFs no e-mail, fotos na galeria do celular. Cada processo espalhado em quatro lugares."
- *Com o JusDrive* — "Um processo, uma pasta. Tudo que chega vai para dentro dele, no celular ou no computador."
- *Na hora de mostrar* — "Um link, ou um QR code para o cliente apontar a câmera. Ele vê os arquivos e não altera nada."

**4. Como funciona** (âncora `#como-funciona`) — rótulo "COMO FUNCIONA", título "Três passos, e pronto." e três cards brancos, cada um com um número em quadrado marinho (dígito dourado em Spectral):
1. **Crie o processo** — "Dê o nome do processo e o nome do cliente. É o único cadastro que existe."
2. **Junte os arquivos** — "Arraste PDFs ou envie fotos e prints direto do celular. Tudo fica dentro do processo."
3. **Compartilhe o link** — "Cada processo tem um link com QR code, somente leitura. Mande pelo WhatsApp e pronto."

**5. Faixa marinho `#1C2E4A` (âncora `#compartilhar`)** — duas colunas. À esquerda, sobre o marinho: rótulo dourado "LINK E QR CODE", título Spectral 40px branco "O cliente abre e vê. Nada para instalar.", parágrafo em `#C7CEDA`, e três itens com travessão dourado: "Somente leitura: ninguém apaga ou altera seus arquivos.", "Você desliga o link quando quiser.", "Funciona com PDF, foto, print e vídeo." À direita: um cartão branco reproduzindo a página pública do processo — logo no topo com "Somente leitura" à direita, rótulo "PROCESSO COMPARTILHADO", nome do processo, um bloco `#F6F3EC` com QR code e o endereço `jusdrive.com.br/p/4f2a` em dourado monoespaçado, e quatro arquivos em grade 2×2 com nome e tamanho.

**6. Planos** (âncora `#planos`) — título "Preço simples, como o produto.", subtítulo em duas linhas: "Comece grátis. Planos pagos a partir de R$ 59,90 por mês." / "Só o Premium tem os recursos de IA." Quatro cards em uma linha (grid de 4 colunas iguais; 2×2 no tablet, 1 coluna no celular). Cada card: nome (com selo ao lado quando houver), preço em Source Serif 4 38px seguido de "/mês" menor em cinza, divisória fina, lista de itens com travessão dourado, e botão de largura total no rodapé do card.

| Plano | Preço | Itens | Selo | Botão |
|---|---|---|---|---|
| Gratuito | R$ 0 /mês | 1 processo · 2 arquivos e vídeos · 1 modelo de peça · Sem IA | — | "Criar conta" (contornado) |
| Profissional | R$ 59,90 /mês | 9 processos · 30 arquivos e vídeos · 6 modelos de peça · Sem IA | — | "Assinar" (contornado) |
| **Ilimitado** | R$ 99,90 /mês | Processos ilimitados · Arquivos e vídeos ilimitados · Modelos ilimitados · Sem IA | "MAIS POPULAR" em chip `#EEF1F6` | "Assinar" (cheio, marinho) |
| Premium | R$ 149,90 /mês | Tudo do Ilimitado · Gerar petições com IA · Resumir processos com IA · Recursos ilimitados | "COM IA" em chip `#1C2E4A` com texto `#B0862F` | "Assinar" (contornado) |

O card **Ilimitado** é o destaque visual: borda 1.5px em `#B0862F` e sombra mais forte. O **Premium** tem borda marinho `#1C2E4A` (sem dourado) para se diferenciar sem competir.
Abaixo da grade: "Todos os planos incluem link com QR code e acesso pelo celular. Sem contrato de fidelidade, cancele quando quiser."

**7. CTA final** — faixa branca centralizada: "Organize o primeiro processo hoje.", subtítulo "Crie sua conta, envie os arquivos e mande o link para o cliente. Sem treinamento, sem manual." e botão grande "Criar minha conta grátis".

**8. Rodapé** `#17233B` — logo com ícone dourado, links "Entrar no app", "Planos", "contato@jusdrive.com.br", e a linha "© 2026 JusDrive. Todos os direitos reservados."

### Animações (discretas, nunca chamativas)
- **Entrada por scroll:** títulos e cards sobem 22px com fade em 0,7s (cubic-bezier(.22,.61,.36,1)), escalonados 90ms entre irmãos, via IntersectionObserver. O que já está visível no carregamento aparece sem animação.
- **Mockup do hero:** flutuação lenta e contínua, ±10px em 7s.
- **QR code:** halo dourado pulsando a cada 3,2s.
- **Cards (passos e planos):** no hover sobem 6px com sombra mais profunda; botões e links com transição de 0,2s.
- Respeite `prefers-reduced-motion: reduce`: com ele nada se move e nada fica escondido.

### SEO
- Title: `JusDrive — os arquivos de cada processo, organizados num só lugar`
- Description: `Organizador de arquivos para advogados. Guarde PDFs, fotos e vídeos dentro de cada processo e compartilhe por link com QR code. Grátis para começar.`
- Favicon: o ícone JusDrive (`jusdrive-icone-512.png`).

### Responsivo
No celular, todas as seções de duas ou três colunas viram uma coluna; o mockup do app entra abaixo do texto do hero; os botões ficam de largura total. O menu do cabeçalho vira um botão "Entrar" apenas.

---

## Imagens fornecidas (pasta `png/` e SVGs na raiz do pacote)

| Arquivo | Uso |
|---|---|
| `jusdrive-logo-fundo-claro.png` | logo do cabeçalho, fundo papel |
| `jusdrive-logo-fundo-marinho.png` | logo sobre faixas escuras e rodapé |
| `jusdrive-logo-fundo-branco.png` | logo sobre cards brancos |
| `jusdrive-icone-512.png` | favicon, ícone de app, redes sociais |
| `jusdrive-icone-invertido-512.png` | ícone sobre fundo escuro |
| `jusdrive-lp-referencia-final.png` | referência visual da LP inteira (1383×4071) — anexe no Horizons e peça "reproduza este layout" |

## Configuração de domínio
- `jusdrive.com.br` e `www.jusdrive.com.br` → esta landing page.
- `app.jusdrive.com.br` → o app (projeto separado no Horizons).
- No projeto do app, o logo do cabeçalho deve linkar para `https://jusdrive.com.br`.
