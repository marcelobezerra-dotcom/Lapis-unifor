# Especificação de Requisitos Não Funcionais — SINAIZ

![Logomarca proposta SINAIZ](assets/logo-sinaiz.png)

**Sistema de Inteligência Acadêmica e Internacionalização**  
**Identificador:** RNF-SINAIZ-001 | **Versão:** 1.0 | **Data:** 02/11/2026  
**Base de rastreabilidade:** Visão da Demanda SINAIZ v2.3 (F-01 a F-26; M01 a M06).  
**Natureza:** material didático para Requisitos e Modelagem de Sistemas — Unifor. **Não aprovado institucionalmente.**

> **Legenda:** **Definido na VD** = decisão descrita na visão; **Proposto** = detalhamento para validação; **Pendente** = informação a confirmar com interessados.

## 1. Objetivo, escopo e método

Definir atributos de qualidade e restrições verificáveis para os seis módulos do SINAIZ. A VD v2.3 define funcionalidades e condições gerais, **mas não aprova metas técnicas quantitativas**. Portanto, os números indicados abaixo são **valores candidatos para exercício de especificação**, e devem ser homologados com a DRI e a TI antes de serem tratados como compromisso institucional.

**Classificação:** **Base VD** (derivada diretamente da visão); **Proposta** (detalhamento técnico/didático); **Pendente** (depende de decisão ou medição).

## 2. Matriz de requisitos não funcionais

