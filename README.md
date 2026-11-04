# Sistema de Apoio ao ENADE (Web & Mobile) - Unifor
**Disciplina:** Requisitos e Modelagem de Sistemas
**Sprint 1 (Milestone M1):** 19/10/2026 a 01/11/2026

---

## 1. Documento de Visão
* **Contexto:** O ENADE é componente curricular obrigatório e indicador fundamental da qualidade do ensino superior brasileiro.
* **Problemática (Visão do Estudante):** Os estudantes enfrentam dificuldades no preparo devido à falta de materiais organizados, simulados práticos, feedback imediato sobre desempenho, canais dinâmicos para tirar dúvidas entre colegas e incentivos práticos que mantenham o engajamento contínuo.
* **Problemática (Visão Docente, Coordenação e Controle Populacional):** Professores, coordenadores e administradores enfrentam dificuldades para mapear e controlar com precisão o universo de alunos aptos ao ENADE no ano vigente, além de carecerem de monitoramento contínuo e de um **retorno prévio (diagnóstico antecipado)** sobre o nível de preparo das turmas antes do exame oficial.
* **Objetivo Geral:** Especificar uma plataforma integrada **Web e Mobile** de questões comentadas e simulados do ENADE (seguindo o padrão IEEE 830), integrada diretamente ao **AVA Unifor** para controle populacional automático, geração de planilhas gerenciais de alunos concluintes/ingressantes do ano e monitoramento pedagógico prévio.
* **Proposta de Valor e Incentivo aos Alunos (O que o aluno ganha?):**
  1. **Horas de Atividades Complementares Sincronizadas no AVA:** Emissão e registro automático de horas complementares a cada trilha de simulados concluída com aproveitamento mínimo.
  2. **Pontos Extras por Monitoria Solidária:** Alunos que respondem dúvidas de colegas na aba Tira-Dúvidas ou enviam sugestões de estudo que recebem o selo de validação do professor ganham pontuação extra no sistema de recompensas.
  3. **Bonificação Acadêmica Integrada:** Relatórios e planilhas de participação exportáveis para que professores concedam pontuação bônus parcial em disciplinas do AVA Unifor aos alunos que cumprirem as metas diagnósticas.
  4. **Gamificação e Microcertificados:** Sistema de ofensivas de estudo (*streaks*), ranking opcional de colaboração e selos digitais de proficiência por área de conhecimento.
* **Escopo do Sistema:** Integração com o AVA Unifor (login institucional SSO e importação da base de alunos elegíveis no ano), exportação de planilhas/dados nominais para professores e administradores, banco de questões (organizadas por ano, curso/área e componente), gabarito comentado, aba dinâmica de tira-dúvidas e sugestões aluno-para-aluno com revisão periódica docente, simulados cronometrados, painel de retorno prévio e módulo de recompensas acadêmicas.

---

## 2. Identificação de Stakeholders
| Stakeholder | Papel / Perfil | Interesse e Responsabilidade no Sistema |
| :--- | :--- | :--- |
| **Estudantes de Graduação** | Usuário Primário (App Mobile / Web) | Acessar via credenciais do AVA Unifor, realizar simulados, resolver questões, publicar sugestões, interagir na aba Tira-Dúvidas e acumular horas complementares. |
| **Professores (Admin Pedagógico)** | Apoio Pedagógico e Revisor (Web/Mobile) | Receber retorno prévio sobre dificuldades da turma, exportar planilhas de desempenho dos seus alunos aptos ao ENADE no ano e revisar periodicamente a aba Tira-Dúvidas. |
| **Coordenações de Curso** | Gestor Acadêmico (Portal Web) | Controlar a população de estudantes enquadrados no ENADE daquele ano, exportar planilhas gerenciais completas e planejar intervenções pedagógicas prévias. |
| **Administradores do Sistema** | Gestão Técnica e Operacional | Gerenciar a sincronização com o AVA Unifor, extrair relatórios/planilhas globais de alunos elegíveis no ano, moderar a comunidade e alimentar o banco de questões do INEP. |
| **AVA Unifor (Sistema Acadêmico)** | Sistema Externo Integrado | Fornecer autenticação institucional (SSO), dados de matrícula, curso, percentual de integralização curricular e receber os registros de horas complementares. |

---

## 3. Roteiro e Resultados de Entrevistas
### Roteiro Aplicado (Estudantes, Professores e Coordenação)
1. Quais dificuldades você encontra ao buscar provas anteriores do ENADE no portal do INEP?
2. Qual a importância de visualizar um gabarito comentado logo após responder uma questão?
3. Você acharia útil uma aba dinâmica onde os próprios colegas pudessem responder suas dúvidas e deixar sugestões de estudo, com revisão periódica de um professor?
4. Que tipo de recompensa prática integrada ao AVA Unifor (horas complementares, bônus em nota) faria você utilizar o aplicativo toda semana?
5. **(Para Professores/Coordenação/Admin):** Qual o impacto de ter o sistema integrado ao AVA Unifor gerando automaticamente uma planilha pronta com todos os alunos que farão o ENADE naquele ano e o respectivo status de preparo?

