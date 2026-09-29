# AI-Assisted Learning Architecture

Uma arquitetura prática para transformar estudo disperso em um processo guiado, organizado e contínuo com apoio de IA.

> **Status:** v1.0 — MVP funcional da arquitetura

## A dor que este projeto resolve

Estudar com IA pode ser muito poderoso, mas costuma gerar uma nova carga operacional:

- lembrar em que ponto o estudo parou;
- organizar prints, transcrições, resumos e arquivos;
- decidir o que vem depois;
- saber quando debater, resumir ou consolidar;
- evitar perder contexto entre conversas;
- reconstruir o histórico quando muda de IA;
- manter uma metodologia consistente ao longo de semanas ou meses.

A proposta desta arquitetura é retirar essa carga do estudante.

## Ideia central

**O usuário estuda. A IA gerencia o processo de estudo.**

O papel do estudante é:

- consumir o conteúdo;
- compartilhar insumos;
- fazer perguntas;
- debater;
- testar entendimento;
- relacionar conceitos;
- aprender e consolidar conhecimento.

O papel da IA é atuar como **facilitadora e gestora da continuidade**:

- identificar onde o estudo está;
- entender qual é o próximo passo;
- organizar os arquivos;
- direcionar cada artefato para o lugar correto;
- lembrar etapas pendentes;
- sugerir debate, resumo, infográfico ou revisão quando chegar o momento;
- manter nomenclatura e rastreabilidade;
- atualizar o estado do estudo;
- consolidar o conhecimento progressivamente.

Em outras palavras, o estudante não precisa gastar energia mental administrando o método. A arquitetura faz essa gestão operacional para que ele concentre energia em aprender.

## O que fica automatizado

Dentro de um ambiente em que o agente tenha acesso ao repositório e às ferramentas necessárias, o fluxo pode ser conduzido assim:

```text
Você estuda e compartilha
        ↓
A IA identifica Disciplina → Tema → Bloco
        ↓
Classifica e salva os insumos
        ↓
Percebe o que já foi concluído
        ↓
Identifica o próximo passo
        ↓
Conduz debate e tira dúvidas
        ↓
Gera e persiste resumo
        ↓
Gera e organiza infográfico
        ↓
Conduz revisão auditiva
        ↓
Atualiza o estado
        ↓
Avança para a próxima etapa
        ↓
Consolida Tema / prepara revisão e avaliação
```

O estudante não precisa administrar manualmente a árvore de arquivos durante o estudo.

## Exemplo simples de uso

Você termina uma videoaula e envia ao agente:

- a transcrição;
- alguns prints que considerou importantes;
- suas dúvidas.

A partir daí, o agente:

1. identifica onde aquele material pertence;
2. persiste os arquivos;
3. conduz o debate;
4. verifica o que ainda falta;
5. cria o resumo no momento correto;
6. propõe ou gera o infográfico;
7. conduz a revisão auditiva;
8. registra o estado;
9. sabe se o próximo passo é outro Bloco ou a consolidação.

A continuidade não depende de você lembrar tudo nem de uma única conversa permanecer aberta.

## O papel do AGENTS

O `AGENTS.md` funciona como o **manual operacional da arquitetura**.

Ele explica para qualquer agente de IA:

- qual é a estrutura;
- como interpretar o repositório;
- como descobrir onde o estudo parou;
- quais etapas são obrigatórias;
- onde cada tipo de arquivo deve ser salvo;
- como distinguir fonte de derivado;
- como manter proveniência;
- quando avançar;
- quando consolidar;
- como retomar o trabalho sem depender da memória da conversa anterior.

Por isso a arquitetura é **multi-IA por design**: o agente pode mudar, desde que leia o protocolo e o estado persistido.

## Caso real e versão pública

Esta arquitetura nasceu de um **caso real de estudo pessoal**, aplicado a uma disciplina de pós-graduação e refinado durante o uso.

A implementação privada contém a estrutura completa e os materiais reais de estudo.

Este repositório público foi **sanitizado e adaptado** para demonstração:

- materiais institucionais protegidos não são redistribuídos;
- transcrições de aulas podem ser substituídas por placeholders;
- capturas privadas podem ser removidas ou recriadas;
- branding institucional é retirado dos derivados públicos quando necessário;
- caminhos, IDs e dados privados não são expostos.

O objetivo é mostrar fielmente **a arquitetura, o método, o fluxo e a capacidade de automação**, sem publicar conteúdo institucional que não pertence ao projeto.

## Benefício principal

A arquitetura tenta resolver uma pergunta prática:

> **“Como posso estudar com IA sem transformar o próprio estudo em um trabalho de organização?”**

A resposta proposta é separar responsabilidades:

- **humano:** aprender, perguntar, decidir e consolidar;
- **IA:** facilitar, organizar, lembrar, persistir e conduzir continuidade;
- **repositório:** guardar o estado real;
- **AGENTS:** tornar esse estado compreensível para qualquer agente.

O resultado é uma metodologia em que a parte operacional fica progressivamente automatizada e o estudante permanece focado no aprendizado.

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
