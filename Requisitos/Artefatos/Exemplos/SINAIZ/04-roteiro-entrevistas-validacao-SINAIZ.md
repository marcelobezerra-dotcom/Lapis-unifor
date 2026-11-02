# Roteiro de Entrevistas para Validação de Requisitos — SINAIZ

![Logomarca proposta SINAIZ](assets/logo-sinaiz.png)

**Sistema de Inteligência Acadêmica e Internacionalização**  
**Identificador:** ENT-SINAIZ-001 | **Versão:** 1.0 | **Data:** 02/11/2026  
**Base de rastreabilidade:** Visão da Demanda SINAIZ v2.3 (F-01 a F-26; M01 a M06).  
**Natureza:** material didático para Requisitos e Modelagem de Sistemas — Unifor. **Não aprovado institucionalmente.**

> **Legenda:** **Definido na VD** = decisão descrita na visão; **Proposto** = detalhamento para validação; **Pendente** = informação a confirmar com interessados.

## 1. Objetivo da entrevista

Validar as hipóteses e decisões da **Visão da Demanda v2.3**, identificar conflitos entre interessados, definir critérios de aceitação e transformar pontos pendentes em decisões rastreáveis. Este roteiro **não pressupõe** que as respostas já tenham sido dadas ou aprovadas.

**Participantes previstos:** Prof. Marcelo Ponte (interlocutor), direção da DRI (aprovação), Gestor e Analista de Internacionalização, docentes, TI/UOL/identidade, responsável por dados pessoais e, quando aplicável, representantes das integrações.

## 2. Preparação da equipe entrevistadora

1. Ler VD v2.3, glossário e RNF; marcar hipóteses e questões PQ-01 a PQ-13.
2. Selecionar participantes de acordo com a matriz abaixo; agendar entrevistas separadas quando necessário.
3. Preparar exemplos de currículo, artigo com coautoria, evento importado e indicador; **usar dados fictícios** no exercício.
4. Definir moderador, responsável pelas anotações e pessoa que controla o tempo.
5. Solicitar consentimento para gravação, se houver; não presumir autorização.
6. Registrar decisões com identificador, responsável, data e evidência.

### 2.1 Matriz de sessões sugeridas

| Sessão | Público | Duração sugerida | Ênfase |
| --- | --- | --- | --- |
| E01 | Marcelo Ponte + Gestor da DRI | 60–75 min | Objetivos, indicadores, escopo, aprovação |
| E02 | Analistas da DRI | 60 min | Oportunidades, curadoria, inconsistências, e-mail |
| E03 | Docentes (amostra de áreas distintas) | 40–50 min | Consulta, compreensão, exportação e confiança |
| E04 | TI/UOL/identidade/CNPq | 60–75 min | Integrações, dados, autenticação, operação |
| E05 | TI/segurança/encarregado de dados | 45–60 min | LGPD, acessos, retenção, RNF |
| E06 | Reunião de consolidação com DRI | 45 min | Conflitos, prioridades, aceite e pendências |

## 3. Abertura — roteiro sugerido

> Estamos validando um estudo de caso do SINAIZ, pensado para apoiar a internacionalização acadêmica. A proposta atual ainda não está aprovada. Queremos confirmar necessidades reais, regras, dados disponíveis, limites e prioridades. Vou apresentar cenários e registrar o que está confirmado, o que precisa de ajuste e o que permanece pendente. Podemos começar pelo seu trabalho atual?

## 4. Perguntas comuns a todos os interessados

