# Sistema de Apoio ao ENADE (Web & Mobile) - Unifor
**Disciplina:** Requisitos e Modelagem de Sistemas
**Sprint 1 (Milestone M1):** 19/10/2026 a 01/11/2026

---

## 1. Documento de Visão
* **Contexto:** O ENADE é componente curricular obrigatório e indicador fundamental da qualidade do ensino superior brasileiro.
* **Problemática (Visão do Estudante):** Os estudantes enfrentam dificuldades no preparo devido à falta de materiais organizados, ausência de treino focado em questões discursivas, falta de rastreamento automático dos próprios erros para revisão direcionada, escassez de canais dinâmicos para tirar dúvidas entre colegas e falta de incentivos práticos que mantenham o engajamento contínuo.
* **Problemática (Visão Docente, Coordenação e Controle Populacional):** Professores, coordenadores e administradores enfrentam dificuldades para mapear e controlar com precisão o universo de alunos aptos ao ENADE no ano vigente, além de carecerem de monitoramento contínuo e de um **retorno prévio (diagnóstico antecipado)** sobre o nível de preparo objetivo e discursivo das turmas antes do exame oficial.
* **Objetivo Geral:** Especificar uma plataforma integrada **Web e Mobile** de questões comentadas (objetivas e discursivas) e simulados do ENADE (seguindo o padrão IEEE 830), integrada diretamente ao **AVA Unifor** para controle populacional automático, geração de planilhas gerenciais de alunos do ano e monitoramento pedagógico prévio.
* **Proposta de Valor e Incentivo aos Alunos (O que o aluno ganha?):**
  1. **Horas de Atividades Complementares Sincronizadas no AVA:** Emissão e registro automático de horas complementares a cada trilha de simulados e revisões do Caderno de Erros concluída com aproveitamento mínimo.
  2. **Pontos Extras por Monitoria Solidária:** Alunos que respondem dúvidas de colegas na aba Tira-Dúvidas ou enviam sugestões de estudo que recebem o selo de validação do professor ganham pontuação extra no sistema de recompensas.
  3. **Bonificação Acadêmica Integrada:** Relatórios e planilhas de participação exportáveis para que professores concedam pontuação bônus parcial em disciplinas do AVA Unifor aos alunos que cumprirem as metas diagnósticas.
  4. **Gamificação e Microcertificados:** Sistema de ofensivas de estudo (*streaks*), ranking opcional de colaboração e selos digitais de proficiência por área de conhecimento.
* **Escopo do Sistema:** Integração com o AVA Unifor (login institucional SSO e importação da base de alunos elegíveis no ano), exportação de planilhas/dados nominais para professores e administradores, banco de questões objetivas e **treino de questões discursivas** (com espelho de correção do INEP), **caderno automático de erros** para revisão personalizada, gabarito comentado, aba dinâmica de tira-dúvidas e sugestões aluno-para-aluno com revisão periódica docente, simulados cronometrados, painel de retorno prévio e módulo de recompensas acadêmicas.

---

## 2. Identificação de Stakeholders
| Stakeholder | Papel / Perfil | Interesse e Responsabilidade no Sistema |
| :--- | :--- | :--- |
| **Estudantes de Graduação** | Usuário Primário (App Mobile / Web) | Acessar via AVA Unifor, realizar simulados, treinar questões discursivas, revisar pendências no Caderno Automático de Erros, interagir na aba Tira-Dúvidas e acumular horas complementares. |
| **Professores (Admin Pedagógico)** | Apoio Pedagógico e Revisor (Web/Mobile) | Receber retorno prévio sobre dificuldades da turma, exportar planilhas dos seus alunos aptos ao ENADE, avaliar respostas discursivas e revisar periodicamente a aba Tira-Dúvidas. |
| **Coordenações de Curso** | Gestor Acadêmico (Portal Web) | Controlar a população de estudantes enquadrados no ENADE daquele ano, exportar planilhas gerenciais completas e planejar intervenções pedagógicas prévias. |
| **Administradores do Sistema** | Gestão Técnica e Operacional | Gerenciar a sincronização com o AVA Unifor, extrair relatórios/planilhas globais de alunos elegíveis, moderar a comunidade e alimentar o banco de questões e espelhos do INEP. |
| **AVA Unifor (Sistema Acadêmico)** | Sistema Externo Integrado | Fornecer autenticação institucional (SSO), dados de matrícula, curso, percentual de integralização curricular e receber os registros de horas complementares. |

