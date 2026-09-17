# Barberis — Sistema de Agendamento Online

Projeto de produto de software para agendamento em barbearias de pequeno porte, donas do próprio negócio, que atualmente realizam os agendamentos manualmente pelo WhatsApp.

## Problema

Barbeiros autônomos testam aplicativos de agendamento, mas nem sempre encontram uma solução que seja ao mesmo tempo **barata, simples e adequada às necessidades do negócio**.

Como consequência, alguns acabam desistindo dos aplicativos e voltam a utilizar o WhatsApp, onde precisam responder mensagens manualmente, gastam tempo com agendamentos e podem ocorrer conflitos de horário.

**Fonte da evidência:** conversa real com um barbeiro amigo, dono da própria barbearia.

---

## requisitos/

Lista dos requisitos funcionais levantados a partir da pesquisa realizada com o barbeiro.

| Código | Requisito | Fonte |
|---|---|---|
| RF01 | Cliente vê horários livres do barbeiro | Barbeiro |
| RF02 | Cliente agenda escolhendo serviço e horário | Barbeiro |
| RF03 | Cliente cancela ou remarca sozinho | Barbeiro |
| RF04 | Dono vê agenda do dia e da semana | Barbeiro |
| RF05 | Sistema bloqueia horário já ocupado | Barbeiro |
| RF06 | Dono cadastra serviços e preços de forma simples | Barbeiro |
| RF07 | Sistema envia lembrete automático ao cliente | Barbeiro |

Lista dos requisitos não funcionais, considerando usabilidade, simplicidade, desempenho, custo e segurança.

| Código | Requisito | Categoria | Fonte |
|---|---|---|---|
| RNF01 | Cadastro de serviço e horário deve levar até 5 minutos | Usabilidade | Barbeiro |
| RNF02 | Interface deve ter no máximo 3 telas principais | Simplicidade | Barbeiro |
| RNF03 | Página de agendamento carrega em até 3 segundos no 4G | Desempenho | Equipe |
| RNF04 | Funcionar bem em celular | Usabilidade | Barbeiro |
| RNF05 | Custo de operação baixo, utilizando hospedagem gratuita ou barata | Custo | Barbeiro |
| RNF06 | Dados do cliente devem seguir a LGPD | Segurança | Equipe |


Documento que relaciona cada requisito à sua fonte, à etapa da jornada e à prioridade definida para o projeto.

| Requisito | Fonte | Jornada relacionada | Prioridade |
|---|---|---|---|
| RF01 | Barbeiro | Etapa 3 — Escolher horário | Alta |
| RF02 | Barbeiro | Etapa 3 — Escolher horário | Alta |
| RF03 | Barbeiro | Etapa 6 — Cancelar ou comparecer | Alta |
| RF04 | Barbeiro | — | Alta |
| RF05 | Barbeiro | Etapa 3 — Escolher horário | Alta |
| RF06 | Barbeiro | Etapa 2 — Escolher serviço | Média |
| RF07 | Barbeiro | Etapa 5 — Lembrete | Média |
| RNF05 | Barbeiro | — | Alta |

---

## jornada/

Mapa da experiência do cliente durante o processo de agendamento.

| Etapa | O que acontece | Dor | Oportunidade |
|---|---|---|---|
| 1. Descobre a barbearia | Vê no Instagram ou passa na frente | Não sabe se tem vaga | Link direto para agendar |
| 2. Escolhe serviço | Vê corte, barba ou combo | Preço não fica claro | Serviço com preço visível |
| 3. Escolhe horário | Vê horários livres | Medo de conflito | Bloqueio automático |
| 4. Confirma | Recebe confirmação na hora | Não sabe se deu certo | Confirmação imediata |
| 5. Lembrete | Recebe aviso antes | Esquece o horário | Lembrete automático |
| 6. Cancela ou comparece | Desmarca pelo app ou comparece | Cancelar pelo WhatsApp é trabalhoso | Cancelamento em 1 clique |

#### Momentos críticos

