# Clínica Conecta

Projeto da disciplina Gestão de Projetos (Prof. Edson Vaz Lopes). A Clínica Conecta é uma plataforma digital centralizada de agendamento de consultas para uma rede privada de saúde com três clínicas em 
bairros diferentes da mesma cidade. Hoje cada unidade opera de forma isolada. O sistema unifica agendas, cadastro de pacientes e indicadores gerenciais, com integração obrigatória aos sistemas legados de faturamento, 
financeiro e convênios, sem interromper o atendimento diário.

## Fases do projeto

| Fase | Documento | Data / versão |
| N1 · Iniciação | Dossiê de Iniciação (Unidade 1) | 23/09/2026 · v1.0 |
| N2 · Planejamento | Relatório da Unidade 2 | 29/10/2026 · v0.1 |
| N3 · Execução | Checkpoint Consolidado (Unidade 3) | 05/11/2026 (prazo 08/11) · v1.0 |

## Problema e objetivo

Problema:gestão não unificada gera silos de informação, conflitos de horário, cancelamentos não registrados, retrabalho, alta taxa de no-show e baixa ocupação dos profissionais.

Objetivo geral:implantar um sistema de agendamento centralizado, integrado e multicanal para as três unidades, com visão única do paciente, agendas em tempo real e conformidade com a LGPD.

**Critérios de sucesso**

- 100% das agendas das três unidades no sistema, sem conflitos de horário
- Cadastro unificado acessível por qualquer unidade
- Integração funcional com faturamento, financeiro e convênios
- Redução mensurável do no-show
- Pouca ou nenhuma interrupção do atendimento na transição
- Conformidade com segurança e proteção de dados de saúde

## Abordagem

Híbrida:lógica preditiva para o que é estável e crítico (integração com legados, LGPD, controle formal de mudanças) e lógica adaptativa para o que precisa de feedback (portal do paciente e notificações). A implantação começa por uma unidade piloto antes da expansão.

## Escopo

Entregas principais

- Plataforma de agendamento centralizada e multicanal
- Cadastro unificado de pacientes e médicos
- Módulo de integração técnica com os sistemas legados
- Painel gerencial com indicadores
- Plano de transição e piloto, com treinamento

Fora do escopo:parte financeira (pagamento de médicos e consultas). Encaixes só presencialmente, não pelo site.

Restrições:continuidade do atendimento, sistemas legados insubstituíveis, LGPD e interface acessível para pessoas de baixo letramento digital.

### Backlog (frente adaptativa)

| Épico | Conteúdo |
| A · Agendamento Centralizado | Cadastro de paciente e de médico, consulta de horários, marcar, cancelar e remarcar sem conflito |
| B · Portal do Paciente e Notificações | Autoatendimento simplificado, lembretes (SMS/WhatsApp), registro de confirmação ou cancelamento |
| C · Painel de Gestão | Taxa de ocupação por unidade, relatórios de 30/60/90 dias, verificação de elegibilidade de convênio |

## Cronograma (N2)

Três releases em 12 sprints de duas semanas (24 semanas, sendo a semana 24 reserva de prazo).

| Release | Semanas | Conteúdo | Marco |
| 1 | 1 a 10 | Levantamento, integração com legados, cadastro unificado, segurança/LGPD e migração | M1: início do desenvolvimento (fim da sem. 10) |
| 2 | 11 a 18 | Agendamento, testes, treinamento da unidade piloto e piloto assistido | M2: piloto validado (fim da sem. 18) |
| 3 | 19 a 24 | Painel, portal com WhatsApp, auditoria LGPD, capacitação e expansão | M3: conclusão (fim da sem. 23) |

Caminho crítico:A → B → M1 → F → (G e I) → H → M2 → (O e N) → L → M3, com 23 semanas.
Priorização MoSCoW: Must cadastro, agendamento, integração, segurança/LGPD e piloto. Should painel, WhatsApp e expansão. Could autosserviço completo do portal.

## Orçamento

| Item | Valor |
| Pessoas (3.008 h) | R$ 134.720 |
| Fornecedores | R$ 61.000 |
| Materiais e tecnologia | R$ 15.000 |
| **Custo estimado** | **R$ 210.720** |
| Reserva de contingência | R$ 18.250 |
| **Linha de base** | **R$ 228.970** |
| Teto | R$ 240.000 |
| Reserva gerencial (folga até o teto) | R$ 11.030 |

