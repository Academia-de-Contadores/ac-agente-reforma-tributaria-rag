---
title: Modelos - Agente Reforma Tributaria
type: knowledge-templates
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

# Modelos de resposta e checklists - Agente Reforma Tributaria

## Modelos deste agente
- Roteiro 7/30/90
- Resposta cliente
- Diagnostico Reforma

## Modelo 1 - Resposta operacional segura
```markdown
### Leitura curta
[Explique o caso em linguagem simples.]

### Dados que tenho
- [listar]

### Dados faltantes
- [listar]

### Checklist
1. [passo revisavel]
2. [passo revisavel]
3. [passo revisavel]

### Risco e revisao humana
[Explique o limite tecnico.]

### Fonte ou lacuna de fonte
[Informe a fonte oficial/versionada usada ou diga claramente qual fonte falta.]

### Proxima acao segura
[Uma acao de 15 minutos sem decisao final.]
```

## Modelo 2 - Handoff para outro agente
```markdown
Agente destino: [nome]
Motivo do encaminhamento: [sinal]
Dados ja coletados: [lista]
Dados faltantes: [lista]
Risco: [baixo/medio/alto]
Pedido para o agente destino: [acao]
```

## Modelo 3 - Acionamento de Reforma por outro agente
```markdown
Agente origem:
Motivo do acionamento:
Ano da analise:
Regime atual:
Atividade/CNAE:
UF/municipio:
Documento fiscal envolvido:
ERP/emissor:
Operacao B2B/B2C:
Campos fiscais envolvidos:
Fonte vigente ja consultada:
Dados faltantes:
Pergunta para Reforma:
Limite tecnico observado:
```

## Modelo 4 - Resposta com lacuna de fonte vigente
```markdown
Consigo organizar o caminho, mas nao devo fechar a conclusao tecnica sem fonte vigente.

O que ja sabemos:
- [listar]

Fonte que falta validar:
- [lei/manual/tabela/nota tecnica/portal oficial]

Proximo passo seguro:
- [acao revisavel, sem classificacao/calc final]

Limite:
- Esta nao e uma classificacao final, parecer ou calculo definitivo.
```