- **Maior valor:** cliente consegue realizar o agendamento sozinho, sem depender da resposta do barbeiro.
- **Maior risco de frustração:** conflito de horário ou utilização de um aplicativo complicado demais.

Registro das principais falas e evidências coletadas durante a pesquisa.

#### Fonte

Conversa real com um barbeiro amigo, dono da própria barbearia.

#### Relatos coletados

> "Já usei dois apps, mas um cobrava mensalidade alta e o outro era complicado demais."

> "No WhatsApp eu resolvo, mas perco tempo e às vezes dois clientes marcam no mesmo horário."

> "Queria algo simples e barato. Só ver a agenda e o cliente marcar sozinho."

> "Não preciso de relatório, financeiro, nada disso. Só agenda."

#### Conclusões da pesquisa

1. Simplicidade e custo baixo são requisitos de primeira linha e não apenas características de usabilidade.
2. O problema central está na dependência do barbeiro para responder aos clientes e na possibilidade de conflito de horários.
3. Funcionalidades extras, como relatórios, controle financeiro e suporte a múltiplos barbeiros, não são prioridade no primeiro ciclo.
4. O WhatsApp representa a principal solução utilizada atualmente e, portanto, é uma referência importante para o projeto.

---

## Escopo inicial priorizado

### Prioridade alta — MVP

- RF01 — Cliente vê horários livres.
- RF02 — Cliente agenda escolhendo serviço e horário.
- RF03 — Cliente cancela ou remarca sozinho.
- RF04 — Dono vê a agenda do dia e da semana.
- RF05 — Sistema bloqueia horários já ocupados.
- RNF01 — Cadastro simples.
- RNF02 — Interface simples.
- RNF04 — Funcionamento adequado em celular.
- RNF05 — Baixo custo de operação.

### Prioridade média

- RF06 — Cadastro de serviços e preços.
- RF07 — Lembretes automáticos.
- RNF03 — Desempenho de carregamento.
- RNF06 — Conformidade com a LGPD.

### Prioridade baixa — Próximo ciclo

- Relatórios.
- Controle financeiro.
- Suporte a múltiplos barbeiros.
- Integração com pagamentos.

### Justificativa

O escopo foi definido com base na evidência obtida durante a conversa com o barbeiro.

As principais necessidades identificadas foram:

- simplicidade;
- baixo custo;
- visualização da agenda;
- autonomia do cliente para realizar o agendamento;
- prevenção de conflitos de horário.

Por esse motivo, o MVP prioriza as funcionalidades diretamente relacionadas a esses problemas e deixa recursos complementares para ciclos futuros.

O RNF05, relacionado ao baixo custo de operação, também influencia a escolha das tecnologias, infraestrutura e hospedagem desde o início do projeto.

---

## Objetivo do projeto

Desenvolver uma solução simples de agendamento online para pequenas barbearias, permitindo que o cliente escolha o serviço e o horário disponível sem depender de uma resposta manual pelo WhatsApp.

Ao mesmo tempo, o sistema deve ajudar o barbeiro a organizar sua agenda, evitar conflitos de horário e reduzir o tempo gasto com atendimento relacionado aos agendamentos.

---

## Escopo do MVP

O MVP será focado nas funções essenciais para validar a solução:

1. Visualização de horários disponíveis.
2. Escolha de serviço.
3. Agendamento.
4. Cancelamento ou remarcação.
5. Visualização da agenda pelo barbeiro.
6. Bloqueio automático de horários ocupados.
7. Interface simples e adaptada para celular.
8. Operação com baixo custo.

Funcionalidades administrativas e integrações mais complexas serão avaliadas em ciclos posteriores, após a validação do produto inicial.

---

## Fonte da pesquisa

A definição do problema, dos requisitos e do escopo foi baseada em uma conversa real com um barbeiro proprietário de uma barbearia de pequeno porte.

Essa pesquisa permitiu identificar problemas reais relacionados ao uso do WhatsApp e às dificuldades encontradas em aplicativos de agendamento já testados.

A evidência coletada foi utilizada como base para a definição dos requisitos e para a priorização do MVP.
