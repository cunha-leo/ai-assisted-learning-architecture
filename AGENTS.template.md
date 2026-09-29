# AGENTS — TEMPLATE DE ARQUITETURA DE APRENDIZAGEM ASSISTIDA POR IA

Versão: 1.0

## 1. Objetivo

Este arquivo é a porta de entrada operacional para qualquer agente de IA que participe do processo de estudo.

O estudante estuda, compartilha, debate e decide.
A IA organiza, classifica, persiste, nomeia, evita duplicatas, mantém rastreabilidade e gerencia continuidade.

## 2. Hierarquia pedagógica

DISCIPLINA → TEMA → BLOCO

O Bloco é a menor unidade operacional de estudo.

## 3. Estrutura de cada Bloco

```text
Bloco-NN/
├── 01-Capturas/
├── 02-Transcricao/
├── 03-Resumo-e-Debate/
├── 04-Infografico/
└── 05-Podcast-de-Estudo/
```

## 4. Cadeia padrão do Bloco

1. receber/localizar fonte principal;
2. persistir transcrição;
3. preservar capturas relevantes;
4. debater conteúdo;
5. produzir resumo de fixação;
6. gerar infográfico;
7. gerar revisão auditiva;
8. persistir derivados;
9. atualizar estado/checklist.

## 5. Fontes vs derivados

### Fontes
- materiais oficiais;
- transcrições;
- capturas;
- leituras;
- instruções;
- avaliações.

### Derivados
- resumos;
- debates;
- glossários;
- infográficos;
- mapas mentais;
- podcasts de estudo;
- transcrições de podcasts;
- consolidações.

Nunca sobrescrever fonte com derivado.

## 6. Regra de ingestão automática

Quando o estudante enviar material relevante, a IA deve:

1. identificar disciplina, tema e bloco;
2. inferir o destino correto;
3. persistir;
4. nomear consistentemente;
5. evitar duplicatas;
6. atualizar cobertura.

## 7. Continuidade

Se uma etapa obrigatória estiver pendente, a IA deve lembrar naturalmente antes de avançar.

## 8. Consolidação por Tema

Depois dos Blocos:

- revisar fontes consolidadas;
- cruzar conceitos;
- gerar síntese do Tema;
- gerar infográfico consolidado;
- opcionalmente gerar podcast consolidado.

## 9. Revisão auditiva

A revisão em áudio deve usar somente os insumos do escopo atual.

Não incluir fontes de outros Blocos quando isso puder antecipar conteúdo não estudado.

## 10. Publicação pública

A implementação privada pode conter fontes institucionais e dados não destinados à redistribuição.

A versão pública deve preservar a arquitetura e substituir fontes restritas por placeholders ou equivalentes autorais.

## 11. Princípio final

A estrutura existe para reduzir carga cognitiva e manter continuidade, não para criar burocracia.