| ID | Categoria | Requisito verificável | Módulos | Origem | Verificação |
| --- | --- | --- | --- | --- | --- |
| RNF-01 | Segurança | O acesso deve usar autenticação institucional, sem armazenar senha do usuário no SINAIZ. | Todos/M05 | Base VD; integração pendente | Teste de autenticação e revisão de configuração |
| RNF-02 | Autorização | Toda operação protegida e toda exportação devem validar permissões no servidor, inclusive quando a interface ocultar o botão. | Todos/M05 | Base VD | Testes de API com perfis autorizados e não autorizados |
| RNF-03 | Privilégio mínimo | Perfis Gestor, Analista, Docente e Administrador Técnico devem seguir a matriz de permissões da VD; privilégio técnico não implica acesso de negócio. | Todos/M05 | Base VD | Matriz de testes por perfil |
| RNF-04 | Proteção em trânsito | Tráfego autenticado e integrações devem usar transporte criptografado compatível com padrões institucionais. | Todos | Proposta | Inspeção de configuração e testes de conexão |
| RNF-05 | Privacidade | Dados pessoais, exportações, logs e histórico devem observar política institucional de finalidade, acesso, retenção e descarte, a ser definida com o encarregado. | Todos | Base VD; política pendente | Revisão de conformidade e evidências de controle |
| RNF-06 | Auditoria | Alterações de perfis, oportunidades, indicadores, notificações e reprocessamentos devem registrar autor, horário, ação, alvo e resultado. | M02–M06 | Base VD | Execução de cenários e inspeção de trilhas |
| RNF-07 | Integridade da fonte | Dados importados do Lattes devem permanecer somente leitura; correções devem ocorrer na fonte e ser confirmadas em sincronização posterior. | M01/M04 | Base VD | Tentativa de edição e reconciliação após sincronização |
| RNF-08 | Resiliência de lote | Falha em currículo individual não deve interromper o processamento dos demais; falhas devem ser sinalizadas. | M01/M06 | Base VD | Injeção de erro em lote de teste |
| RNF-09 | Atualização | O sistema deve permitir programação de verificação semanal de alterações do Lattes, respeitando disponibilidade e limites do provedor. | M01/M06 | Base VD; viabilidade pendente | Teste de agendamento e logs |
| RNF-10 | Rastreabilidade | Registro importado deve permitir identificar fonte, data de obtenção, versão/ciclo e status de processamento. | M01–M04 | Base VD | Amostragem de registros |
| RNF-11 | Consistência analítica | Resultados de indicadores devem identificar definição/versionamento, filtros, período, fontes e data de referência. | M03 | Base VD | Teste de exportação e detalhamento |
| RNF-12 | Deduplicação | A contagem institucional deve evitar duplicação de uma mesma produção em múltiplos currículos; a regra aplicada deve ser auditável. | M01/M03 | Base VD; algoritmo pendente | Casos de coautoria e registros equivalentes |
| RNF-13 | Qualidade de dados | Dados insuficientes para classificar internacionalização devem ser sinalizados como não classificáveis, sem classificação presumida. | M01/M03/M04 | Base VD | Casos com país/sede ausentes |
| RNF-14 | Exportação | Consultas permitidas devem poder ser exportadas para Excel e PDF, incluindo metadados necessários à interpretação do resultado. | M01–M03 | Base VD | Abrir arquivos, comparar filtros e resultados |
| RNF-15 | Usabilidade | O construtor de indicadores deve utilizar opções guiadas e controladas, sem SQL ou fórmulas arbitrárias. | M03 | Base VD | Teste de tarefas com gestor |
| RNF-16 | Evolutividade | A arquitetura deve permitir incorporar outras fontes de oportunidades no futuro sem exigir reescrita integral do fluxo de validação. | M02/M06 | Base VD; desenho proposto | Revisão de arquitetura e prova de conceito |
| RNF-17 | Observabilidade | Integrações devem registrar início, término, totais processados, sucessos, falhas e motivo de reprocessamento. | M01/M02/M06 | Base VD | Simulação de falhas e inspeção do painel |
| RNF-18 | Acessibilidade | Interfaces devem observar padrão de acessibilidade adotado pela instituição; como referência de projeto, considerar WCAG 2.2 nível AA. | Todos | Proposta | Auditoria automatizada e testes manuais |
| RNF-19 | Desempenho de consulta | **Meta candidata:** 95% das consultas usuais de docentes e oportunidades respondidas em até 3 segundos, sob carga acordada. | M01/M02 | Proposta, não homologada | Teste de carga com massa e usuários definidos |
| RNF-20 | Desempenho de painéis | **Meta candidata:** 95% dos painéis com filtros comuns carregados em até 5 segundos, sob carga acordada. | M03 | Proposta, não homologada | Teste de desempenho com dados representativos |
| RNF-21 | Disponibilidade | **Meta candidata:** disponibilidade mensal de 99,5% para a interface, excluídas janelas previamente aprovadas; depende de infraestrutura e SLA. | Todos | Proposta, não homologada | Monitoramento mensal e cálculo de disponibilidade |
| RNF-22 | Recuperação | Devem existir rotinas de cópia e recuperação dos dados próprios; **RPO/RTO ainda não definidos**. | Todos | Proposta; parâmetros pendentes | Ensaio de restauração |
| RNF-23 | Escalabilidade | A capacidade deve ser dimensionada para volume real de docentes, currículos, oportunidades e séries históricas, ainda não medido. | Todos | Pendente | Levantamento de volumetria e teste de carga |
| RNF-24 | Compatibilidade | **Proposta:** interface responsiva para navegadores institucionais homologados; matriz de versões a definir com TI. | Todos | Proposta | Testes em matriz de navegadores/dispositivos |
| RNF-25 | Mensageria | Notificação deve registrar envio, falha e reenvio; não deve afirmar entrega ao destinatário sem confirmação do serviço de e-mail. | M04 | Base VD + detalhamento | Teste com servidor de e-mail simulado |
| RNF-26 | Segurança de integrações | Credenciais de serviços externos não devem ser expostas em código, logs, URLs ou arquivos exportados. | M01/M02/M05/M06 | Proposta | Revisão de configuração e testes de vazamento |
| RNF-27 | Manutenibilidade | Regras de internacionalização e definições de indicadores devem ser rastreáveis, testáveis e alteráveis de modo controlado. | M01/M03 | Base VD + detalhamento | Testes automatizados de regressão e versionamento |
| RNF-28 | Transparência | Interface deve informar data da última atualização e avisar quando resultados dependerem de dados incompletos ou desatualizados. | M01–M03 | Base VD | Testes de interface e cenários de falha |

## 3. Requisitos por módulo e prioridades de validação

### M01 — Docentes e Currículos
Priorizar RNF-07 a RNF-10, RNF-12, RNF-13, RNF-17 e RNF-28. Testar sincronização semanal, falhas individuais, vínculo com ID Lattes, histórico e proveniência. **Não presumir que a integração direta com o CNPq esteja tecnicamente disponível** antes da confirmação formal.

### M02 — Oportunidades Científicas
Priorizar RNF-06, RNF-10, RNF-16 e RNF-17. Diferenciar publicação imediata de cadastro manual e publicação condicionada à validação de importações ResearchRadar; impedir duplicidades e registrar bloqueios.

### M03 — Indicadores de Internacionalização
Priorizar RNF-02, RNF-11 a RNF-15, RNF-20 e RNF-27. Testar total institucional distinto, recortes por docente, ausência de denominador, versão de definição, acesso a rascunhos e metadados de exportação.

### M04 — Qualidade de Dados e Notificações
Priorizar RNF-06, RNF-07 e RNF-25. Validar fluxo pendente → em análise → resolvida, preservação de histórico e notificação manual revisável com reenvio.

