---
title: Fontes canonicas - Agente Reforma Tributaria
type: knowledge-sources
status: draft
produto: Desafio Contadora CEO com IA
pilar: agentes
departamento: Reforma Tributaria
fonte_tipo: curadoria
origem: agents/knowledge
data_criacao: 2026-07-04
data_consulta: 2026-07-04
entra_no_rag: reference_only
confiabilidade: interna_curada
tags:
  - academia-contadores/dcceo/agentes
---

# Fontes canonicas - Agente Reforma Tributaria

## Fontes deste agente
| # | Fonte | Status RAG | Uso |
|---|---|---|---|
| 1 | agents/reforma/_curated | reference_only | fonte para curadoria/operacao |
| 2 | 04_PESQUISA_EXTERNA_DEEP_SEARCH/08_REFORMA_TRIBUTARIA_DAY_RAG | reference_only | fonte para curadoria/operacao |
| 3 | 06_PROMPTS_AGENTES_E_RAG/07_RAG_RELATORIO_OPERACAO_ESCRITORIO | reference_only | fonte para curadoria/operacao |

## Regra de fonte
- Fonte bruta ZIP/PDF/DOCX: `nao` entra no Git curado.
- Knowledge Pack: base operacional principal.
- Prompt v2: candidato para uso no builder.
- RAG: somente se gate justificar.

## Hierarquia obrigatoria de fonte

Quando a pergunta depender de regra, prazo, tabela, leiaute, classificacao, documento fiscal, cronograma, aliquota, decreto, nota tecnica ou aplicacao operacional, a ordem de autoridade deve ser:

1. fonte oficial vigente: Constituicao, emenda constitucional, lei complementar, decreto, resolucao, portaria, nota tecnica, manual ou tabela oficial;
2. portal oficial ou manual tecnico com versao identificavel;
3. corpus Day/Reforma aprovado, quando ele trouxer citacoes, lacunas e status da fonte;
4. Knowledge Pack interno, apenas como organizacao operacional;
5. material de aula, prompt ou marketing, apenas como apoio pedagogico.

Se houver conflito, a fonte oficial vigente vence. Se nao houver fonte versionada disponivel, o agente deve marcar lacuna e nao fechar resposta tecnica.

## Quando exigir fonte vigente

Exigir fonte vigente antes de responder conclusivamente quando aparecer:

- CBS, IBS, Imposto Seletivo ou cronograma 2026-2033;
- DFe/XML, NF-e, NFC-e, NFS-e, CT-e, BP-e, NFCom ou NF3e;
- ERP, emissor, leiaute, integracao, schema ou campo de documento fiscal;
- CST, cClassTrib, IndOp, NCM, NBS ou tabela de classificacao;
- split payment, creditos, cashback ou regime de transicao;
- aliquota, prazo, obrigatoriedade, penalidade ou guia.

## Lacuna padrao
Se a fonte nao existir, estiver duplicada, sem transcricao ou sem revisao humana, marcar como lacuna e nao usar como fundamento final.
