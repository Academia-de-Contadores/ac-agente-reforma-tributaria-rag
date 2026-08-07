---
title: Lacunas e roadmap - Agente Reforma Tributaria
type: knowledge-roadmap
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

# Lacunas e roadmap - Agente Reforma Tributaria

## Lacunas atuais
- Validar prompt v2 no ambiente final do agente ou GPT Builder.
- Rodar matriz de testes v2 com respostas reais, nao apenas revisao de desenho.
- Confirmar fontes canonicas com Arquivista Senior.
- Confirmar riscos com Contador Senior.
- Confirmar se a Action Day/Reforma retorna `retrieved_chunks`, `citations`, `source_status`, `gaps` e `recommended_response_rules` quando acionada.
- Registrar se RAG segue como referencia existente ou se virou necessidade real por volume/fonte.

## Decisao RAG atual
`manter_existente_referencia` - nao reconstruir; usar como referencia de guardrails e fonte vigente.

## Criterio para mudar a decisao RAG

So reabrir RAG se houver uma destas evidencias:

- o Knowledge Pack nao suporta recuperar fonte ou trecho especifico;
- os casos reais exigem citacao granular de lei, manual, nota tecnica, tabela ou versao;
- a Action Day/Reforma nao consegue devolver fonte, lacuna e regra de resposta de forma confiavel;
- ha conflito recorrente entre materiais internos e fonte oficial;
- os demais agentes comecam a responder Reforma sem acionar a camada correta.

## Roadmap
1. Revisao por thread especializada.
2. Ajustes de prompt v2.
3. Testes de casos reais.
4. QA de claims.
5. Handoff para configuracao no builder/agente.