### M05 — Identidade e Controle de Acesso
Priorizar RNF-01 a RNF-06 e RNF-26. Confirmar a integração com identidade institucional e origem dos vínculos e papéis.

### M06 — Operação e Integrações
Priorizar RNF-08 a RNF-10, RNF-17, RNF-22 e RNF-26. Verificar monitoração, reprocessamento controlado, auditoria e recuperação.

## 4. Cenários de teste não funcional

| Teste | Preparação e ação | Resultado esperado | RNF |
| --- | --- | --- | --- |
| TNF-01 | Docente envia chamada direta à API de criação de indicador. | Operação recusada; nenhum indicador criado. | RNF-02, RNF-03 |
| TNF-02 | Dois currículos contêm o mesmo DOI; consultar total institucional. | Uma publicação no total, com critério de deduplicação rastreável. | RNF-11, RNF-12 |
| TNF-03 | Um currículo do lote semanal falha; demais são válidos. | Demais processados; falha individual registrada. | RNF-08, RNF-17 |
| TNF-04 | País do periódico ausente. | Produção sinalizada como não classificável. | RNF-13, RNF-28 |
| TNF-05 | Indicador ativo tem regra alterada. | Nova versão; versão anterior auditável. | RNF-11, RNF-27 |
| TNF-06 | Gestor exporta indicador com filtros. | PDF/Excel abrem e incluem versão, período, fonte e filtros. | RNF-11, RNF-14 |
| TNF-07 | Serviço de e-mail falha após acionamento do analista. | Falha registrada; possibilidade de reenvio sem perda do histórico. | RNF-06, RNF-25 |
| TNF-08 | Usuário tenta modificar dado importado do Lattes. | Alteração recusada. | RNF-07 |
| TNF-09 | Serviço ResearchRadar indisponível. | Falha registrada; oportunidades previamente publicadas preservadas. | RNF-17 |
| TNF-10 | Executar carga acordada de consultas e painéis. | Comparar tempos observados com metas homologadas, não com números presumidos. | RNF-19, RNF-20 |
| TNF-11 | Restaurar base a partir de cópia de segurança. | Integridade recuperada dentro de RPO/RTO a homologar. | RNF-22 |
| TNF-12 | Avaliar navegação por teclado, contraste, rótulos e mensagens. | Conformidade com padrão de acessibilidade aprovado. | RNF-18 |

## 5. Pendências técnicas e de negócio

| ID | Questão | Responsável sugerido | Efeito |
| --- | --- | --- | --- |
| P-RNF-01 | Contratos do UOL: docentes, cursos, histórico, ID Lattes e atualização. | TI/UOL | RNF-09, RNF-10, RNF-23 |
| P-RNF-02 | Habilitação, periodicidade e limites do Lattes Extrator. | TI/CNPq | RNF-08, RNF-09 |
| P-RNF-03 | API, termos, limites e cobertura do ResearchRadar. | TI/DRI | RNF-16, RNF-17 |
| P-RNF-04 | Volume de docentes, publicações, consultas e usuários simultâneos. | TI/DRI | RNF-19 a RNF-23 |
| P-RNF-05 | SLA, disponibilidade, RPO, RTO, janelas e infraestrutura. | TI | RNF-21, RNF-22 |
| P-RNF-06 | Política LGPD, perfis, retenção, logs e exportações. | Encarregado/TI/DRI | RNF-02 a RNF-06 |
| P-RNF-07 | Navegadores, acessibilidade e dispositivos-alvo. | TI/usuários | RNF-18, RNF-24 |
| P-RNF-08 | Regras oficiais de cálculo, indicadores e níveis de aprovação. | DRI | RNF-11 a RNF-15 |
| P-RNF-09 | Serviço de e-mail e evidência de envio/entrega. | TI | RNF-25 |

## 6. Checklist de homologação

- [ ] Cada RNF possui responsável, prioridade e forma de teste acordados.
- [ ] Metas numéricas de desempenho e disponibilidade foram aprovadas ou removidas.
- [ ] Políticas de acesso, privacidade, auditoria e retenção foram validadas.
- [ ] Integrações e contratos foram confirmados tecnicamente.
- [ ] Volumetria e ambientes de teste foram definidos.
- [ ] Os testes foram executados com evidências e desvios registrados.

## 7. Registro de aprovação

| Papel | Nome | Data | Resultado |
| --- | --- | --- | --- |
| DRI — negócio | A definir | — | Pendente |
| TI — arquitetura e operação | A definir | — | Pendente |
| Segurança/privacidade | A definir | — | Pendente |
