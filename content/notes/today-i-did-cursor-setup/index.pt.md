+++
title = "Hoje configurei um workspace perfeito no Cursor para este site"
date = 2025-01-13
description = "Log rápido de como deixei meu ambiente de desenvolvimento ideal"

[taxonomies]
tags = ["ferramentas", "workflow", "cursor"]

[extra]
kind = "Log"
+++

Passei um tempo hoje deixando minha configuração do Cursor perfeita para trabalhar neste site Zola. Aqui está o que fez a maior diferença:

**Extensões que importam:**

- Even Better TOML (essencial para frontmatter)
- Zola syntax highlighting
- Live Server (para previews rápidos)

**Configurações do workspace:**

```json
{
  "files.associations": {
    "*.md": "markdown"
  },
  "markdown.preview.breaks": true
}
```

**O divisor de águas:** Configurei um snippet customizado para novos posts do blog que preenche automaticamente o template do frontmatter. Chega de copiar e colar datas ou esquecer campos obrigatórios.

**Integração com IA do Cursor:** A IA entende muito bem a estrutura do Zola agora que tenho trabalhado neste workspace. Ela sugere a sintaxe correta de shortcodes e pega erros no frontmatter.

Pequenas melhorias que se somam para uma experiência de escrita muito mais fluida. O atrito entre "quero escrever algo" e "estou realmente escrevendo" agora é quase zero.
