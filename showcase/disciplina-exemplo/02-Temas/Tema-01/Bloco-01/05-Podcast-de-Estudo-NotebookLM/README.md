# 05 — Podcast de Estudo / Revisão Auditiva

## Objetivo
Transformar os artefatos já consolidados do Bloco em uma revisão auditiva didática. O áudio não substitui a aula; ele reforça fixação e revisão.

## Ferramenta
O piloto usa NotebookLM, mas a arquitetura não depende dele.

## Fontes do Bloco
- transcrição;
- capturas relevantes;
- resumo;
- infográfico;
- Prompt Mestre.

Não misture material de outros Blocos quando isso puder antecipar conteúdo ainda não estudado.

## Como fazer no NotebookLM
1. crie um caderno para o Bloco;
2. adicione os insumos;
3. adicione o Prompt Mestre;
4. oriente a ferramenta a ler primeiro o Prompt Mestre;
5. escolha o recurso de resumo em áudio;
6. selecione modalidade, idioma e duração;
7. gere e baixe o áudio;
8. transcreva o áudio;
9. envie áudio + transcrição ao agente;
10. o agente organiza, nomeia e preserva proveniência.

Prompt curto de exemplo:

> Leia primeiro o Prompt Mestre e siga suas regras. Depois utilize os demais anexos deste Bloco como base factual.

## Estrutura por idioma
```text
Prompt-Mestre.md
PT/
ES/
EN/
```

Criar pastas de idioma apenas quando existirem artefatos.

## Benefícios
Revisão sem tela, repetição, exposição multilíngue, reforço conceitual e preparação para a consolidação do Tema.
