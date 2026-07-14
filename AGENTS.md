# AGENTS.md

Este repositório é o catálogo canônico de providers do Torii.

## Invariantes

- Pacotes são data-only: nunca adicione binários, scripts executáveis, hooks ou instaladores.
- O `rules.yaml` da raiz de todo pacote deve permanecer vazio: `deny: []` e `accept: []`.
- Políticas de exemplo ficam em `setups/<nome>/rules.yaml` e devem ser declaradas como `readonly` no manifest.
- Operações que retornam segredos, credenciais ou tokens não pertencem a accepts read-only.
- Cada release deve usar artifacts imutáveis e atualizar SHA-256, versão e URL no `index.yaml`.
- Não inclua credenciais, contas, clusters ou endpoints reais.

## Validação

Antes de publicar, instale cada diretório e archive com o Torii, aplique seus setups e confirme que update preserva a política ativa.