| ID | Pergunta aberta | Objetivo / evidência | Rastreabilidade |
| --- | --- | --- | --- |
| Q-G01 | Qual decisão ou tarefa o SINAIZ deveria tornar mais simples? | Validar problema e valor | VD §1–3 |
| Q-G02 | Como essa tarefa é realizada hoje? Pode demonstrar? | Obter processo atual, evidências e dificuldades | VD §2 |
| Q-G03 | Quais dados você usa e em quais sistemas os consulta? | Confirmar fontes e lacunas | M01–M03 |
| Q-G04 | O que seria um resultado útil e confiável? | Critérios de sucesso | VD §3 |
| Q-G05 | O que seria um erro grave ou um resultado enganoso? | Riscos e exceções | RNF-10–RNF-13 |
| Q-G06 | Quais funcionalidades são indispensáveis na primeira entrega? | Priorização | F-01–F-26 |
| Q-G07 | Quem pode ver, alterar, validar ou publicar cada informação? | Perfis e governança | M05 |
| Q-G08 | Que situação importante ainda não aparece no documento? | Descobrir requisitos ausentes | Todos |

## 5. Sessão E01 — Solicitante, gestor e direção da DRI

### 5.1 Objetivos e alcance
| ID | Pergunta | Evidência / decisão esperada | Ref. |
| --- | --- | --- | --- |
| Q-DRI-01 | Qual problema institucional motiva a demanda? Qual é o custo atual? | Problema mensurável | VD §2–3 |
| Q-DRI-02 | O foco inicial é exclusivamente a DRI? Quais atividades ficam fora? | Limite de escopo | VD §4, §7 |
| Q-DRI-03 | Quem aprova oficialmente requisitos, metodologia de indicadores e implantação? | Papéis e aprovação | PQ-10, PQ-13 |
| Q-DRI-04 | Quais resultados devem aparecer na tela inicial? | Priorização do painel | F-13, F-25 |
| Q-DRI-05 | A consulta deve considerar todos os docentes ou recortes específicos? | Universo e acesso | M01, M03 |
| Q-DRI-06 | Como distinguir produção anterior, durante e posterior ao vínculo? | Regra temporal | PQ-13 |
| Q-DRI-07 | Como tratar docentes vinculados a mais de um curso? | Contagem e agregação | PQ-13 |
| Q-DRI-08 | Quais resultados precisam de exportação formal? | Conteúdo dos relatórios | F-13, F-25 |

### 5.2 Indicadores — principal bloco de validação
| ID | Pergunta | Evidência / decisão esperada | Ref. |
| --- | --- | --- | --- |
| Q-IND-01 | Quais dos IND-01 a IND-07 são relevantes? Quais faltam? | Catálogo inicial homologável | VD §6.4 |
| Q-IND-02 | O que exatamente significa “internacionalização” para a DRI? | Definição institucional | F-07, PQ-03 |
| Q-IND-03 | Artigo internacional depende da sede do periódico, do idioma ou de outro critério? | Confirmação ou revisão da regra | F-07 |
| Q-IND-04 | Livro/capítulo depende da sede da editora? Como verificar a sede? | Evidência classificatória | F-07 |
| Q-IND-05 | Como classificar evento presencial, virtual e híbrido? | Regras e exceções | F-07, F-12 |
| Q-IND-06 | Qual a diferença entre participação em evento e oportunidade de submissão? | Evitar mistura de métricas | IND-04, IND-06 |
| Q-IND-07 | Uma publicação de dois docentes conta uma vez na Unifor e uma vez para cada docente? | Deduplicação | RN-IND-03 |
| Q-IND-08 | Como tratar ausência de país, editora ou identificador? | Não classificáveis | RN-IND-05 |
| Q-IND-09 | Que dimensões e filtros o gestor deve poder combinar? | Catálogo do construtor | F-21 |
| Q-IND-10 | O gestor pode criar indicadores oficiais diretamente ou há aprovação adicional? | Governança | PQ-13, F-23 |
| Q-IND-11 | Que estados são necessários: rascunho, ativo, inativo? | Ciclo de vida | F-23 |
| Q-IND-12 | Mudança de regra deve recalcular anos anteriores ou preservar séries emitidas? | Versionamento e histórico | RN-IND-06 |
| Q-IND-13 | Que metas precisam ser cadastradas? Quem as define e revisa? | Escopo de metas | F-24 |
| Q-IND-14 | Como comprovar o cálculo de um indicador para auditoria? | Drill-down e proveniência | F-25, RNF-11 |
| Q-IND-15 | O que o sistema deve mostrar quando o denominador é zero? | Regra de percentual | RN-IND-04 |
| Q-IND-16 | Quais gráficos são úteis? Quais podem induzir interpretação errada? | Visualização | F-21, F-25 |
| Q-IND-17 | Como diferenciar um indicador oficial de uma análise exploratória? | Comunicação e publicação | PQ-09 |
| Q-IND-18 | Que dados mínimos tornam um indicador confiável? | Cobertura e alerta | F-26 |

