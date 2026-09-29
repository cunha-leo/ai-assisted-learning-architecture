# Guia de uso do template

Este template representa a arquitetura em formato reutilizável.

## Antes de começar

Mapeie a estrutura real do seu curso ou formação. Não assuma que toda instituição usa os mesmos níveis.

Exemplos possíveis:

```text
Curso → Disciplina → Tema → Bloco
Curso → Disciplina → Módulo → Aula
Certificação → Domínio → Tópico
```

Adapte o esqueleto sem perder os princípios de fontes, derivados, estado e continuidade.

## Passo 1 — mapear a disciplina

Preencha a camada `01-Apresentacao-da-Disciplina/` com um documento que registre:

- identificação;
- Temas/Módulos;
- Blocos/Aulas;
- componentes extras;
- materiais gerais;
- avaliação;
- ponto inicial de estudo.

Use o exemplo do showcase como referência.

## Passo 2 — preparar Arquivos Gerais

Registre quais insumos pertencem à disciplina inteira ou a um Tema completo. Evite colocá-los artificialmente dentro de um Bloco.

## Passo 3 — estudar por unidade

Para cada Bloco:

```text
capturas + transcrição
        ↓
debate
        ↓
resumo
        ↓
infográfico
        ↓
revisão auditiva
```

Os READMEs do Tema 01 no showcase explicam finalidade, fluxo, nomenclatura e benefício de cada camada.

## Passo 4 — manter estado observável

Use Checklist Mestre + arquivos físicos como fonte da verdade. Uma IA nova deve conseguir reconstruir o ponto atual sem depender de memória de outra conversa.

## Passo 5 — consolidar

Quando todos os Blocos forem concluídos, use `90-Consolidacao-do-Tema/` para subir o nível de abstração e integrar o conhecimento do Tema.

## Passo 6 — adaptar o AGENTS

Copie `AGENTS.template.md` para o seu ambiente e personalize:

- estrutura;
- regras obrigatórias;
- nomenclatura;
- ferramentas;
- critérios de conclusão;
- política de publicação.

O objetivo é permitir que múltiplas IAs operem o mesmo sistema de maneira consistente.
