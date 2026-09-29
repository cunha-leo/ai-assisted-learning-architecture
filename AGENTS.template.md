# AGENTS — TEMPLATE DE ARQUITETURA DE APRENDIZAGEM ASSISTIDA POR IA

Versão: 1.1

## 1. Finalidade

Este arquivo é o protocolo operacional e a porta de entrada para qualquer agente de IA que participe deste sistema de aprendizagem.

Ele não depende de uma IA específica. ChatGPT, Claude, Gemini, Copilot, agentes locais, IDEs ou outras ferramentas podem assumir o processo desde que consigam ler este arquivo e acessar o repositório.

Objetivo: permitir que um agente novo compreenda **o que é este projeto, como ele está organizado, onde o estudo parou, o que já foi concluído, o que falta e qual é a próxima ação válida**, sem depender de memória de uma conversa anterior.

## 2. Contrato de responsabilidades

### Estudante
O estudante:
- assiste, lê e estuda;
- compartilha insumos;
- pergunta;
- debate;
- relaciona conceitos;
- valida entendimento;
- toma decisões.

### Agente de IA
O agente:
- identifica Disciplina, Tema e Bloco;
- classifica insumos;
- determina destino canônico;
- persiste materiais;
- mantém nomenclatura;
- preserva proveniência;
- evita duplicatas;
- verifica cobertura;
- identifica lacunas;
- gera derivados quando previsto;
- atualiza estado;
- retoma o processo do último ponto válido.

### Repositório
O repositório é a fonte persistente do estado real. Conversas são transitórias; arquivos, estrutura e checklist são persistentes.

## 3. Bootstrap obrigatório de qualquer novo agente

Antes de continuar o estudo, executar:

1. ler este `AGENTS.md`;
2. identificar a disciplina em foco;
3. localizar o Checklist Mestre ou arquivo equivalente de estado;
4. localizar o Tema atual;
5. localizar o Bloco atual;
6. inspecionar os artefatos já existentes;
7. comparar artefatos existentes com a cadeia obrigatória;
8. identificar a primeira etapa pendente;
9. carregar somente as fontes necessárias para essa etapa;
10. continuar dali.

Não perguntar “onde paramos?” quando isso puder ser inferido do repositório.

## 4. Regra de reconstrução de estado

O agente deve tratar presença física de artefatos + Checklist Mestre como evidência de estado.

Exemplo:

```text
Transcrição: existe
Capturas: existem
Resumo: existe
Infográfico: existe
Podcast: ausente
```

Conclusão operacional:

```text
Bloco ainda não concluído.
Próxima etapa = revisão auditiva / podcast.
```

Nunca marcar uma etapa como concluída apenas porque ela foi mencionada em uma conversa anterior.

## 5. Hierarquia pedagógica

Estrutura conceitual:

```text
DISCIPLINA → TEMA → BLOCO
```

O Bloco é a menor unidade operacional de estudo.

A quantidade de Temas e Blocos deve ser lida do curso real. Não assumir números fixos.

## 6. Estrutura canônica de um Bloco

```text
Bloco-NN/
├── 01-Capturas-Oficiais/
├── 02-Transcricao-da-Videoaula/
├── 03-Resumo-e-Debate/
├── 04-Infografico/
└── 05-Podcast-de-Estudo-NotebookLM/
```

As pastas fazem parte da arquitetura. Em sistemas como Git, onde diretórios vazios não são versionados, usar `.gitkeep`, `README.md` ou placeholder para preservar a posição arquitetural.

## 7. Cadeia obrigatória de um Bloco

Fluxo padrão:

1. localizar/receber a fonte principal;
2. persistir transcrição;
3. persistir capturas relevantes quando existirem;
4. realizar debate e entendimento;
5. produzir resumo de fixação;
6. persistir o resumo;
7. gerar infográfico;
8. persistir infográfico;
9. gerar revisão auditiva/podcast;
10. persistir áudio e respectiva transcrição;
11. atualizar Checklist Mestre;
12. somente então considerar o Bloco concluído.

O estudante pode explicitamente dispensar uma etapa. Sem dispensa explícita, seguir o fluxo.

## 8. Ingestão automática

Quando o estudante enviar um novo material, o agente deve:

1. identificar curso/disciplina/tema/bloco;
2. identificar proveniência;
3. determinar se é fonte ou derivado;
4. decidir destino canônico;
5. verificar se já existe;
6. normalizar nomenclatura sem apagar proveniência;
7. persistir;
8. atualizar estado;
9. continuar o estudo.

Não devolver ao estudante tarefas de filesystem que o agente consiga executar.

## 9. Fontes vs derivados

### Fontes / insumos
- materiais oficiais;
- videoaulas como referência;
- transcrições;
- capturas;
- leituras;
- instruções;
- avaliações.

### Derivados
- resumos;
- debates consolidados;
- glossários;
- infográficos;
- mapas conceituais;
- podcasts de estudo;
- transcrições de podcasts;
- consolidações.

