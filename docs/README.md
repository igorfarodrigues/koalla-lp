# Documentação do Koalla.ai

Esta pasta centraliza as decisões de produto, design, conteúdo e desenvolvimento da landing page do Koalla.ai.

## Por que `docs/`?

`docs/` é um padrão simples e amplamente usado para documentação técnica e de produto. Para este projeto, ela funciona como a fonte de verdade para:

- Guia de design e estilo visual.
- Regras de implementação da landing page.
- Tom de voz, mensagens e conteúdo comercial.
- Orientações para uso de IA no projeto.

> Sugestão complementar: se o projeto passar a usar agentes de IA com frequência, pode ser criado também um arquivo `AGENTS.md` na raiz apontando para estes guias. A pasta `docs/` deve continuar sendo a documentação principal.

## Guias disponíveis

| Documento | Objetivo |
|---|---|
| [`design-guide.md`](./design-guide.md) | Tokens visuais, cores, tipografia, componentes e direção estética. |
| [`project-standards.md`](./project-standards.md) | Padrões de estrutura, HTML, CSS, JavaScript, acessibilidade e responsividade. |
| [`content-guide.md`](./content-guide.md) | Posicionamento, tom de voz, CTAs, planos, textos e placeholders. |
| [`ai-guidelines.md`](./ai-guidelines.md) | Regras para pedir, revisar e aplicar mudanças feitas com apoio de IA. |

## Estrutura atual do projeto

```text
koalla-lp/
├── index.html
├── pages/
│   └── koalla-landing.html
├── docs/
│   ├── README.md
│   ├── design-guide.md
│   ├── project-standards.md
│   ├── content-guide.md
│   └── ai-guidelines.md
└── README.md
```

## Fonte de verdade

- `index.html` deve ser tratado como a página principal publicada.
- `pages/koalla-landing.html` parece ser uma cópia/variação da landing atual. Antes de alterar uma seção, confirme se a mudança precisa ser replicada nos dois arquivos ou se o projeto deve consolidar apenas `index.html`.
- Este diretório `docs/` deve ser atualizado sempre que uma decisão visual, textual ou técnica mudar.

## Como usar estes documentos

Antes de criar ou alterar qualquer seção da landing page:

1. Leia [`design-guide.md`](./design-guide.md) para manter consistência visual.
2. Leia [`content-guide.md`](./content-guide.md) para manter tom de voz e promessa do produto.
3. Siga [`project-standards.md`](./project-standards.md) ao editar HTML/CSS/JS.
4. Se estiver usando IA, use [`ai-guidelines.md`](./ai-guidelines.md) como checklist de qualidade.