**Dinâmica prática:** apresente uma tabela fictícia com dois docentes coautores de um artigo, um periódico sem país e um docente inativo. Peça que o gestor calcule IND-02 manualmente e explique quais registros entram. Registre a regra antes de demonstrar a proposta do sistema.

## 6. Sessão E02 — Analistas de Internacionalização

| ID | Pergunta | Evidência / decisão esperada | Ref. |
| --- | --- | --- | --- |
| Q-ANA-01 | Como vocês descobrem e registram oportunidades hoje? | Fluxo atual | M02 |
| Q-ANA-02 | Quais campos são obrigatórios para publicar uma oportunidade manual? | Regras de cadastro | F-09 |
| Q-ANA-03 | A publicação manual deve ser imediata em todos os casos? | Confirmar exceções | F-09 |
| Q-ANA-04 | Como validar uma oportunidade importada do ResearchRadar? | Critérios de aprovação | F-10 |
| Q-ANA-05 | Como reconhecer oportunidades duplicadas quando título ou data mudam? | Chave e tratamento de duplicidade | F-11 |
| Q-ANA-06 | O que fazer quando prazo, custo ou modalidade estão ausentes? | Qualidade da oportunidade | F-12 |
| Q-ANA-07 | Quais inconsistências do Lattes vocês conseguem identificar? | Taxonomia e prioridades | F-15 |
| Q-ANA-08 | Quando uma inconsistência passa de pendente para em análise e resolvida? | Fluxo de estados | F-15 |
| Q-ANA-09 | Que conteúdo deve aparecer no rascunho de e-mail ao docente? | Modelo de comunicação | F-16 |
| Q-ANA-10 | Quem revisa e aciona o envio? Quando é permitido reenviar? | Autorização e histórico | F-16 |
| Q-ANA-11 | Como comprovar que o dado foi corrigido na origem? | Critério de encerramento | F-03, F-15 |
| Q-ANA-12 | Quais filtros, exportações e indicadores são usados diariamente? | Usabilidade e prioridades | F-12, F-13, F-25 |

**Dinâmica prática:** mostrar duas oportunidades quase iguais (uma manual e outra importada) e pedir decisão: publicar, rejeitar, sinalizar duplicidade ou solicitar revisão.

## 7. Sessão E03 — Docentes

| ID | Pergunta | Evidência / decisão esperada | Ref. |
| --- | --- | --- | --- |
| Q-DOC-01 | Quais dados da sua produção você gostaria de localizar? | Necessidades de consulta | F-04–F-08 |
| Q-DOC-02 | É útil consultar a produção de outros docentes? Com quais limites? | Escopo de acesso | AT-04, RNF-05 |
| Q-DOC-03 | Que filtros e formatos de exportação seriam úteis? | Consultas e relatórios | F-13 |
| Q-DOC-04 | Como você reconheceria que uma publicação foi classificada incorretamente? | Transparência | F-07 |
| Q-DOC-05 | O que deveria constar em um aviso de inconsistência? | Linguagem da notificação | F-16 |
| Q-DOC-06 | Como você atualiza seu Lattes? Que dificuldades encontra? | Processo de correção na origem | M04 |
| Q-DOC-07 | Que informação deve ficar visível sobre atualização e fonte? | Confiança | RNF-10, RNF-28 |
| Q-DOC-08 | O que faria você deixar de usar o sistema? | Riscos de adoção | RNF-15, RNF-18 |

