# Sprints — Plano de Construção

Cronograma inicial de sprints com critérios de priorização explícitos.

## Estrutura

```text
sprints/
├── README.md
├── criterios.md
├── sprint-01.md
├── sprint-02.md
├── sprint-03.md
└── sprint-04.md
```

## Visão geral

```mermaid
gantt
    title Cronograma de Sprints
    dateFormat  YYYY-MM-DD
    section Sprint 1 - Fundação
    Repositórios e ambiente      :s1a, 2026-10-26, 3d
    Backend modelos e RF01/RF05  :s1b, after s1a, 4d
    Angular agenda do dono RF04  :s1c, after s1b, 3d
    section Sprint 2 - Cliente agenda
    Tela 1 RF01/RF06             :s2a, 2026-11-09, 3d
    Tela 2 RF02                  :s2b, after s2a, 3d
    Cadastro serviços RF06       :s2c, after s2b, 2d
    section Sprint 3 - Gestão
    Cancelar e remarcar RF03     :s3a, 2026-11-23, 4d
    Bloqueio manual RF08         :s3b, after s3a, 3d
    section Sprint 4 - Acabamento
    Lembrete RF07                :s4a, 2026-12-07, 3d
    Identidade visual e LGPD     :s4b, after s4a, 4d
```

## Critérios de priorização

- Valor direto para o barbeiro e para o cliente.
- Dependência técnica entre itens.
- Risco de bloquear outros itens se não for feito cedo.
- Simplicidade e custo baixo como restrição permanente.

## Regras de alocação

- Nenhuma sprint começa sem que os itens da sprint anterior estejam concluídos ou explicitamente replanejados.
- Requisitos não funcionais entram como critério transversal, não como item isolado.
- Itens fora do MVP não entram no cronograma.