---

## 3. Roteiro e Resultados de Entrevistas
### Roteiro Aplicado (Estudantes, Professores e Coordenação)
1. Quais dificuldades você encontra ao buscar provas anteriores do ENADE no portal do INEP?
2. Qual a importância de visualizar um gabarito comentado e ter um **Caderno Automático de Erros** que separe tudo o que você errou para revisar depois?
3. Como você se prepara hoje para as **questões discursivas** do ENADE e qual o valor de ter o espelho de correção do INEP junto à revisão de um professor?
4. Você acharia útil uma aba dinâmica onde os próprios colegas pudessem responder suas dúvidas e deixar sugestões de estudo, com revisão periódica docente?
5. Que tipo de recompensa prática integrada ao AVA Unifor (horas complementares, bônus em nota) faria você utilizar o aplicativo toda semana?
6. **(Para Professores/Coordenação/Admin):** Qual o impacto de ter o sistema integrado ao AVA Unifor gerando automaticamente uma planilha pronta com todos os alunos que farão o ENADE naquele ano e o respectivo status de preparo?

### Síntese dos Resultados Elicitados
* **89% dos estudantes** relataram que provas soltas em PDF dificultam o estudo, preferindo um aplicativo Mobile/Web integrado ao login do AVA Unifor com questões filtradas por ano, curso e componente.
* **94% dos entrevistados** apontaram o **Gabarito Comentado** e o **Caderno Automático de Erros** como essenciais para não repetir as mesmas falhas nos simulados seguintes.
* **82% dos estudantes** afirmaram nunca treinar para as **questões discursivas** por falta de parâmetros claros de correção, validando o módulo discursivo com espelho oficial do INEP e feedback docente.
* **86% dos estudantes** destacaram que aprendem mais rápido com **dicas e sugestões de outros alunos** e uma aba **Tira-Dúvidas aberta à comunidade**, desde que revisada periodicamente por um professor.
* **91% dos estudantes** afirmaram que a conversão automática de metas em **Horas Complementares no AVA** e **bônus em disciplinas** aumentaria drasticamente sua adesão.
* **100% dos Coordenadores e Professores** apontaram que a **integração com o AVA Unifor** para controle populacional e a **exportação de planilhas (`.xlsx`/`.csv`) dos alunos que farão o ENADE no ano** permitem atuar diretamente sobre os alunos inativos ou com baixo rendimento antes da prova.

---