Regra: nunca sobrescrever uma fonte com um derivado.

## 10. Proveniência

Quando um nome de arquivo já trouxer proveniência, preservá-la.

Exemplos de proveniência:
- data;
- motor de transcrição;
- estágio de pipeline;
- idioma;
- modalidade;
- número da geração.

Não inventar metadados ausentes.

## 11. Resumo e debate

O resumo deve ser produzido somente depois do estudo e debate.

Ele deve:
- registrar a ideia central;
- explicar relações;
- preservar terminologia importante;
- distinguir fonte de interpretação;
- incluir exemplos quando úteis;
- registrar limites e ressalvas;
- servir como insumo para revisão posterior.

Quando o processo exigir, o resumo deve ser persistido e também apresentado ao estudante para revisão.

## 12. Infográfico

O infográfico é derivado do estudo, não uma simples decoração.

Deve:
- refletir conceitos realmente estudados;
- mostrar relações, contrastes, sequência ou processo;
- ser útil para revisão;
- evitar excesso de texto;
- manter consistência visual entre Blocos.

Implementação privada pode preservar identificação institucional quando útil ao estudo. Versões públicas devem remover branding que possa sugerir material oficial e substituir elementos institucionais quando necessário.

## 13. Revisão auditiva / podcast de estudo

Objetivo: revisar e fixar o conteúdo do Bloco.

Regras:
- usar somente os insumos do escopo atual;
- não antecipar outros Blocos;
- permitir analogias e exemplos pedagógicos dentro do eixo conceitual;
- manter Prompt Mestre separado de parâmetros variáveis;
- idioma, duração e modalidade podem variar por geração;
- áudio e transcrição devem permanecer pareados.

## 14. Organização por idioma

Quando houver material em vários idiomas:

```text
05-Podcast-de-Estudo-NotebookLM/
├── Prompt-Mestre.md
├── PT/
├── ES/
└── EN/
```

Criar pastas de idioma somente quando existirem artefatos correspondentes.

A variante pode permanecer no nome do arquivo, por exemplo:
- PTBR;
- PTPT;
- ESLA;
- ESES;
- ENUS;
- ENGB.

## 15. Consolidação do Tema

Após concluir todos os Blocos:

1. verificar cobertura de cada Bloco;
2. revisar derivados;
3. incorporar fontes gerais do Tema quando apropriado;
4. identificar lacunas;
5. gerar síntese consolidada;
6. gerar infográfico consolidado;
7. opcionalmente gerar revisão auditiva consolidada;
8. atualizar estado do Tema.

Estrutura:

```text
90-Consolidacao-do-Tema/
├── 01-Resumo-do-Tema/
├── 02-Infografico-Consolidado/
└── 03-Podcast-de-Estudo-NotebookLM/
```

## 16. Checklist Mestre

O Checklist Mestre representa o estado operacional da disciplina.

Deve acompanhar, quando aplicável:
- fontes gerais localizadas;
- transcrição;
- capturas;
- debate;
- resumo;
- infográfico;
- revisão auditiva;
- consolidação do Tema;
- avaliação.

O agente deve atualizar o checklist quando o estado físico do repositório mudar.

## 17. Regra de continuidade

Antes de avançar para outro Bloco ou Tema:

- verificar se há etapa obrigatória pendente;
- se houver, informar naturalmente e conduzir à etapa;
- se o estudante ordenar explicitamente pular, registrar e seguir.

O agente não deve repetir etapas concluídas apenas por segurança.

## 18. Multi-IA e independência de ferramenta

A arquitetura foi desenhada para sobrevivência de contexto entre ferramentas.

Qualquer agente deve conseguir operar a partir de:

```text
AGENTS
+ árvore de diretórios
+ arquivos persistidos
+ convenções de nomenclatura
+ proveniência
+ Checklist Mestre
```

Nenhuma regra crítica deve existir apenas na memória de uma conversa.

## 19. Publicação pública

Separar:

### Implementação privada
Sistema vivo, completo e operacional.

### Showcase público
Snapshot demonstrativo, sanitizado e navegável.

### Template
Estrutura neutra e reutilizável.

No showcase público:
- preservar a posição arquitetural de fontes;
- substituir conteúdo restrito por placeholder;
- remover dados privados;
- remover IDs internos;
- remover branding institucional quando necessário;
- manter derivados autorais quando adequados.

## 20. Precedência

Em caso de conflito:

1. instrução explícita mais recente do estudante;
2. fonte primária do curso;
3. estado real do repositório;
4. Checklist Mestre;
5. este AGENTS;
6. interpretações anteriores.

Não harmonizar silenciosamente conflitos importantes.

## 21. Princípio final

```text
O estudante aprende e decide.
O agente organiza, mantém continuidade e ajuda a compreender.
O repositório preserva o estado.
O AGENTS permite que qualquer IA reconstrua e continue esse estado.
```

A arquitetura existe para reduzir carga cognitiva, não para criar burocracia.
