# AI-Assisted Learning Architecture

Uma arquitetura metodológica para organizar aprendizagem assistida por IA com continuidade entre sessões, governança de fontes, rastreabilidade, artefatos derivados e operação independente da ferramenta de IA utilizada.

> **Status:** v1.0 — MVP funcional da arquitetura

## O que este projeto demonstra

Este projeto não é um repositório de uma faculdade nem um espelho de materiais acadêmicos. É a documentação pública de uma arquitetura real criada para organizar estudo de forma contínua, reproduzível e auditável.

A ideia central é simples: **o estudante não precisa administrar manualmente o sistema enquanto estuda**. Ele assiste, lê, pergunta, debate, relaciona conceitos e decide. A camada de IA assume a gestão operacional do fluxo: classifica insumos, identifica onde cada item pertence, persiste artefatos, mantém nomenclatura, detecta lacunas, evita duplicatas e retoma o estudo do ponto correto.

## Visão arquitetural

A arquitetura separa quatro responsabilidades:

1. **Humano** — interpretação, decisão, dúvida, conexão, validação e construção de significado.
2. **Agente de IA** — continuidade, organização, classificação, síntese, rastreabilidade e gestão operacional.
3. **Repositório** — persistência, estrutura, proveniência, histórico e estado real do estudo.
4. **Ferramentas especializadas** — transcrição, geração visual, revisão auditiva, síntese multimodal e outras.

Essa separação permite trocar a IA ou a ferramenta sem perder o método. O protocolo não depende de uma marca específica: qualquer IA/agente capaz de ler o `AGENTS.md`, consultar o repositório e manipular os artefatos pode assumir o trabalho.

## Papel do AGENTS

O `AGENTS.md` é a camada de **governança e continuidade**.

Ele existe para que uma IA nova, em uma conversa nova ou até em outra ferramenta, consiga:

- entender qual é a estrutura do estudo;
- identificar a disciplina, Tema e Bloco em foco;
- saber quais artefatos são fontes e quais são derivados;
- localizar o estado real no repositório;
- descobrir o que já foi concluído;
- detectar o que ainda falta;
- respeitar a sequência metodológica;
- saber onde persistir cada novo insumo;
- retomar automaticamente do último ponto válido;
- manter as mesmas convenções de nomenclatura e proveniência;
- não depender da memória de uma conversa anterior.

Em outras palavras, **o repositório guarda o estado e o AGENTS ensina qualquer agente a interpretar e operar esse estado**.

## Como a continuidade funciona

Uma nova IA não deve perguntar ao estudante “onde paramos?” se a resposta estiver registrada no sistema.

O fluxo esperado é:

```text
1. Ler AGENTS
       ↓
2. Ler estrutura / Checklist Mestre
       ↓
3. Identificar Disciplina → Tema → Bloco atual
       ↓
4. Inspecionar artefatos existentes
       ↓
5. Detectar etapa concluída e próxima etapa obrigatória
       ↓
6. Carregar apenas as fontes necessárias
       ↓
7. Continuar o estudo
       ↓
8. Persistir novos artefatos e atualizar estado
```

Isso transforma contexto conversacional temporário em **continuidade operacional persistente**.

## Fluxo macro de aprendizagem

```text
Fonte
  ↓
Transcrição / Captura
  ↓
Debate humano–IA
  ↓
Resumo de fixação
  ↓
Infográfico
  ↓
Revisão auditiva / Podcast de estudo
  ↓
Transcrição do podcast + proveniência
  ↓
Consolidação do Tema
  ↓
Avaliação / revisão
```

O fluxo não é apenas uma sequência de arquivos. Cada camada tem uma função pedagógica e operacional.

## Arquitetura do repositório

A árvore faz parte do próprio projeto. Pastas vazias também representam posições arquiteturais válidas e, no GitHub, são preservadas com placeholders quando necessário.

```text
Curso/
└── Disciplina/
    ├── 00-ArquivosGerais/
    ├── 01-Apresentacao-da-Disciplina/
    ├── 02-Temas/
    │   ├── Tema-01/
    │   │   ├── Bloco-01/
    │   │   │   ├── 01-Capturas-Oficiais/
    │   │   │   ├── 02-Transcricao-da-Videoaula/
    │   │   │   ├── 03-Resumo-e-Debate/
    │   │   │   ├── 04-Infografico/
    │   │   │   └── 05-Podcast-de-Estudo-NotebookLM/
    │   │   ├── Bloco-02/
    │   │   │   └── [mesmas 5 camadas]
    │   │   ├── Bloco-03/
    │   │   │   └── [mesmas 5 camadas]
    │   │   ├── Bloco-04/
    │   │   │   └── [mesmas 5 camadas]
    │   │   ├── Bloco-05/
    │   │   │   └── [mesmas 5 camadas]
    │   │   └── 90-Consolidacao-do-Tema/
    │   │       ├── 01-Resumo-do-Tema/
    │   │       ├── 02-Infografico-Consolidado/
    │   │       └── 03-Podcast-de-Estudo-NotebookLM/
    │   ├── Tema-02/
    │   │   └── [mesmo esqueleto]
    │   ├── Tema-03/
    │   │   └── [mesmo esqueleto]
    │   └── Tema-04/
    │       └── [mesmo esqueleto]
    ├── 03-Saiba-Mais-na-Pratica/
    ├── 04-Aulas-ao-vivo/
    ├── 05-Demonstracao-Pratica/
    ├── 06-Avaliacao/
    └── Checklist-Mestre
```