## 4. Requisitos do Sistema (Padrão IEEE 830)
### 4.1. Requisitos Funcionais (RF)
* **RF01 - Autenticação Integrada (SSO AVA Unifor):** Permitir login unificado utilizando as credenciais institucionais do AVA Unifor para estudantes, professores, coordenadores e administradores nas plataformas Web e Mobile.
* **RF02 - Sincronização e Controle Populacional via AVA:** Importar e sincronizar automaticamente via API do AVA Unifor a relação de estudantes matriculados, identificando o grupo populacional que realizará o ENADE no ano vigente.
* **RF03 - Exportação de Planilhas de Alunos do ENADE do Ano:** Permitir que professores, coordenadores e administradores exportem planilhas estruturadas (`.xlsx` e `.csv`) contendo a lista nominal dos alunos que farão o ENADE naquele ano, matrícula, turma, simulados realizados, média de acertos (objetivas e discursivas), horas acumuladas e alerta de inatividade.
* **RF04 - Banco de Questões Objetivas e Discursivas:** Permitir o cadastro de questões objetivas e discursivas organizadas por ano, curso/área de conhecimento e componente (Formação Geral e Conhecimento Específico).
* **RF05 - Busca e Resolução Prática:** Permitir busca e filtragem de questões para resolução em computadores ou smartphones.
* **RF06 - Caderno Automático de Erros:** Compilar automaticamente todas as questões que o estudante errou em simulados ou listas avulsas em um caderno inteligente de revisão, permitindo gerar treinos focados exclusivamente nas suas vulnerabilidades.
* **RF07 - Treino de Questões Discursivas:** Disponibilizar ambiente para redação de respostas discursivas com contagem de linhas/caracteres, exibição do Padrão de Resposta Oficial do INEP (espelho de correção) após o envio e encaminhamento opcional para avaliação de um professor.
* **RF08 - Gabarito Comentado:** Exibir gabarito comentado detalhado após a submissão da resposta objetiva.
* **RF09 - Simulados Cronometrados:** Gerar simulados cronometrados (incluindo questões objetivas e discursivas) para prática realista do exame.
* **RF10 - Aba Tira-Dúvidas Colaborativa:** Disponibilizar uma aba de dúvidas vinculada às questões e temas gerais, onde qualquer estudante pode postar perguntas e os próprios alunos podem respondê-las imediatamente.
* **RF11 - Mural de Sugestões Aluno-para-Aluno:** Permitir que estudantes publiquem dicas de estudo, resumos estratégicos e sugestões de resolução para auxiliar outros alunos, com sistema de votos positivos (*upvotes*).
* **RF12 - Fila de Revisão Periódica e Correção Discursiva (Professor/Admin):** Disponibilizar um painel de curadoria para que administradores professores revisem periodicamente as respostas/sugestões da aba Tira-Dúvidas (atribuindo o selo *"Validado pelo Professor"*) e avaliem respostas discursivas submetidas pelos alunos.
* **RF13 - Estatísticas do Estudante:** Apresentar gráficos de desempenho individual por área de conhecimento, taxa de superação do Caderno de Erros e evolução nas discursivas.
* **RF14 - Monitoramento e Retorno Prévio (Docentes/Coordenação):** Disponibilizar um painel gerencial com alertas antecipados sobre os conteúdos de maior dificuldade da população de alunos do ENADE do ano vigente.
* **RF15 - Gamificação e Recompensas Acadêmicas:** Contabilizar pontos de engajamento (XP por simulados, revisões do Caderno de Erros e respostas validadas no Tira-Dúvidas) e sincronizar comprovantes para validação de Horas Complementares e bonificação docente no AVA Unifor.

### 4.2. Requisitos Não Funcionais (RNF)
* **RNF01 (Arquitetura Web e Mobile):** Aplicação Web responsiva (foco em estudo detalhado, redação discursiva, curadoria docente e exportação de planilhas) e aplicativo Mobile (foco em resolução rápida, revisão do Caderno de Erros, tira-dúvidas dinâmico e gamificação).
* **RNF02 (Segurança e Conformidade LGPD):** Senhas/tokens autenticados via OAuth2/JWT com o AVA Unifor e controle de acesso restrito na exportação de planilhas nominais de alunos, em conformidade com a LGPD.
* **RNF03 (Desempenho):** Tempo de resposta inferior a 2 segundos para filtragem de questões e atualização do Caderno de Erros, e inferior a 5 segundos para geração da planilha consolidada de alunos do ano.
* **RNF04 (Interoperabilidade):** Comunicação automatizada via API RESTful com os serviços acadêmicos do AVA Unifor para atualização diária de matrículas e aptidão ao ENADE.
* **RNF05 (Usabilidade):** Diferenciação visual clara entre respostas da comunidade e respostas validadas por um professor administrador, além de salvamento automático (*auto-save*) de rascunhos nas questões discursivas.

---

