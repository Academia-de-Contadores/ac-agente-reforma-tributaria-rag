# Validação da instalação limpa — 2026-09-20

## Origem e destino

- Repositório: `https://github.com/Academia-de-Contadores/ac-agente-reforma-tributaria-rag.git`
- Worktree de origem: `/Volumes/SSD-500GB-1/chat/Projetos-codex/gptspersonalizados/agent-repos/ac-agente-reforma-tributaria-rag/.worktrees/rag-skill-ready`
- Branch de origem: `feat/rag-skill-ready`
- Commit-fonte exato: `a1ea42e2ab7019bafe5a9942cbcfa4af9e385b55`
- Destino: `/Users/levy/.codex/skills/ac-reforma-tributaria-rag`
- Estado inicial do destino: ausente (`test ! -e ...` retornou `0`)

## Conteúdo instalado

A instalação foi feita por cópia local seletiva. Somente os itens autorizados foram copiados:

- `SKILL.md`
- `agent.yaml`
- `agents/`
- `profiles/`
- `references/`
- `instructions/`
- `knowledge/`
- `connectors/`

O destino final contém 60 arquivos em 16 diretórios. Uma comparação recursiva com `diff -qr` confirmou paridade byte a byte entre cada item autorizado da origem e sua contraparte instalada.

## Conteúdo excluído

Nenhum outro item do repositório foi instalado. Isso exclui explicitamente `.git`, `.github`, `.superpowers`, caches, `scripts/`, `tests/`, `evaluations/`, `reports/`, `governance/`, `docs/`, documentação de manutenção e os demais diretórios ou arquivos de desenvolvimento na raiz (`adapters/`, `decisions/`, `identity/`, `objectives/`, `skills/`, `.gitignore`, `CHANGELOG.md`, `HOW-TO-USE.md` e `README.md`).

A inspeção do topo do destino encontrou exatamente os oito itens autorizados. Uma busca dedicada também confirmou a ausência de `.git`, `.github`, `.superpowers`, `scripts`, `tests`, `evaluations`, `reports`, `governance`, `docs`, `__pycache__` e `.pytest_cache` em qualquer profundidade.

## Validação fora do workspace

O validador foi executado a partir de `/tmp`, usando o interpretador vinculante com PyYAML:

```text
/Users/levy/.pyenv/versions/3.10.13/bin/python3 \
  /Users/levy/.codex/skills/.system/skill-creator/scripts/quick_validate.py \
  /Users/levy/.codex/skills/ac-reforma-tributaria-rag
```

Resultado:

```text
Skill is valid!
```

Assim, a skill instalada carrega pelo destino do Codex sem depender do diretório de trabalho do repositório original.
