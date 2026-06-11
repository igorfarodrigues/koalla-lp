# Guia de Design e Estilo

Este guia documenta a identidade visual atual da landing page do Koalla.ai, conforme implementada em `index.html`.

## Direção visual

O visual do Koalla.ai combina:

- **Tecnologia acessível:** IA e automação sem parecer complexa.
- **Confiança e segurança:** base escura, contrastes controlados e foco em privacidade.
- **Produtividade cotidiana:** comunicação direta, WhatsApp como canal principal e cards funcionais.
- **Toque humano:** emoji de coala, linguagem simples e microinterações suaves.

## Paleta de cores

Tokens CSS atuais em `:root`:

| Token | Valor | Uso recomendado |
|---|---:|---|
| `--navy` | `#0b1526` | Fundo principal da página. |
| `--navy-mid` | `#0f1e36` | Seções alternadas e gradientes. |
| `--navy-light` | `#162845` | Cards, blocos e áreas elevadas. |
| `--blue-brand` | `#1a4fa8` | Azul institucional secundário. |
| `--blue-accent` | `#2563eb` | CTAs, ícones principais e destaques. |
| `--blue-glow` | `#3b82f6` | Glow, foco acessível e efeitos. |
| `--gold` | `#c9a84c` | Destaques premium e `.ai` da marca. |
| `--gold-light` | `#e8c76a` | Destaques dourados claros. |
| `--white` | `#f0f4ff` | Texto principal sobre fundo escuro. |
| `--white-dim` | `rgba(240,244,255,0.7)` | Texto secundário. |
| `--white-muted` | `rgba(240,244,255,0.35)` | Metadados, notas e detalhes. |
| `--border` | `rgba(255,255,255,0.07)` | Bordas discretas. |
| `--card-bg` | `rgba(22,40,69,0.6)` | Fundo translúcido de cards. |

### Regras de uso

- Use `--blue-accent` para ações primárias e elementos clicáveis importantes.
- Use `--gold` com parcimônia para reforçar marca, plano em destaque ou pontos premium.
- Evite adicionar novas cores sem transformar em token no `:root`.
- Em fundos escuros, garanta contraste suficiente usando `--white` ou `--white-dim`.

## Tipografia

Fontes carregadas via Google Fonts:

- **Sora:** títulos, marca, preços e elementos de alta hierarquia.
- **DM Sans:** corpo de texto, descrições, listas e navegação.

### Hierarquia atual

| Elemento | Família | Peso | Observação |
|---|---|---:|---|
| Logo `Koalla.ai` | Sora | 700 | `.ai` em dourado. |
| Hero `h1` | Sora | 800 | Usa `clamp()` e destaque com gradiente. |
| Títulos de seção `.section-title` | Sora | 800 | `letter-spacing: -0.02em`. |
| Labels `.section-label` | DM Sans | 700 | Caixa alta, tracking amplo. |
| Corpo e descrições | DM Sans | 400/500 | Legibilidade e tom conversacional. |
| Preços `.price-amount` | Sora | 800 | Forte impacto comercial. |

## Layout e espaçamento

- Container principal: `.container` com `max-width: 1100px`.
- Padding desktop: `0 48px` em containers e navegação.
- Padding mobile: `0 20px` e navegação com `16px 20px`.
- Seções principais usam cerca de `100px` de padding vertical.
- Cards geralmente usam `border-radius` entre `12px` e `28px`.
- Grids usam `gap` generoso, normalmente entre `24px` e `80px`.

## Componentes principais

### Navegação

- `nav` fixo no topo com fundo translúcido e `backdrop-filter`.
- Links internos apontam para seções por `id`.
- CTA principal: `.nav-cta`.
- Menu mobile usa botão `.hamburger` com `aria-expanded`.

### Hero

- Deve comunicar a promessa em até poucos segundos.
- Headline atual: `Registre. Organize. Encontre Tudo.`
- CTA principal deve apontar para WhatsApp ou checkout, conforme fase do produto.
- Mockup mostra a experiência de conversa + categorização.

### Cards

- Usar fundos translúcidos, bordas discretas e sombras leves.
- Cards devem ter ícone/emoji, título curto e descrição objetiva.
- Evitar excesso de texto dentro de cards.

### Pricing

- Planos atuais: Starter, Pro e Business.
- O plano Pro usa destaque visual com `.featured` e badge `Mais popular`.
- Qualquer mudança de preço deve ser refletida também em `README.md` e `docs/content-guide.md`.

### CTA final

- Deve reforçar a ação principal.
- Manter botões claros: uma ação primária e, no máximo, uma secundária.

## Motion e interação

- Scroll reveal usa `.reveal` e `.visible` com `IntersectionObserver`.
- Transições devem ser suaves e curtas, entre `0.2s` e `0.7s`.
- Evite animações que prejudiquem leitura ou performance.

## Responsividade

Breakpoint atual:

```css
@media (max-width: 768px) {
  /* regras mobile */
}
```

No mobile:

- Grids viram uma coluna.
- Menu vira tela cheia.
- Sidebar do mockup é ocultada.
- Footer vira coluna centralizada.

## Acessibilidade visual

- Manter `:focus-visible` em elementos interativos.
- Ícones decorativos devem usar `aria-hidden="true"`.
- Textos importantes não devem depender apenas de cor.
- Links e botões devem ter labels compreensíveis.

## Checklist antes de alterar design

- [ ] A mudança usa tokens existentes ou adiciona token no `:root`?
- [ ] O contraste continua adequado em fundo escuro?
- [ ] A seção funciona no breakpoint de `768px`?
- [ ] O CTA principal continua evidente?
- [ ] A mudança mantém o tom premium, simples e confiável?