## 5. Regras de Negócio (RN)
* **RN01 (Estrutura Padrão do Simulado):** O simulado oficial completo deve espelhar a prova do ENADE, contendo 40 questões (36 objetivas e 4 discursivas, divididas entre Formação Geral e Conhecimento Específico) com limite de 4 horas.
* **RN02 (Bloqueio Durante Simulado):** O gabarito comentado, o espelho de correção discursiva, as sugestões e a aba Tira-Dúvidas ficam bloqueados durante a realização do simulado cronometrado.
* **RN03 (Submissão por Tempo):** O simulado é encerrado e submetido automaticamente quando o cronômetro atinge zero.
* **RN04 (Autoria Oficial):** Somente professores e administradores podem publicar ou editar gabaritos comentados e espelhos de correção oficiais.
* **RN05 (Critério de Recompensa):** Para desbloquear a sincronização de Horas Complementares no AVA Unifor, o estudante deve concluir no mínimo 3 simulados cronometrados com taxa de acerto igual ou superior a 50% e revisar pelo menos 70% das pendências do seu Caderno Automático de Erros.
* **RN06 (Alerta de Retorno Prévio):** Sempre que um tópico apresentar taxa de acerto média da turma inferior a 40%, o sistema deve destacar o tema em vermelho no painel de retorno prévio dos professores e coordenadores.
* **RN07 (Dinâmica de Publicação e Revisão Periódica):** As respostas e sugestões enviadas por alunos na aba Tira-Dúvidas são publicadas imediatamente com o status *"Comunidade"*; periodicamente, o professor administrador revisa as postagens, concedendo o selo *"Verificado pelo Professor"* (que fixa a resposta no topo e concede XP extra ao autor) ou removendo conteúdos inadequados.
* **RN08 (Enquadramento Populacional Automático via AVA Unifor):** O sistema classifica automaticamente como *"Elegível ao ENADE no Ano Vigente"* os estudantes de cursos pertencentes ao ciclo trienal do MEC cujo percentual de integralização curricular no AVA Unifor atinja a faixa regulamentar do edital do INEP.
* **RN09 (Escopo de Exportação da Planilha):** Administradores exportam a planilha populacional de todos os cursos da Unifor; Coordenadores exportam a planilha completa do seu respectivo curso; Professores exportam a planilha filtrada pelos alunos matriculados em suas turmas no AVA Unifor.
* **RN10 (Ciclo de Vida no Caderno Automático de Erros):** Toda questão objetiva respondida incorretamente ingressa automaticamente no Caderno de Erros do estudante com status *"Pendente"*; a questão só muda para *"Dominada"* (saindo da fila prioritária) quando o estudante a acerta em 2 tentativas subsequentes realizadas em dias diferentes.
* **RN11 (Avaliação de Questões Discursivas):** Ao submeter uma resposta discursiva, o sistema libera imediatamente o Padrão de Resposta Oficial do INEP para autoavaliação por critérios e encaminha o texto à fila docente para atribuição de nota (0 a 100) e observações pedagógicas.

---