Fornecedores:integração financeira R$ 25.000 (8 semanas), treinamento R$ 12.000, infraestrutura e nuvem R$ 18.000, mensageria WhatsApp R$ 6.000 (estimativa a confirmar com cotação) e dispositivos R$ 15.000.

Reservas de contingência (riscos de custo)

| Risco | Reserva |
| R1 · Atraso do fornecedor de integração | R$ 7.200 |
| R2 · Retrabalho de migração de dados | R$ 3.600 |
| R3 · Reteste e correções após auditoria LGPD | R$ 2.800 |
| R4 · Variação em treinamento, infraestrutura e dispositivos | R$ 2.250 |
| R5 · Baixa adesão de pacientes e resistência da equipe | R$ 2.400 |
| **Total** | **R$ 18.250** |

A contingência só é usada com aprovação do gerente e Change Request. A reserva gerencial só pode ser liberada pela Direção da rede.

Fazer ou contratar:contratar a integração, o treinamento, a nuvem e a mensageria WhatsApp. Fazer internamente o cadastro unificado e o agendamento.

## Governança

- Mudanças de escopo, custo, integração, aceite e linha de base exigem aprovação formal do patrocinador.
- A equipe decide requisitos detalhados, backlog e soluções técnicas internas.
- Matriz RACI com 13 entregas e marcos, sempre com um único A por linha.
- **Se o teto for reduzido:** proteger cadastro, agendamento, integração e LGPD. Ordem de corte: faseamento MoSCoW, redução do Designer de 50% para 25% após a semana 6 (cerca de R$ 1.600), faseamento da implantação e pedido de aumento ao patrocinador.

## Execução (N3): cinco eventos

| Evento | Responsável | Resposta |
| Riscos da integração financeira (documentação desatualizada, fornecedor com até 5 dias úteis de resposta) | Pedro Henrique | Checklist de acessos, marcos contratuais com penalidade, contato formal com os legados e escalação ao patrocinador |
| Ausência do desenvolvedor por 3 semanas | Júlia Melissa | Redistribuir tarefas, documentar conhecimento, definir substitutos e proteger o caminho crítico |
| Reclamação da direção médica | Carolina de Lima Scheibel | Registrar em 1 dia útil, reunião de validação na semana 7 ou 8, consulta a cada sprint, escalonamento em 5 dias úteis e coluna nova na RACI |
| Pedido de SMS e consentimento (LGPD) | Mateus Rodrigues | Change Request com análise de prazo, custo e escopo (análise pendente) |
| Indicadores e plano de recuperação | Erick Cristhian | Ver abaixo |

### Indicadores acumulados

| Indicador | Situação | Causa | Meta |
| Cronograma | Atraso de 2 semanas | Dependências dos legados e consolidação de dados | Zerar em até 3 sprints |
| Velocidade | 25% abaixo do previsto | Complexidade da regra contra overbooking | 100% (~250 h/sprint) |
| Satisfação do protótipo | 62% | Usabilidade para perfis de menor letramento digital | 85% |

Recomendação proposta:corrigir. Se o atraso persistir após 3 sprints, reduzir escopo via faseamento MoSCoW, com Change Request. A equipe precisa confirmar.

## Pendências

- Impacto do pedido de SMS em prazo, custo e escopo
- Matriz de probabilidade e impacto dos riscos de integração
- Prazo de folga para os até 5 dias úteis de resposta do fornecedor
- Cotação da mensageria WhatsApp (R$ 6.000 é estimativa)

## Equipe

| Integrante | Principais contribuições |
| Carolina de Lima Scheibel | N1: problema de negócio, benefícios, abordagem. N2: fornecedores e matriz RACI. N3: direção médica |
| Erick Cristhian | N1: stakeholders e governança. N2: alternativa de redução de orçamento e premissas. N3: indicadores |
| Júlia Melissa | N1: produto, objetivos e justificativa. N2: cronograma, releases e recursos. N3: contingência do desenvolvedor |
| Mateus Rodrigues | N1: viabilidade e ciclo de vida. N2: fazer ou contratar e conflitos de recursos. N3: SMS e LGPD |
| Pedro Henrique | N2: custos, orçamento e reservas. N3: riscos da integração financeira |

## Arquivos

- N1 - Iniciação: Dossiê de Iniciação (PDF)
- N2 - Planejamento: Relatório da Unidade 2 (PDF) e apresentação (PPTX)
- N3 - Execução: Checkpoint Consolidado (slides em PDF) e cronograma da equipe (PDF)