**Dinâmica prática:** pedir ao docente que encontre uma publicação, verifique a fonte e explique como corrigiria um erro (no Lattes, não no SINAIZ).

## 8. Sessão E04 — TI, UOL, identidade e integrações

| ID | Pergunta | Evidência / decisão esperada | Ref. |
| --- | --- | --- | --- |
| Q-TI-01 | O UOL expõe interface autorizada para docentes, vínculos, cursos e ID Lattes? | Contrato, campos, limites | PQ-01 |
| Q-TI-02 | Existe histórico de vínculo por período e múltiplas unidades? | Cálculo histórico | PQ-13 |
| Q-TI-03 | O SINAIZ pode consultar diretamente o Lattes Extrator? Sob qual habilitação? | Autorização e integração | PQ-02 |
| Q-TI-04 | É possível identificar mudanças semanais sem reextrair todo o acervo? | Estratégia de atualização | PQ-04 |
| Q-TI-05 | Como lidar com falhas parciais, quotas e indisponibilidade do CNPq? | Resiliência | F-03, RNF-08 |
| Q-TI-06 | Quais atributos chegam da autenticação institucional Google/UOL? | Identidade e vínculo | PQ-11 |
| Q-TI-07 | Como conceder e revogar papéis? Quem pode administrar administradores? | Segurança | F-18 |
| Q-TI-08 | O ResearchRadar oferece API, exportação ou outro meio permitido? | Viabilidade e termos | PQ-05 |
| Q-TI-09 | Que campos, limites e atualização são garantidos pelo ResearchRadar? | Cobertura de oportunidades | F-10 |
| Q-TI-10 | Qual serviço institucional pode enviar e-mails e retornar falhas? | Integração de mensagens | PQ-12 |
| Q-TI-11 | Qual volume de currículos, publicações e usuários devemos suportar? | Dimensionamento | RNF-19–RNF-23 |
| Q-TI-12 | Que política de logs, monitoramento, backup e restauração se aplica? | Operação | M06, RNF-17, RNF-22 |
| Q-TI-13 | Como adicionar uma nova fonte de oportunidades no futuro? | Extensibilidade | RNF-16 |
| Q-TI-14 | Quais ambientes, navegadores e padrões de acessibilidade são homologados? | Compatibilidade | RNF-18, RNF-24 |

**Evidências a solicitar:** documentação de API, exemplo de payload anonimizado, política de identidade, SLA, limites de consumo, esquema de dados e fluxos de falha.

## 9. Sessão E05 — Segurança, privacidade e conformidade

| ID | Pergunta | Evidência / decisão esperada | Ref. |
| --- | --- | --- | --- |
| Q-SEG-01 | Qual a finalidade institucional legítima de cada categoria de dado? | Mapeamento de finalidade | PQ-07 |
| Q-SEG-02 | Quais dados curriculares podem ser consultados por todos os docentes? | Matriz de acesso | AT-04 |
| Q-SEG-03 | Que restrições se aplicam a dados pessoais, exportações e relatórios? | Regras de compartilhamento | RNF-05 |
| Q-SEG-04 | Por quanto tempo manter histórico, inconsistências, notificações e logs? | Política de retenção | RNF-05, RNF-06 |
| Q-SEG-05 | Como atender pedidos de correção e contestação sem editar o Lattes? | Procedimento de governança | M04 |
| Q-SEG-06 | Quem pode acessar logs e qual detalhe é permitido registrar? | Auditoria com minimização | M06 |
| Q-SEG-07 | Quais requisitos de criptografia, autenticação e testes são obrigatórios? | Baseline institucional | RNF-01–RNF-04 |
| Q-SEG-08 | É necessário avaliar transferência internacional de dados para serviços externos? | Risco e tratamento | PQ-07 |

## 10. Sessão E06 — Validação consolidada