## 6. Backlog Priorizado
| ID | História de Usuário | Prioridade | Requisitos | Sprint |
| :--- | :--- | :---: | :---: | :---: |
| **US01** | Como usuário, quero me autenticar via Web ou Mobile usando meu login institucional do AVA Unifor. | Alta (Must) | RF01, RNF01, RNF02 | Sprint 1 |
| **US02** | Como administrador/coordenador, quero que o sistema sincronize com o AVA Unifor para mapear automaticamente a população de alunos que fará o ENADE no ano. | Alta (Must) | RF02, RNF04, RN08 | Sprint 1 |
| **US03** | Como administrador, quero cadastrar questões objetivas e discursivas por ano, curso e componente. | Alta (Must) | RF04 | Sprint 1 |
| **US04** | Como estudante, quero filtrar questões por área e ano no app ou web para praticar. | Alta (Must) | RF05, RNF03 | Sprint 1 |
| **US05** | Como professor/coordenador/admin, quero exportar uma planilha (`.xlsx`/`.csv`) com os dados dos alunos que farão o ENADE no ano e seu status de preparo. | Alta (Must) | RF03, RN08, RN09 | Sprint 2 |
| **US06** | Como estudante, quero consultar o gabarito comentado e realizar simulados cronometrados. | Alta (Must) | RF08, RF09, RN01-04 | Sprint 2 |
| **US07** | Como estudante, quero que o sistema salve automaticamente as questões que errei em um Caderno de Erros para que eu possa revisar meus pontos fracos. | Alta (Must) | RF06, RN10 | Sprint 2 |
| **US08** | Como estudante, quero praticar questões discursivas comparando minha resposta com o espelho oficial do INEP e recebendo avaliação do professor. | Alta (Must) | RF07, RF12, RN11 | Sprint 2 |
| **US09** | Como professor/coordenador, quero acessar o painel de monitoramento e retorno prévio para identificar lacunas da turma antes do ENADE. | Alta (Must) | RF14, RN06 | Sprint 2 |
| **US10** | Como estudante, quero postar sugestões de estudo e responder dúvidas de colegas na aba Tira-Dúvidas para manter o estudo dinâmico. | Média (Should) | RF10, RF11, RN07 | Sprint 3 |
| **US11** | Como professor administrador, quero revisar periodicamente as respostas da aba Tira-Dúvidas e corrigir questões discursivas dos alunos. | Média (Should) | RF12, RN07, RN11 | Sprint 3 |
| **US12** | Como estudante, quero acumular metas, revisões do Caderno de Erros e respostas validadas para contabilizar horas complementares e bonificação no AVA Unifor. | Média (Should) | RF13, RF15, RN05 | Sprint 3 |

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
        UC5("UC05 - Consultar Gabarito Comentado e Espelho INEP")
        UC6("UC06 - Revisar Questões pelo Caderno Automático de Erros")
        UC7("UC07 - Praticar e Submeter Questões Discursivas")
        UC8("UC08 - Postar Sugestões e Responder na Aba Tira-Dúvidas")
        UC9("UC09 - Revisar Tira-Dúvidas e Avaliar Discursivas Periodicamente")
        UC10("UC10 - Monitorar Retorno Prévio da Turma")
        UC11("UC11 - Contabilizar Metas e Horas Complementares")
        UC12("UC12 - Gerenciar Banco de Questões e Gabaritos")
    end

    Est --> UC1 & UC4 & UC6 & UC7 & UC8 & UC11
    UC4 -.->|"<<extend>>"| UC5
    UC4 -.->|"<<extend>>"| UC6
    UC7 -.->|"<<include>>"| UC5
    Prof --> UC1 & UC3 & UC8 & UC9 & UC10 & UC12
    UC7 -.->|"<<extend>>"| UC9
    UC8 -.->|"<<extend>>"| UC9
    Coord --> UC1 & UC2 & UC3 & UC10
    Adm --> UC1 & UC2 & UC3 & UC9 & UC12

    UC1 --> AVA
    UC2 --> AVA
    UC11 --> AVA
~~~

### 7.2. Diagrama de Componentes
~~~mermaid
flowchart TB
    subgraph Front-end Multiplataforma
        Web["[Componente] Portal Web (Estudo, Discursivas, Curadoria & Planilhas)"]
        Mob["[Componente] App Mobile (Prática, Caderno de Erros, Tira-Dúvidas & Gamificação)"]
    end
    subgraph Back-end API - Sistema ENADE
        API["[Componente] API Gateway"]
        Auth["[Componente] Autenticação SSO & Conector AVA Unifor"]
        PopCtrl["[Componente] Controle Populacional & Exportador de Planilhas (XLSX/CSV)"]
        BancoQ["[Componente] Banco de Questões Objetivas, Discursivas & Espelhos INEP"]
        Sim["[Componente] Motor de Simulados Cronometrados"]
        CadErros["[Componente] Caderno Automático de Erros & Repetição Espaçada"]
        TiraDuvidas["[Componente] Aba Tira-Dúvidas, Sugestões & Revisão Docente"]
        Monit["[Componente] Motor de Monitoramento & Retorno Prévio"]
        Gamif["[Componente] Módulo de Gamificação & Horas Complementares"]
    end
    subgraph Sistemas Externos e Persistência
        AVA_API["[Interface Externa] API AVA Unifor (Matrículas & Turmas)"]
        DB[("PostgreSQL")]
    end

    Web & Mob -->|HTTPS/REST| API
    API --> Auth & PopCtrl & BancoQ & Sim & CadErros & TiraDuvidas & Monit & Gamif
    Auth & PopCtrl & Gamif -->|REST / OAuth2| AVA_API
    Auth & PopCtrl & BancoQ & Sim & CadErros & TiraDuvidas & Monit & Gamif --> DB
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
