# 02 — Transcrição da Videoaula

## O que entra aqui

A transcrição textual da videoaula correspondente ao Bloco.

## Por que usar transcrição em vez de armazenar o vídeo

O vídeo é uma excelente fonte para o estudante, mas é um artefato pesado e nem sempre é a forma mais eficiente de fornecer contexto para uma IA.

A transcrição:

- reduz peso de armazenamento;
- facilita busca por termos;
- permite leitura rápida;
- torna o conteúdo indexável;
- ajuda a IA a localizar conceitos e relações;
- preserva o conteúdo falado em formato mais operacional;
- facilita revisão, resumo e comparação posterior.

A arquitetura **não depende de uma ferramenta específica de transcrição**. Pode ser usado qualquer serviço capaz de gerar uma saída suficientemente confiável.

## Fluxo sugerido

```text
Videoaula
   ↓
Ferramenta de transcrição
   ↓
TXT / Markdown
   ↓
Revisão ou limpeza, quando necessária
   ↓
Persistência nesta pasta
   ↓
Debate humano–IA
```

## Proveniência

Sempre que disponível, preserve no nome:

- data;
- motor de transcrição;
- estágio do pipeline (`raw`, `clean` etc.).

Exemplo:

`2026-09-29__assemblyai__clean.txt`

`clean` significa que passou por uma etapa de limpeza/revisão; não significa perfeição absoluta.

## Repositório público

Quando a transcrição deriva de conteúdo institucional ou de terceiros que não deve ser redistribuído, **a posição arquitetural permanece**, mas o texto original deve ser substituído por placeholder explicativo.

O objetivo do showcase é mostrar onde a transcrição entra no sistema, não redistribuir a aula.