### Síntese dos Resultados Elicitados
* **89% dos estudantes** relataram que provas soltas em PDF dificultam o estudo, preferindo um aplicativo Mobile/Web integrado ao login do AVA Unifor com questões filtradas por ano, curso e componente.
* **94% dos entrevistados** apontaram o **Gabarito Comentado** como essencial para entender o conceito das respostas.
* **86% dos estudantes** destacaram que aprendem mais rápido com **dicas e sugestões de outros alunos** e uma aba **Tira-Dúvidas aberta à comunidade**, desde que revisada periodicamente por um professor.
* **91% dos estudantes** afirmaram que a conversão automática de metas em **Horas Complementares no AVA** e **bônus em disciplinas** aumentaria drasticamente sua adesão.
* **100% dos Coordenadores e Professores** apontaram que a **integração com o AVA Unifor** para controle populacional e a **exportação de planilhas (`.xlsx`/`.csv`) dos alunos que farão o ENADE no ano** eliminam o trabalho manual de cruzamento de matrículas e permitem cobrar engajamento de quem está inativo antes da prova.

---

## 4. Requisitos do Sistema (Padrão IEEE 830)
### 4.1. Requisitos Funcionais (RF)
* **RF01 - Autenticação Integrada (SSO AVA Unifor):** Permitir login unificado utilizando as credenciais institucionais do AVA Unifor para estudantes, professores, coordenadores e administradores nas plataformas Web e Mobile.
* **RF02 - Sincronização e Controle Populacional via AVA:** Importar e sincronizar automaticamente via API do AVA Unifor a relação de estudantes matriculados, identificando o grupo populacional que realizará o ENADE no ano vigente (com base no curso e percentual de integralização da grade).
* **RF03 - Exportação de Planilhas de Alunos do ENADE do Ano:** Permitir que professores, coordenadores e administradores gerem e exportem planilhas estruturadas (`.xlsx` e `.csv`) contendo a lista nominal dos alunos que farão o ENADE naquele ano, matrícula, turma, simulados realizados, média de acertos, horas acumuladas e alerta de inatividade.
* **RF04 - Banco de Questões:** Permitir o cadastro de questões organizadas por ano, curso/área de conhecimento e componente (Formação Geral e Conhecimento Específico).
* **RF05 - Busca e Resolução Prática:** Permitir busca e filtragem de questões para resolução em computadores ou smartphones.
* **RF06 - Gabarito Comentado:** Exibir gabarito comentado com explicações detalhadas após a submissão da resposta.
* **RF07 - Simulados Cronometrados:** Gerar simulados cronometrados para prática realista do exame.
* **RF08 - Aba Tira-Dúvidas Colaborativa:** Disponibilizar uma aba de dúvidas vinculada às questões e temas gerais, onde qualquer estudante pode postar perguntas e os próprios alunos podem respondê-las imediatamente.
* **RF09 - Mural de Sugestões Aluno-para-Aluno:** Permitir que estudantes publiquem dicas de estudo, resumos estratégicos e sugestões de resolução para auxiliar outros alunos, com sistema de votos positivos (*upvotes*).
* **RF10 - Fila de Revisão Periódica (Professor/Admin):** Disponibilizar um painel de curadoria para que administradores professores revisem periodicamente as respostas e sugestões dos alunos, atribuindo o selo *"Validado pelo Professor"*, editando complementos ou ocultando informações incorretas.
* **RF11 - Estatísticas do Estudante:** Apresentar gráficos de desempenho individual por área de conhecimento.
* **RF12 - Monitoramento e Retorno Prévio (Docentes/Coordenação):** Disponibilizar um painel gerencial com alertas antecipados sobre os conteúdos de maior dificuldade da população de alunos do ENADE do ano vigente.
* **RF13 - Gamificação e Recompensas Acadêmicas:** Contabilizar pontos de engajamento (XP por simulados e respostas validadas no Tira-Dúvidas) e sincronizar comprovantes para validação de Horas Complementares e bonificação docente no AVA Unifor.

