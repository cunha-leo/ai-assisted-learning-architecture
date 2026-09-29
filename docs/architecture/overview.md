# Visão arquitetural

Esta arquitetura transforma contexto de estudo temporário em um sistema persistente que pode ser retomado por diferentes agentes de IA.

## Responsabilidades

1. **Humano** — interpretação, decisão, dúvida, conexão e validação.
2. **Agente de IA** — continuidade, organização, classificação, síntese e gestão operacional.
3. **Repositório** — persistência, rastreabilidade, proveniência, histórico e estado.
4. **Ferramentas especializadas** — transcrição, geração visual, revisão auditiva e outras.

## Contrato de continuidade

```text
AGENTS
  +
Estrutura de diretórios
  +
Artefatos persistidos
  +
Checklist Mestre
  +
Proveniência
  ↓
Qualquer agente consegue reconstruir o estado
  ↓
Identifica a próxima etapa válida
  ↓
Continua o estudo
```

O objetivo é evitar dependência de uma conversa, sessão ou fornecedor específico de IA.

## Fluxo macro

```text
Fonte
  ↓
Transcrição / Captura
  ↓
Debate humano–IA
  ↓
Resumo
  ↓
Infográfico
  ↓
Podcast de estudo
  ↓
Transcrição do podcast
  ↓
Consolidação do Tema
  ↓
Avaliação / revisão
```

## Retomada automática

Um novo agente deve:

```text
Ler AGENTS
  ↓
Ler Checklist / estado
  ↓
Inspecionar Tema e Bloco atuais
  ↓
Comparar o que existe com a cadeia obrigatória
  ↓
Detectar lacuna
  ↓
Carregar apenas o necessário
  ↓
Continuar
```

## Objetivo

Transformar estudo disperso em um sistema reproduzível, navegável, auditável e independente de ferramenta.