A quantidade de Temas e Blocos não é fixa. O agente deve adaptar a estrutura ao curso real.

## Anatomia de um Bloco

Cada Bloco é tratado como a menor unidade operacional de aprendizagem.

### 01 — Capturas Oficiais
Evidências visuais relevantes, quando existirem.

### 02 — Transcrição da Videoaula
Fonte textual primária do conteúdo falado. Em um repositório público, o conteúdo institucional pode ser substituído por placeholder sem remover sua posição arquitetural.

### 03 — Resumo e Debate
Síntese construída após interação humano–IA. Não é uma cópia da aula; registra compreensão, relações, exemplos, limites e linguagem consolidada.

### 04 — Infográfico
Representação visual autoral para revisão e fixação.

### 05 — Podcast de Estudo
Revisão auditiva gerada a partir dos artefatos do próprio Bloco, com controle de escopo, idioma, modalidade e proveniência.

## Consolidação do Tema

Quando os Blocos são concluídos, a arquitetura sobe um nível de abstração:

```text
Bloco 01 ┐
Bloco 02 ├─→ Consolidação do Tema
Bloco 03 ┤      ├─ resumo consolidado
Bloco 04 ┤      ├─ infográfico consolidado
Bloco 05 ┘      └─ revisão auditiva consolidada
```

Nesse momento, fontes gerais do Tema podem ser cruzadas com os derivados produzidos durante o percurso.

## Estado e Checklist Mestre

A arquitetura não considera uma etapa concluída apenas porque ela foi discutida em uma conversa.

O estado deve ser verificável no repositório.

Exemplos de cobertura:

- transcrição localizada;
- capturas persistidas;
- debate realizado;
- resumo persistido;
- infográfico produzido;
- revisão auditiva persistida;
- Tema consolidado;
- avaliação revisada.

O **Checklist Mestre** funciona como uma camada de estado observável. Um novo agente consulta o checklist e os arquivos existentes para reconstruir o ponto atual sem depender de memória conversacional.

## Multi-IA por design

A arquitetura foi desenhada para não depender de uma única IA.

Uma ferramenta pode fazer o debate; outra pode transcrever; outra pode gerar áudio; outra pode produzir imagens; outra pode assumir o repositório posteriormente.

O contrato entre elas é composto por:

```text
AGENTS + estrutura de diretórios + convenções + proveniência + estado persistido
```

Se esse contrato for respeitado, a ferramenta pode mudar sem quebrar a continuidade.

## Separação entre fontes e derivados

```text
FONTES / INSUMOS
├── materiais oficiais
├── transcrições
├── capturas
├── leituras
└── instruções

DERIVADOS
├── resumos
├── debates consolidados
├── infográficos
├── podcasts de estudo
├── transcrições dos podcasts
└── consolidações
```

Fontes nunca devem ser sobrescritas por derivados. Proveniência deve ser preservada.

## Implementação privada x showcase público

A implementação real é um sistema vivo e pode conter materiais institucionais, dados operacionais e fontes que não devem ser redistribuídas.

Este GitHub é um **snapshot demonstrativo**.

A regra é:

```text
Implementação privada → sistema real de estudo
GitHub público        → showcase sanitizado da arquitetura
Template              → estrutura neutra e reutilizável
```

Quando uma fonte não pode ser publicada, sua **posição arquitetural permanece visível**, mas o conteúdo é substituído por placeholder.

Veja também: [Política de publicação](docs/governance/publication-policy.md).

## Estrutura deste repositório

- `AGENTS.template.md` — protocolo operacional reutilizável;
- `docs/architecture/` — explicação da arquitetura;
- `docs/governance/` — regras de publicação e separação de responsabilidades;
- `showcase/` — demonstração navegável da implementação;
- `template/` — estrutura neutra para reutilização;
- `CHANGELOG.md` — evolução do projeto.

## Como aplicar em outro contexto

1. Copie o template.
2. Adapte a hierarquia real do curso.
3. Personalize o `AGENTS.template.md`.
4. Defina quais etapas são obrigatórias.
5. Crie um Checklist Mestre.
6. Use o repositório como estado persistente.
7. Permita que qualquer agente leia o protocolo antes de atuar.
8. Evolua a arquitetura somente quando surgir uma necessidade real.

Pode ser adaptado para graduação, pós-graduação, certificações, preparação para provas, estudo de idiomas, formação corporativa ou qualquer processo de aprendizagem estruturado.

## Princípio central

```text
O humano aprende e decide.
A IA ajuda a compreender e gerencia a continuidade.
O repositório preserva o estado.
O AGENTS torna esse estado inteligível para qualquer agente.
```

## Status

**v1.0 — MVP funcional**

A arquitetura já opera de ponta a ponta no nível de Bloco. A evolução futura ocorre por necessidade arquitetural, não pela obrigação de espelhar todo o conteúdo acadêmico.

## Contato

Para discutir adaptação, implementação ou aplicação profissional desta arquitetura, entre em contato pelo perfil do autor no GitHub.
