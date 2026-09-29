# 05 — Podcast de Estudo / Revisão Auditiva

## Objetivo

Transformar os artefatos já consolidados do Bloco em uma revisão auditiva didática.

O áudio **não substitui a aula**. Ele funciona como uma segunda forma de contato com o conteúdo, útil para fixação, revisão e exposição em outros idiomas.

## Ferramenta

A implementação piloto usa NotebookLM, mas a arquitetura não depende dele. Outra ferramenta pode ocupar esta função desde que respeite o escopo e a proveniência.

## Fontes recomendadas no nível do Bloco

Use somente materiais daquele Bloco:

- transcrição da videoaula;
- capturas relevantes;
- resumo de fixação;
- infográfico;
- Prompt Mestre.

Evite adicionar fontes consolidadas de outros Blocos quando isso puder antecipar conteúdo ainda não estudado.

## Prompt Mestre

O Prompt Mestre fica na raiz desta pasta e define:

- escopo;
- objetivo pedagógico;
- regras de transformação;
- limites;
- estilo;
- critérios de fechamento.

Ele deve ser reutilizável e **agnóstico de idioma**.

Idioma, variante, duração e modalidade são parâmetros da execução.

## Exemplo de fluxo no NotebookLM

1. crie um caderno para o Bloco;
2. adicione os insumos do Bloco;
3. adicione o `Prompt Mestre`;
4. peça à ferramenta para considerar primeiro as instruções do Prompt Mestre;
5. escolha o recurso de resumo/revisão em áudio;
6. selecione modalidade e idioma;
7. gere o áudio;
8. faça download;
9. transcreva o áudio;
10. envie áudio + transcrição ao agente;
11. o agente normaliza nomes, preserva proveniência e organiza na subpasta do idioma.

Prompt curto de execução, como exemplo:

> Leia primeiro o Prompt Mestre e siga suas regras. Depois utilize os demais anexos deste Bloco como base factual para gerar a revisão auditiva.

## Organização por idioma

```text
05-Podcast-de-Estudo-NotebookLM/
├── Prompt-Mestre.md
├── PT/
├── ES/
└── EN/
```

As pastas de idioma devem ser criadas somente quando houver artefatos.

## Pareamento

Áudio e transcrição devem compartilhar a mesma identidade-base.

Exemplo:

`Conceitos_de_UX_PTBR_Analise01.m4a`

`Conceitos_de_UX_PTBR_Analise01__2026-09-29__assemblyai__clean.txt`

## Benefícios

- revisão sem tela;
- repetição espaçada;
- contato com a mesma matéria em outra modalidade;
- desenvolvimento de vocabulário em outros idiomas;
- reforço de relações entre conceitos;
- material complementar para consolidação do Tema.