### 4.2. Requisitos Não Funcionais (RNF)
* **RNF01 (Arquitetura Web e Mobile):** Aplicação Web responsiva (foco em estudo detalhado, curadoria docente, exportação de planilhas e painéis de coordenação) e aplicativo Mobile (foco em resolução rápida, tira-dúvidas dinâmico e gamificação).
* **RNF02 (Segurança e Conformidade LGPD):** Senhas/tokens autenticados via OAuth2/JWT com o AVA Unifor e controle de acesso restrito na exportação de planilhas nominais de alunos, em conformidade com a Lei Geral de Proteção de Dados (LGPD).
* **RNF03 (Desempenho):** Tempo de resposta inferior a 2 segundos para filtragem de questões e inferior a 5 segundos para geração e download da planilha consolidada de alunos do ano.
* **RNF04 (Interoperabilidade):** Comunicação automatizada via API RESTful com os serviços acadêmicos do AVA Unifor para atualização diária de matrículas e aptidão ao ENADE.
* **RNF05 (Usabilidade):** Diferenciação visual clara entre respostas da comunidade e respostas validadas por um professor administrador.

---

## 5. Regras de Negócio (RN)
* **RN01:** O simulado padrão deve conter 40 questões (10 de Formação Geral e 30 de Conhecimento Específico) com limite de 4 horas.
* **RN02:** O gabarito comentado, as sugestões e a aba Tira-Dúvidas ficam bloqueados durante a realização do simulado cronometrado.
* **RN03:** O simulado é encerrado e submetido automaticamente quando o cronômetro atinge zero.
* **RN04:** Somente professores e administradores podem publicar ou editar gabaritos comentados oficiais.
* **RN05 (Critério de Recompensa por Simulado):** Para desbloquear a sincronização de Horas Complementares no AVA Unifor, o estudante deve concluir no mínimo 3 simulados cronometrados com taxa de acerto igual ou superior a 50%.
* **RN06 (Alerta de Retorno Prévio):** Sempre que um tópico apresentar taxa de acerto média da turma inferior a 40%, o sistema deve destacar o tema em vermelho no painel de retorno prévio dos professores e coordenadores.
* **RN07 (Dinâmica de Publicação e Revisão Periódica):** As respostas e sugestões enviadas por alunos na aba Tira-Dúvidas são publicadas imediatamente com o status *"Comunidade"*; periodicamente, o professor administrador revisa as postagens, concedendo o selo *"Verificado pelo Professor"* (que fixa a resposta no topo e concede XP extra ao autor) ou removendo conteúdos inadequados.
* **RN08 (Enquadramento Populacional Automático via AVA Unifor):** O sistema classifica automaticamente como *"Elegível ao ENADE no Ano Vigente"* os estudantes de cursos pertencentes ao ciclo trienal do MEC cujo percentual de integralização curricular no AVA Unifor atinja a faixa de concluinte (≥ 80%) ou ingressante definida no edital do INEP.
* **RN09 (Escopo de Exportação da Planilha):** Administradores exportam a planilha populacional de todos os cursos da Unifor; Coordenadores exportam a planilha completa do seu respectivo curso; Professores exportam a planilha filtrada pelos alunos matriculados em suas turmas no AVA Unifor.

---

## 6. Backlog Priorizado
| ID | História de Usuário | Prioridade | Requisitos | Sprint |
| :--- | :--- | :---: | :---: | :---: |
| **US01** | Como usuário, quero me autenticar via Web ou Mobile usando meu login institucional do AVA Unifor. | Alta (Must) | RF01, RNF01, RNF02 | Sprint 1 |
| **US02** | Como administrador/coordenador, quero que o sistema sincronize com o AVA Unifor para mapear automaticamente a população de alunos que fará o ENADE no ano. | Alta (Must) | RF02, RNF04, RN08 | Sprint 1 |
| **US03** | Como administrador, quero cadastrar questões por ano, curso e componente. | Alta (Must) | RF04 | Sprint 1 |
| **US04** | Como estudante, quero filtrar questões por área e ano no app ou web para praticar. | Alta (Must) | RF05, RNF03 | Sprint 1 |
| **US05** | Como professor/coordenador/admin, quero exportar uma planilha (`.xlsx`/`.csv`) com os dados dos alunos que farão o ENADE no ano e seu status de preparo. | Alta (Must) | RF03, RN08, RN09 | Sprint 2 |
| **US06** | Como estudante, quero consultar o gabarito comentado e realizar simulados cronometrados. | Alta (Must) | RF06, RF07, RN01-04 | Sprint 2 |
| **US07** | Como professor/coordenador, quero acessar o painel de monitoramento e retorno prévio para identificar lacunas da turma antes do ENADE. | Alta (Must) | RF12, RN06 | Sprint 2 |
| **US08** | Como estudante, quero postar sugestões de estudo e responder dúvidas de colegas na aba Tira-Dúvidas para manter o estudo dinâmico. | Média (Should) | RF08, RF09, RN07 | Sprint 2 |
| **US09** | Como professor administrador, quero revisar periodicamente as respostas e sugestões dos alunos para validar conteúdos corretos. | Média (Should) | RF10, RN07, RNF05 | Sprint 3 |
| **US10** | Como estudante, quero acumular metas e respostas validadas para contabilizar horas complementares e bonificação no AVA Unifor. | Média (Should) | RF11, RF13, RN05 | Sprint 3 |

