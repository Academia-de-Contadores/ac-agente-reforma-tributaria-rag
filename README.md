# Reforma Tributária Day — Consulta RAG

| Campo | Valor |
| --- | --- |
| ID | `ac.reforma-tributaria-rag` |
| Versão | `0.2.0` |
| Lifecycle | `candidate` |
| Skill | `$ac-reforma-tributaria-rag` |

## Propósito

Atua como assistente consultivo sobre a Reforma Tributária do Consumo com busca
RAG no corpus Day V2.3 via serviço externo conectado ao Chroma Cloud.

O repositório inteiro é o pacote-fonte da skill, com [SKILL.md](SKILL.md) na
raiz e apresentação em [agents/openai.yaml](agents/openai.yaml). A versão é
candidata; os validadores estruturais não comprovam a operação do serviço.

## Usar e manter este agente

Após instalar o pacote completo em uma pasta de skills reconhecida pelo Codex,
invoque:

```text
Use $ac-reforma-tributaria-rag para analisar minha dúvida sobre créditos de CBS,
consultando as fontes e indicando o que falta para concluir.
```

O perfil [current](profiles/current/profile.yaml) é o padrão. Para o RAG
legado/Reforma Oficial ou comparação histórica, solicite explicitamente o
perfil [legacy](profiles/legacy/profile.yaml). Ambos referenciam os anexos
preservados, sem duplicação. O perfil histórico não comprova vigência atual.

Leia [HOW-TO-USE.md](HOW-TO-USE.md) para instalação, transporte HTTP e
manutenção. O [contrato de retrieval](references/retrieval-contract.md) usa o
schema ativo capturado em 2026-09-20; `openapi.yaml` permanece candidato futuro.
A skill não instala a Action ou um MCP: exige ferramenta HTTP/Action disponível
para consultar o serviço externo. Na indisponibilidade ou falta de base,
declara a lacuna e não fecha conclusão normativa. Não envie dados de clientes
ou segredos. Decisões de aplicação exigem validação profissional.

## Guias do repositório

- [Como usar e reconstruir o agente](HOW-TO-USE.md)
- [Estrutura e destino de cada arquivo](docs/REPOSITORY-STRUCTURE.md)
- [Como contribuir](governance/CONTRIBUTING.md)
- [Política de dados e segredos](governance/DATA-AND-SECRETS.md)
- [Política de mudanças](governance/CHANGE-POLICY.md)

## Proteções versionadas e verificáveis

O `.gitignore` reduz o risco de adicionar artefatos locais conhecidos, e
`scripts/validate-agent-repo.sh` rejeita arquivos proibidos, artefatos RAG locais
e arquivos maiores que 5 MB. O workflow `validate` executa esse validador em
pull requests e pushes para `main`. O `CODEOWNERS` solicita revisão para áreas
sensíveis. Workflow e `CODEOWNERS`, isoladamente, não provam bloqueio de merge;
branch protection, rulesets, visibilidade e demais controles devem ser
confirmados na configuração remota. Consulte `reports/task-3-report.md` para a
evidência local e seus limites.
