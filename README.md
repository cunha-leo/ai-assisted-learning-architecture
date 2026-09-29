# AI-Assisted Learning Architecture

Uma arquitetura metodológica para organizar estudo assistido por IA com governança de fontes, artefatos derivados, rastreabilidade e continuidade entre ferramentas.

## Visão geral

Este repositório documenta uma arquitetura de aprendizagem assistida por IA aplicada a um caso real de estudo. O objetivo não é publicar materiais institucionais de terceiros, mas demonstrar como estruturar um processo de aprendizagem com:

- fontes primárias;
- debate humano-IA;
- síntese;
- infográficos;
- revisão auditiva;
- proveniência;
- versionamento;
- consolidação por tema;
- template reutilizável.

A implementação privada continua evoluindo fora deste repositório. Aqui fica uma versão pública, sanitizada e demonstrativa.

## Princípio central

```text
Fonte → estudo/debate → vocabulário/método → síntese → infográfico
→ revisão auditiva → persistência → consolidação → avaliação
```

## Arquitetura

```text
Curso/
└── Disciplina/
    ├── 00-ArquivosGerais/
    ├── 01-Apresentacao/
    ├── 02-Temas/
    │   ├── Tema-01/
    │   │   ├── Bloco-01/
    │   │   │   ├── 01-Capturas/
    │   │   │   ├── 02-Transcricao/
    │   │   │   ├── 03-Resumo-e-Debate/
    │   │   │   ├── 04-Infografico/
    │   │   │   └── 05-Podcast-de-Estudo/
    │   │   └── 90-Consolidacao-do-Tema/
    │   ├── Tema-02/
    │   ├── Tema-03/
    │   └── Tema-04/
    └── 06-Avaliacao/
```

## Separação entre privado e público

A implementação real pode conter fontes institucionais, transcrições, capturas e outros materiais de acesso restrito.

Este repositório público mantém a arquitetura e substitui fontes não redistribuíveis por placeholders explicativos. Artefatos autorais e transformativos podem ser demonstrados quando apropriado.

Veja: [docs/governance/publication-policy.md](docs/governance/publication-policy.md)

## Componentes

- `AGENTS.template.md` — protocolo reutilizável para um agente de IA operar a arquitetura;
- `showcase/` — implementação demonstrativa;
- `template/` — estrutura neutra e replicável;
- `docs/` — documentação arquitetural e de governança;
- `CHANGELOG.md` — evolução da arquitetura.

## Como usar

1. Copie a estrutura de `template/`.
2. Ajuste o `AGENTS.template.md`.
3. Defina sua hierarquia de curso/disciplina/tema/bloco.
4. Use uma IA como gestora de continuidade e organização do filesystem.
5. Mantenha fontes e derivados separados.
6. Consolide por tema antes da avaliação final.

## Caso demonstrativo

O diretório `showcase/disciplina-exemplo/` representa uma disciplina real adaptada para demonstração pública. Um Tema pode ser mostrado em maior profundidade enquanto os demais representam a escalabilidade do modelo.

## Status

**v1.0 — MVP funcional da arquitetura**

A arquitetura já foi validada no nível de Bloco. A consolidação completa por Tema e demais refinamentos poderão gerar versões futuras.

## Contato

Para discutir adaptação, implementação ou uso profissional desta arquitetura, entre em contato pelo meu perfil no GitHub.
