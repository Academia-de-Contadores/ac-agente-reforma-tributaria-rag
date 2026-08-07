---
title: Guardrails Reforma para outros agentes
type: knowledge-guardrails-cross-agent
status: draft
produto: Desafio Contadora CEO com IA
pilar: agentes
departamento: Reforma Tributaria
fonte_tipo: qa_referencia
origem: knowledge/reforma
data_criacao: 2026-07-04
data_consulta: 2026-07-04
entra_no_rag: reference_only
confiabilidade: interna_curada
tags:
  - academia-contadores/dcceo/agentes
---

# Guardrails Reforma para outros agentes

## Quando chamar Reforma

Os demais agentes devem encaminhar, consultar ou citar o Agente Reforma quando a demanda envolver:

- CBS;
- IBS;
- Imposto Seletivo;
- split payment;
- creditos tributarios;
- DFe, XML, NF-e, NFC-e, NFS-e, CT-e, BP-e, NFCom ou NF3e com impacto de Reforma;
- ERP, emissor, integracao fiscal ou layout de documento fiscal;
- CST, cClassTrib, IndOp, NCM/NBS ou classificacao vinculada a tabela vigente;
- cronograma 2026-2033;
- resposta de cliente sobre impacto da Reforma;
- comparacao de regime afetada pela transicao.

## O que nenhum agente pode prometer

- calculo final de impacto;
- melhor regime definitivo;
- economia garantida;
- aliquota futura como certeza;
- classificacao fiscal definitiva;
- cClassTrib final sem dados e tabela vigente;
- parecer tributario;
- decisao de ERP/emissor sem diagnostico;
- fonte privada como fundamento legal principal;
- resposta tecnica sem fonte vigente quando houver lei, decreto, nota tecnica, tabela ou prazo.

## Dados minimos antes de qualquer diagnostico

Quando a pergunta for concreta, o agente deve pedir ou confirmar:

- ano da analise;
- regime atual;
- atividade/CNAE;
- UF e municipio;
- tipo de documento fiscal;
- ERP/emissor utilizado;
- operacao B2B/B2C;
- NCM/NBS quando aplicavel;
- CST/cClassTrib/IndOp quando a duvida envolver DFe/XML;
- receita, margem e compras creditaveis apenas se a pergunta envolver cenario ou simulacao;
- fonte/tabela vigente quando houver classificacao, prazo ou versao.

## Como responder com seguranca

Use esta ordem:

1. traducao simples da duvida;
2. dados conhecidos;
3. dados faltantes;
4. impacto operacional provavel;
5. fonte ou lacuna de fonte;
6. proximo passo revisavel;
7. ressalva de validacao humana.

## Regras por agente

| Agente | Deve fazer | Deve evitar |
|---|---|---|
| Concierge | Direcionar para Reforma quando aparecer CBS, IBS, split, creditos, DFe/XML, ERP ou cClassTrib | Responder tecnicamente |
| Fiscal | Levantar dados de nota, XML, CFOP/NCM/CST/cClassTrib e emissor | Fechar classificacao ou calculo final |
| Onboarding | Marcar se cliente usa ERP/emissor e se emite NF-e/NFC-e/NFS-e | Prometer setup fiscal completo sem revisao |
| Contabil | Relacionar impactos em fechamento, creditos, documentos e reconciliacao | Calcular impacto tributario final |
| Comercial | Usar Reforma como urgencia operacional | Prometer economia, regime melhor ou solucao pronta |
| Conteudo/DAI | Criar educacao e anuncios com promessa segura | Usar medo tecnico sem fonte ou prometer resultado |
| Notion/Gestao | Criar pendencias, responsaveis e prazos de preparacao | Prometer automacao total de compliance |

## Matriz de gatilhos para chamada da Reforma

| Agente origem | Gatilhos obrigatorios | Saida esperada antes da Reforma | O que a Reforma devolve |
|---|---|---|---|
| Concierge | CBS, IBS, split, creditos, DFe/XML, ERP, cClassTrib, cronograma 2026-2033 | resumo da demanda, dados conhecidos e dados faltantes | direcionamento consultivo e limites |
| Fiscal | nota, XML, CFOP/NCM/CST/cClassTrib, DFe, ERP/emissor, Portal Nacional, SEFAZ ou prefeitura com impacto da Reforma | documento fiscal, operacao, regime, UF/municipio, ERP/emissor, NCM/NBS se houver | roteiro consultivo, lacunas de fonte e pontos para revisar |
| Onboarding | cliente novo com emissao de NF-e/NFC-e/NFS-e, ERP, integracao, historico XML ou atividade afetada pela Reforma | checklist de acessos, emissor, ERP, documentos e handoff Fiscal | alertas de preparacao e perguntas para diagnostico |
| Contabil | creditos, split, conciliacao de documentos, fechamento mensal, dados fiscais que impactam balancete | periodo, relatorios, apuracoes, documentos e lacunas de integracao | impactos operacionais e pontos de controle |
| Comercial | lead quer vender Reforma, economia, regime ou oportunidade tributaria | objetivo comercial, publico, claim desejado e prova disponivel | linguagem segura e bloqueios de promessa |
| Conteudo/DAI | anuncio, post, roteiro ou aula com Reforma + IA | publico, dor, cena real, claim e CTA pretendido | educacao consultiva e claims seguros |
| Notion/Gestao | tarefa recorrente, prazo, status, evidencia ou check-in de preparacao para Reforma | tarefa, responsavel, data, evidencia e dependencia tecnica | checklist de governanca, sem automacao de compliance |

## Regra de comunicacao consultiva

Quando outro agente chamar Reforma, a resposta deve tratar a Reforma como **referencia tecnica consultiva**. A resposta pode explicar, organizar, diagnosticar lacunas e sugerir proximos passos, mas nao pode:

- transformar cenario em decisao final;
- transformar estimativa em guia;
- transformar comparacao em melhor regime definitivo;
- transformar fonte privada em fundamento legal principal;
- transformar material de aula ou marketing em fonte normativa.

## Frase padrao de seguranca

> Esta resposta e informativa e consultiva. Antes de aplicar, valide o caso concreto, a versao oficial da fonte e o entendimento do responsavel tributario.
