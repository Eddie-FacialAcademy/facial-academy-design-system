# Facial Academy — Design System

Design system da **Facial Academy** (assinatura de HOF da Facial Academy). Marca de cor predominante **roxo `#644389`** (medium purple); tipografia **Silka** (embutida em woff2, headers em **Medium 500**).

Desenvolvido por **Edegar Junior**.

## Entregas

- **index.html** — design system reutilizável (showcase navegável): paleta (institucional + derivada), temas **dark/light**, tipografia (Silka), **gradientes**, **ícones** (Phosphor Thin, copiar SVG), **logos** (copiar/baixar SVG) e sistema de **botões** (variantes/tamanhos/estados); os botões fill/solid usam o token `--cta` (CTA escuro clareado para passar contraste de componente). Click-to-copy em cores, valores e código; download PNG dos gradientes.
  - 🌐 **Online (para compartilhar):** https://eddie-facialacademy.github.io/facial-academy-design-system/ — GitHub Pages (repo público `facial-academy-design-system`).

## Design System portátil (`design-system/`)

Pacote para aplicar a marca em **qualquer projeto/ferramenta** (web, React, Framer, agentes de IA).

- **silka.css** — fonte **Silka** (pesos 300–700) embutida em woff2/base64, self-contained; linke antes do CSS principal.
- **facial-academy-design-system.css** — drop-in (tokens dark/light, inclui CTA theme-aware via `--cta` (dark `#7C5EA7`, light `#644389`) + reset + foco + motion + tipografia + botões + chips/badges/status).
- **facial-academy-design-tokens.json** — tokens legíveis por máquina (Style Dictionary, Framer, IA).
- **Button.tsx** — Code Component Framer/React com Property Controls.
- **DESIGN-SYSTEM.md** — spec completa, 3 formas de aplicar e **prompt pronto para IA**.
- **THEME.md** — como o claro/escuro é configurado e ativado pelo tema do sistema do visitante (web + Framer).

## Notas técnicas

- **Cores:** derivadas das **7 cores institucionais** da Facial Academy: roxo `#644389`, lilás `#A289D7`, amarelo claro `#FFE4A4`, vermelho claro `#FFB1BD`, amarelado `#FFCA9B`, branco `#FFFFFF`, preto `#000000`.
- **Tipografia:** Silka (institucional), embutida em base64/woff2; Poppins como fallback (quando a Silka não estiver disponível), depois system-ui. **Headers em Medium (500)**; eyebrow 600; numeral 700; body 300.
- **Ícones:** biblioteca **Phosphor**, peso **Thin** (stroke 1pt na grade 24), `currentColor`.
- **Tema:** dark por padrão; light via `data-theme="light"`; sem atributo segue `prefers-color-scheme`. Toggle persiste em `fc-theme`.
- **Acessibilidade:** contraste em 2 níveis — (1) texto ≥4.5:1; (2) componente/botão vs fundo ≥3:1 (WCAG 1.4.11). O CTA do tema escuro foi clareado para `#7C5EA7` para passar o nível 2.

## Publicação

Repo público `facial-academy-design-system` (conta `Eddie-FacialAcademy`), branch `main`, `index.html` na raiz, GitHub Pages. `.git` fora do OneDrive (`AppData\Local\gitdirs\`); line-endings LF (`.gitattributes`). Deploy: editar → `git add/commit/push` (credencial no Cofre do Windows, sem token). Ver `HANDOFF.md`.

## CHANGELOG

- **1.0.0** — CTA do tema escuro clareado para `#7C5EA7` (gradiente `#7C5EA7`→`#6E51A0`; hover `#6E51A0`; texto branco) via token `--cta` (`--cta-grad`/`--cta-solid`/`--cta-solid-h`/`--cta-ink`); botões `.b.fill`/`.fc-btn.fc-fill` e solid passam a usar `--cta`; documentada acessibilidade em 2 níveis (texto ≥4.5:1; componente ≥3:1, WCAG 1.4.11).
