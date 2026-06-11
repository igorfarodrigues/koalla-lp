# Guia para Uso de IA no Projeto

Este documento define como usar IA para evoluir a landing page do Koalla.ai sem perder consistência visual, textual e técnica.

## Objetivo

A IA deve ajudar a acelerar criação, revisão e manutenção, mas as decisões finais devem respeitar os guias do projeto:

- [`design-guide.md`](./design-guide.md)
- [`project-standards.md`](./project-standards.md)
- [`content-guide.md`](./content-guide.md)

## Regras gerais

Ao pedir alterações para uma IA:

1. Informe que `index.html` é a página principal.
2. Peça para preservar o estilo visual existente.
3. Peça para consultar os arquivos em `docs/` antes de mudar design, conteúdo ou padrões.
4. Peça mudanças pequenas e verificáveis.
5. Evite aceitar reescritas completas sem necessidade.

## Prompt base recomendado

```text
Antes de alterar o projeto, leia os guias em docs/.
Trate index.html como a landing page principal.
Preserve o estilo visual atual: fundo navy, CTAs azuis, destaques dourados, fontes Sora e DM Sans.
Faça a menor alteração necessária, mantendo HTML semântico, acessibilidade e responsividade.
Depois de editar, valide links, placeholders e comportamento mobile quando aplicável.
```

## Checklist para revisar respostas de IA

- [ ] A IA alterou apenas os arquivos necessários?
- [ ] O design segue `docs/design-guide.md`?
- [ ] O texto segue `docs/content-guide.md`?
- [ ] O HTML/CSS/JS segue `docs/project-standards.md`?
- [ ] A mudança mantém responsividade em `max-width: 768px`?
- [ ] CTAs e links de WhatsApp continuam corretos?
- [ ] Placeholders foram mantidos/substituídos conscientemente?
- [ ] A documentação foi atualizada quando houve mudança de padrão?

## Tarefas boas para IA

- Criar variações de copy para headlines e CTAs.
- Propor novas seções com base no estilo atual.
- Revisar consistência de planos e preços.
- Encontrar placeholders antes de publicação.
- Melhorar acessibilidade de componentes existentes.
- Sugerir microinterações simples em JavaScript vanilla.
- Criar documentação e checklists.

## Tarefas que exigem cuidado extra

- Alterar preços, promessas comerciais ou termos legais.
- Criar depoimentos que pareçam reais sem autorização.
- Adicionar bibliotecas externas.
- Reestruturar todo o HTML.
- Substituir o sistema visual por outro.
- Publicar links de WhatsApp, checkout, privacidade ou termos sem validação.

## Padrão para novas seções geradas por IA

Toda nova seção deve incluir:

- Comentário HTML em caixa alta.
- `section` com classe semântica.
- Título claro.
- Descrição curta.
- Layout responsivo.
- Classes compatíveis com o estilo atual.
- Atributos de acessibilidade em elementos decorativos.

Exemplo de estrutura:

```html
<!-- NOVA SEÇÃO -->
<section class="nova-secao" id="nova-secao">
  <div class="container">
    <span class="section-label">Label</span>
    <h2 class="section-title">Título da seção</h2>
    <p class="section-desc">Descrição curta e objetiva.</p>
  </div>
</section>
```

## Como registrar decisões feitas com IA

Se uma mudança criar um novo padrão, atualizar a documentação:

- Novo componente visual → `design-guide.md`
- Nova regra técnica → `project-standards.md`
- Novo tom, oferta ou mensagem → `content-guide.md`
- Novo processo de uso de IA → este arquivo

## Sugestão futura

Se o projeto passar a usar agentes de IA com frequência, criar um `AGENTS.md` na raiz com instruções curtas apontando para estes documentos:

```markdown
# Instruções para agentes de IA

Antes de editar o projeto, leia `docs/README.md` e siga os guias em `docs/`.
`index.html` é a página principal da landing page.
```