---

## 7. Diagramas UML

### 7.1. Diagrama de Casos de Uso
~~~mermaid
flowchart LR
    Est(["👤 Estudante"])
    Prof(["👨‍🏫 Professor (Admin Revisor)"])
    Coord(["📊 Coordenador"])
    Adm(["🛠️ Administrador"])
    AVA(["🏛️ Sistema AVA Unifor"])

    subgraph Sistema de Apoio ao ENADE - Web e Mobile
        UC1("UC01 - Autenticar via SSO AVA Unifor")
        UC2("UC02 - Sincronizar População de Alunos Aptos no Ano")
        UC3("UC03 - Exportar Planilha de Alunos do ENADE do Ano (.xlsx/.csv)")
        UC4("UC04 - Filtrar Questões e Realizar Simulado Cronometrado")
        UC5("UC05 - Consultar Gabarito Comentado")
        UC6("UC06 - Postar Sugestões e Responder na Aba Tira-Dúvidas")
        UC7("UC07 - Revisar e Validar Dúvidas/Sugestões Periodicamente")
        UC8("UC08 - Monitorar Retorno Prévio da Turma")
        UC9("UC09 - Contabilizar Metas e Horas Complementares")
        UC10("UC10 - Gerenciar Banco de Questões e Gabaritos")
    end

    Est --> UC1 & UC4 & UC6 & UC9
    UC4 -.->|"<<extend>>"| UC5
    Prof --> UC1 & UC3 & UC6 & UC7 & UC8 & UC10
    UC6 -.->|"<<extend>>"| UC7
    Coord --> UC1 & UC2 & UC3 & UC8
    Adm --> UC1 & UC2 & UC3 & UC7 & UC10

    UC1 --> AVA
    UC2 --> AVA
    UC9 --> AVA
~~~

### 7.2. Diagrama de Componentes
~~~mermaid
flowchart TB
    subgraph Front-end Multiplataforma
        Web["[Componente] Portal Web (Estudo, Curadoria & Exportação de Planilhas)"]
        Mob["[Componente] App Mobile (Prática, Tira-Dúvidas & Gamificação)"]
    end
    subgraph Back-end API - Sistema ENADE
        API["[Componente] API Gateway"]
        Auth["[Componente] Autenticação SSO & Conector AVA Unifor"]
        PopCtrl["[Componente] Controle Populacional & Exportador de Planilhas (XLSX/CSV)"]
        BancoQ["[Componente] Banco de Questões & Gabaritos"]
        Sim["[Componente] Simulados Cronometrados"]
        TiraDuvidas["[Componente] Aba Tira-Dúvidas, Sugestões & Revisão Docente"]
        Monit["[Componente] Motor de Monitoramento & Retorno Prévio"]
        Gamif["[Componente] Módulo de Gamificação & Horas Complementares"]
    end
    subgraph Sistemas Externos e Persistência
        AVA_API["[Interface Externa] API AVA Unifor (Matrículas & Turmas)"]
        DB[("PostgreSQL")]
    end

    Web & Mob -->|HTTPS/REST| API
    API --> Auth & PopCtrl & BancoQ & Sim & TiraDuvidas & Monit & Gamif
    Auth & PopCtrl & Gamif -->|REST / OAuth2| AVA_API
    Auth & PopCtrl & BancoQ & Sim & TiraDuvidas & Monit & Gamif --> DB
~~~

### 7.3. Diagrama de Implantação
~~~mermaid
flowchart LR
    subgraph Cliente ["«device» Dispositivos dos Usuários"]
        Nav["«executionEnvironment» Navegador Web (PC/Notebook)"]
        App["«executionEnvironment» App Mobile (Android/iOS)"]
    end
    subgraph Nuvem ["«node» Servidor de Aplicação Cloud"]
        Container["«executionEnvironment» Container Docker (API ENADE + Exportador XLSX)"]
    end
    subgraph Infra_Unifor ["«node» Infraestrutura Acadêmica Unifor"]
        AVA_Srv["«executionEnvironment» Servidor AVA Unifor (REST API / SSO)"]
    end
    subgraph BaseDados ["«node» Servidor de Banco de Dados"]
        PG["«executionEnvironment» PostgreSQL Server"]
    end

    Nav -- "HTTPS (443)" --> Container
    App -- "HTTPS (443)" --> Container
    Container -- "HTTPS / OAuth2 (443)" --> AVA_Srv
    Container -- "TCP/IP (5432)" --> PG
~~~