**Apresente um resumo de decisões e solicite confirmação explícita.** Não trate silêncio como aprovação.

| ID | Confirmação | Registro esperado |
| --- | --- | --- |
| V-01 | Objetivo, problema, público e escopo inicial da DRI | Aceito / alterar / pendente |
| V-02 | Perfis e permissões dos quatro usuários humanos | Aceito / alterar / pendente |
| V-03 | Classificação internacional de artigos, livros e eventos | Aceito / alterar / pendente |
| V-04 | Regras de docentes inativos, vínculo histórico e múltiplos cursos | Aceito / alterar / pendente |
| V-05 | Cadastro manual, importação ResearchRadar e duplicidades | Aceito / alterar / pendente |
| V-06 | Central de Inconsistências, notificações e reenvio | Aceito / alterar / pendente |
| V-07 | IND-01 a IND-07, construtor, versões, metas e oficialização | Aceito / alterar / pendente |
| V-08 | Integrações e limitações técnicas | Aceito / alterar / pendente |
| V-09 | RNFs e metas numéricas ainda não homologadas | Aceito / alterar / pendente |
| V-10 | Responsável e prazo para cada pendência | Nome, data e próxima ação |

## 11. Formulário de registro de resposta (copiar por pergunta)

| Campo | Preenchimento |
| --- | --- |
| Sessão / data | |
| Entrevistado / papel | |
| Pergunta ID | |
| Resposta literal ou resumo fiel | |
| Evidência / exemplo apresentado | |
| Requisito afetado (F/RNF/IND/CDU) | |
| Decisão | Confirmado / Alterar / Novo / Pendente / Rejeitado |
| Regra de negócio ou exceção identificada | |
| Prioridade atribuída | |
| Responsável pela validação | |
| Prazo / próxima ação | |

## 12. Matriz de conflitos e decisões

| ID | Tema | Posição A | Posição B | Decisor | Resolução | Situação |
| --- | --- | --- | --- | --- | --- | --- |
| CON-01 | Indicadores oficiais | A levantar | A levantar | Direção da DRI | — | Não discutido |
| CON-02 | Consulta a dados de outros docentes | A levantar | A levantar | DRI + privacidade | — | Não discutido |
| CON-03 | Produção antes do vínculo | A levantar | A levantar | DRI | — | Não discutido |
| CON-04 | Publicação de oportunidades importadas | A levantar | A levantar | DRI | — | Não discutido |

## 13. Checklist de encerramento da entrevista

- [ ] O entrevistado reconheceu o objetivo e os limites da demanda.
- [ ] Perguntas relevantes ao papel foram respondidas ou marcadas como pendentes.
- [ ] Regras e exceções foram exemplificadas com cenários.
- [ ] Decisões foram associadas a F, CDU, IND, RNF ou PQ.
- [ ] Divergências entre interessados foram registradas, sem forçar consenso.
- [ ] Responsáveis e prazos das pendências foram atribuídos.
- [ ] A ata/resumo foi encaminhada para confirmação.
- [ ] A VD e os documentos complementares serão revisados após aceite.

## 14. Critério didático de avaliação dos grupos

Avaliar se a equipe: (1) faz perguntas abertas antes de induzir respostas; (2) distingue fato de hipótese; (3) apresenta exemplos concretos; (4) cobre fluxos alternativos e exceções; (5) rastreia decisões até requisitos; (6) registra conflitos e pendências; (7) solicita confirmação dos interessados.

## 15. Ata resumida da sessão — modelo

**Sessão:** ___  **Data:** ___  **Local/formato:** ___  
**Entrevistador:** ___  **Relator:** ___  **Participantes:** ___

**Objetivo:** ___

**Pontos confirmados:** ___

**Requisitos alterados ou novos:** ___

**Divergências:** ___

**Pendências (responsável e prazo):** ___

**Próxima reunião:** ___

**Validação da ata:** pendente / confirmada em ___ por ___
