# Padrões do Projeto

Este documento define regras práticas para manter a landing page do Koalla.ai consistente, simples de evoluir e fácil de revisar.

## Stack atual

- HTML5 semântico.
- CSS inline dentro de `<style>` em `index.html`.
- JavaScript vanilla ao final do arquivo.
- Google Fonts: Sora + DM Sans.
- Sem framework e sem dependências externas de build.

## Estrutura de arquivos

```text
koalla-lp/
├── index.html                 # Página principal/publicável
├── pages/
│   └── koalla-landing.html    # Cópia ou variação da landing
├── docs/                      # Documentação de design, conteúdo e padrões
└── README.md                  # Visão geral do projeto
```

### Regra de fonte de verdade

- Trate `index.html` como a versão principal da landing page.
- Antes de editar `pages/koalla-landing.html`, confirme se ele ainda precisa existir como cópia separada.
- Se houver mudanças nos dois arquivos, mantenha-os sincronizados ou documente claramente a diferença.

## Padrões de HTML

- Usar HTML semântico sempre que possível: `nav`, `section`, `footer`, `h1`, `h2`, listas e botões reais.
- Cada seção principal deve ter comentário em caixa alta, seguindo o padrão atual:

```html
<!-- FUNCIONALIDADES -->
<section class="features" id="funcionalidades">
```

- Seções navegáveis devem ter `id` claro em português, por exemplo:
  - `como-funciona`
  - `funcionalidades`
  - `planos`
  - `cta`
- Links externos devem usar:

```html
target="_blank" rel="noopener"
```

- Elementos puramente decorativos devem ter `aria-hidden="true"`.
- Evitar texto essencial dentro de `style` inline ou apenas em imagens.

## Padrões de CSS

- Manter tokens globais em `:root`.
- Reutilizar variáveis antes de criar novas cores.
- Seguir a organização atual por blocos:
  - Focus styles
  - Noise overlay
  - Nav
  - Hero
  - Sections
  - How it works
  - Features
  - WhatsApp
  - Testimonials
  - Pricing
  - CTA final
  - Footer
  - Responsive
- Usar nomes de classes curtos, semânticos e consistentes com o padrão existente:
  - `.section-title`
  - `.section-desc`
  - `.feature-item`
  - `.price-card`
  - `.btn-primary`
- Evitar alterar formatação de blocos não relacionados à mudança.
- Evitar adicionar bibliotecas CSS enquanto o projeto estiver simples e estático.

## Padrões de JavaScript

JavaScript atual cobre:

- Scroll reveal com `IntersectionObserver`.
- Sombra da navegação no scroll.
- Menu hamburger mobile.

Regras:

- Usar JavaScript vanilla.
- Inserir scripts perto do final do `body`, como já acontece.
- Conferir existência dos elementos antes de manipular, caso uma seção se torne opcional.
- Evitar dependências externas para interações simples.
- Preservar atributos de acessibilidade como `aria-expanded`.

## Responsividade

- Breakpoint principal atual: `max-width: 768px`.
- Toda nova seção deve ser testada em desktop e mobile.
- Grids complexos devem virar uma coluna no mobile.
- Evitar larguras fixas sem `max-width`.
- Não esconder conteúdo essencial em telas pequenas.

## Acessibilidade

Checklist mínimo:

- [ ] A página mantém apenas um `h1` principal.
- [ ] CTAs têm texto claro e acionável.
- [ ] Links externos têm `rel="noopener"`.
- [ ] Botões interativos usam `<button>` quando não são navegação.
- [ ] Elementos decorativos têm `aria-hidden="true"`.
- [ ] O menu mobile atualiza `aria-expanded` corretamente.
- [ ] O foco visível não foi removido.

## SEO e compartilhamento

Ao alterar posicionamento ou headline, revisar:

- `<title>`
- `<meta name="description">`
- Open Graph:
  - `og:title`
  - `og:description`
  - `og:url`
  - `og:image`
- Twitter Card:
  - `twitter:title`
  - `twitter:description`

## Placeholders obrigatórios antes de publicar

Antes de publicar em produção, substituir:

- `55XXXXXXXXXXX` pelo WhatsApp real do Koalla.ai.
- Links `#` de `Privacidade` e `Termos` por URLs reais.
- `https://koalla.ai/og-image.png` por uma imagem real publicada.
- Link de checkout do plano Pro, se não for via WhatsApp.

## Checklist de revisão antes de commit/publicação

- [ ] `index.html` abre corretamente no navegador.
- [ ] Navegação por âncoras funciona.
- [ ] Menu mobile abre e fecha.
- [ ] CTAs apontam para destino correto.
- [ ] Textos e preços estão sincronizados com `README.md` e `docs/content-guide.md`.
- [ ] Não há placeholders críticos sem intenção.
- [ ] Documentação em `docs/` foi atualizada se houve mudança de padrão.

