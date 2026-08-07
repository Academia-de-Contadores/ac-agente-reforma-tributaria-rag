---
title: Indice - Agente Reforma Tributaria
type: knowledge-index
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

# Indice - Agente Reforma Tributaria

## Papel do agente
Este agente deve servir como referencia tecnica para CBS, IBS, split, creditos, DFe/XML, ERP e cronograma 2026-2033.

## Leitura recomendada
1. `01-REGRAS-DE-USO-E-LIMITES.md`
2. `02-ESCOPO-E-ROTEAMENTO.md`
3. `03-FONTES-CANONICAS.md`
4. `04-SKILLS-E-CENARIOS-DE-USO.md`
5. `05-PERGUNTAS-TESTE-E-RESPOSTAS-ESPERADAS.md`
6. `06-GUARDRAILS-E-CLAIMS-BLOQUEADOS.md`
7. `07-MODELOS-DE-RESPOSTA-E-CHECKLISTS.md`
8. `08-LACUNAS-E-ROADMAP.md`
9. `09-GUARDRAILS-PARA-OUTROS-AGENTES.md`
10. `99-FONTES-LACUNAS-E-CONTROLE-DE-VERSAO.md`

## Skills principais
- CBS
- IBS
- split payment
- creditos
- DFe
- XML
- ERP
- cClassTrib
- cronograma
- fonte oficial

## Decisao RAG
`manter_existente_referencia` - nao reconstruir; usar como referencia de guardrails e fonte vigente.

## Regra de ouro
Se faltar dado critico ou houver risco tecnico, o agente deve pedir dados e orientar revisao humana.

## Uso pelos demais agentes
Os agentes Concierge, Fiscal, Onboarding, Contabil, Comercial, Conteudo/DAI e Notion/Gestao devem consultar `09-GUARDRAILS-PARA-OUTROS-AGENTES.md` quando a demanda envolver CBS, IBS, split payment, creditos, DFe/XML, ERP, cClassTrib ou cronograma 2026-2033.
