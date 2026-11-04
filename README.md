# Sistema de Apoio ao ENADE (Web & Mobile) - Unifor
**Disciplina:** Requisitos e Modelagem de Sistemas
**Sprint 1 (Milestone M1):** 19/10/2026 a 01/11/2026

---

## 1. Documento de Visão
* **Contexto:** O ENADE é componente curricular obrigatório e indicador fundamental da qualidade do ensino superior brasileiro.
* **Problemática (Visão do Estudante):** Os estudantes enfrentam dificuldades no preparo devido à falta de materiais organizados, simulados práticos, feedback imediato sobre desempenho, canais dinâmicos para tirar dúvidas entre colegas e incentivos práticos que mantenham o engajamento contínuo.
* **Problemática (Visão Docente e Coordenação):** Professores e coordenadores de curso carecem de monitoramento contínuo e de um **retorno prévio (diagnóstico antecipado)** sobre o nível de preparo das turmas. Sem dados prévios, a instituição só descobre as lacunas pedagógicas após a divulgação do resultado oficial pelo INEP, quando não há mais tempo hábil para reforço acadêmico.
* **Objetivo Geral:** Especificar uma plataforma integrada **Web e Mobile** de questões comentadas e simulados do ENADE (seguindo o padrão IEEE 830) que conecte a preparação colaborativa dos estudantes ao monitoramento pedagógico prévio e curadoria de professores e coordenadores.
* **Proposta de Valor e Incentivo aos Alunos (O que o aluno ganha?):**
  1. **Horas de Atividades Complementares:** Emissão automática de declarações de horas complementares a cada trilha de simulados concluída com aproveitamento mínimo.
  2. **Pontos Extras por Monitoria Solidária:** Alunos que respondem dúvidas de colegas na aba Tira-Dúvidas ou enviam sugestões de estudo que recebem o selo de validação do professor ganham pontuação extra no sistema de recompensas.
  3. **Bonificação Acadêmica Integrada:** Relatórios de participação exportáveis para que professores concedam pontuação bônus parcial em disciplinas correlatas aos alunos que cumprirem as metas diagnósticas.
  4. **Gamificação e Microcertificados:** Sistema de ofensivas de estudo (*streaks*), ranking opcional de colaboração e selos digitais de proficiência por área de conhecimento.
* **Escopo do Sistema:** Banco de questões (organizadas por ano, curso/área de conhecimento e componente específico), gabarito comentado, aba dinâmica de tira-dúvidas e sugestões aluno-para-aluno com revisão periódica docente, simulados cronometrados, painel de monitoramento e retorno prévio para docentes/coordenação, módulo de recompensas acadêmicas e autenticação segura.

---

## 2. Identificação de Stakeholders
| Stakeholder | Papel / Perfil | Interesse e Responsabilidade no Sistema |
| :--- | :--- | :--- |
| **Estudantes de Graduação** | Usuário Primário (App Mobile / Web) | Realizar simulados, resolver questões, publicar sugestões de estudo para colegas, perguntar e responder na aba Tira-Dúvidas e acumular pontos para horas complementares. |
| **Professores (Admin Pedagógico)** | Apoio Pedagógico e Revisor (Web/Mobile) | Receber retorno prévio sobre dificuldades da turma, validar gabaritos comentados e realizar a **revisão periódica** das respostas e sugestões dos alunos na aba Tira-Dúvidas. |
| **Coordenações de Curso** | Gestor Acadêmico (Portal Web) | Monitorar estatísticas consolidadas e diagnósticos prévios por área de conhecimento para planejar revisões e intervenções pedagógicas antes do exame oficial. |
| **Administradores do Sistema** | Gestão Técnica e Moderação | Gerenciar autenticação de usuários, moderar conteúdos sinalizados na comunidade, configurar regras de horas complementares e alimentar o banco de questões do INEP. |

---

## 3. Roteiro e Resultados de Entrevistas
### Roteiro Aplicado (Estudantes, Professores e Coordenação)
1. Quais dificuldades você encontra ao buscar provas anteriores do ENADE no portal do INEP?
2. Qual a importância de visualizar um gabarito comentado logo após responder uma questão?
3. Você acharia útil uma aba dinâmica onde os próprios colegas pudessem responder suas dúvidas e deixar sugestões de estudo, com revisão periódica de um professor?
4. Que tipo de recompensa prática (horas complementares, bônus em nota, certificados) faria você utilizar o aplicativo toda semana?
5. **(Para Professores/Coordenação):** Como um painel com retorno prévio de desempenho e curadoria periódica das dúvidas dos alunos ajudaria a corrigir falhas de aprendizado antes da prova oficial?

### Síntese dos Resultados Elicitados
* **89% dos estudantes** relataram que provas soltas em PDF dificultam o estudo, preferindo um aplicativo Mobile/Web com questões filtradas por ano, curso e componente.
* **94% dos entrevistados** apontaram o **Gabarito Comentado** como essencial para entender o conceito das respostas.
* **86% dos estudantes** destacaram que aprendem mais rápido com **dicas e sugestões de outros alunos** (linguagem acessível) e que uma aba **Tira-Dúvidas aberta à comunidade** evita esperas longas, desde que um professor revise o conteúdo periodicamente para garantir confiabilidade.
* **91% dos estudantes** afirmaram que a conversão de metas de estudo e ajuda aos colegas em **Horas Complementares** e **pequenos bônus em disciplinas** aumentaria drasticamente sua adesão.
* **Professores e Coordenadores** ressaltaram que o **monitoramento e retorno prévio**, somados à visualização das dúvidas mais frequentes na aba colaborativa, permitem identificar matérias críticas com meses de antecedência.

---

## 4. Requisitos do Sistema (Padrão IEEE 830)
### 4.1. Requisitos Funcionais (RF)
* **RF01 - Autenticação Multiperfil:** Permitir cadastro e autenticação segura de estudantes, professores, coordenadores e administradores nas plataformas Web e Mobile.
* **RF02 - Banco de Questões:** Permitir o cadastro de questões organizadas por ano, curso/área de conhecimento e componente (Formação Geral e Conhecimento Específico).
* **RF03 - Busca e Resolução Prática:** Permitir busca e filtragem de questões para resolução em computadores ou smartphones.
* **RF04 - Gabarito Comentado:** Exibir gabarito comentado com explicações detalhadas após a submissão da resposta.
* **RF05 - Simulados Cronometrados:** Gerar simulados cronometrados para prática realista do exame.
* **RF06 - Aba Tira-Dúvidas Colaborativa:** Disponibilizar uma aba de dúvidas vinculada às questões e temas gerais, onde qualquer estudante pode postar perguntas e os próprios alunos podem respondê-las imediatamente.
* **RF07 - Mural de Sugestões Aluno-para-Aluno:** Permitir que estudantes publiquem dicas de estudo, resumos estratégicos e sugestões de resolução para auxiliar outros alunos, com sistema de votos positivos (*upvotes*).
* **RF08 - Fila de Revisão Periódica (Professor/Admin):** Disponibilizar um painel de curadoria para que administradores professores revisem periodicamente as respostas e sugestões dos alunos, podendo atribuir o selo *"Validado pelo Professor"*, editar complementos ou ocultar informações incorretas.
* **RF09 - Estatísticas do Estudante:** Apresentar gráficos de desempenho individual por área de conhecimento.
* **RF10 - Monitoramento e Retorno Prévio (Docentes/Coordenação):** Disponibilizar um painel gerencial com alertas antecipados sobre os conteúdos de maior dificuldade da turma e evolução do preparo antes do exame.
* **RF11 - Gamificação e Recompensas Acadêmicas:** Contabilizar pontos de engajamento (XP por simulados e respostas validadas no Tira-Dúvidas) e emitir comprovantes automáticos para validação de Horas Complementares e bonificação docente.

### 4.2. Requisitos Não Funcionais (RNF)
* **RNF01 (Arquitetura Web e Mobile):** O sistema deve possuir aplicação Web responsiva (foco em estudo detalhado, curadoria docente e painéis de coordenação) e aplicativo Mobile (foco em resolução rápida, tira-dúvidas dinâmico e gamificação).
* **RNF02 (Segurança):** Senhas criptografadas (bcrypt), autenticação via token JWT e código de verificação antifraude nos certificados de horas complementares.
* **RNF03 (Desempenho):** Tempo de resposta inferior a 2 segundos para filtragem de questões, publicação no Tira-Dúvidas e atualização dos relatórios de retorno prévio.
* **RNF04 (Usabilidade):** Diferenciação visual clara entre respostas em aberto da comunidade e respostas já revisadas/chanceladas por um professor administrador.

---

## 5. Regras de Negócio (RN)
* **RN01:** O simulado padrão deve conter 40 questões (10 de Formação Geral e 30 de Conhecimento Específico) com limite de 4 horas.
* **RN02:** O gabarito comentado, as sugestões e a aba Tira-Dúvidas ficam bloqueados durante a realização do simulado cronometrado.
* **RN03:** O simulado é encerrado e submetido automaticamente quando o cronômetro atinge zero.
* **RN04:** Somente professores e administradores podem publicar ou editar gabaritos comentados oficiais.
* **RN05 (Critério de Recompensa por Simulado):** Para desbloquear o certificado base de Horas Complementares, o estudante deve concluir no mínimo 3 simulados cronometrados com taxa de acerto igual ou superior a 50%.
* **RN06 (Alerta de Retorno Prévio):** Sempre que um tópico apresentar taxa de acerto média da turma inferior a 40%, o sistema deve destacar o tema em vermelho no painel de retorno prévio dos professores e coordenadores.
* **RN07 (Dinâmica de Publicação e Revisão Periódica):** As respostas e sugestões enviadas por alunos na aba Tira-Dúvidas são publicadas imediatamente com o status *"Comunidade"* para garantir dinamismo; periodicamente, o professor administrador revisa as postagens mais acessadas, concedendo o selo *"Verificado pelo Professor"* (que fixa a resposta no topo) ou removendo conteúdos inadequados.
* **RN08 (Bonificação por Colaboração):** Cada resposta ou sugestão de aluno que receber o selo *"Verificado pelo Professor"* concede pontos extras de engajamento que aceleram a conquista de Horas Complementares.

---

## 6. Backlog Priorizado
| ID | História de Usuário | Prioridade | Requisitos | Sprint |
| :--- | :--- | :---: | :---: | :---: |
| **US01** | Como usuário, quero me cadastrar e autenticar via Web ou Mobile. | Alta (Must) | RF01, RNF01, RNF02 | Sprint 1 |
| **US02** | Como administrador, quero cadastrar questões por ano, curso e componente. | Alta (Must) | RF02 | Sprint 1 |
| **US03** | Como estudante, quero filtrar questões por área e ano no app ou web para praticar. | Alta (Must) | RF03, RNF03 | Sprint 1 |
| **US04** | Como estudante, quero consultar o gabarito comentado após responder. | Alta (Must) | RF04, RN04 | Sprint 2 |
| **US05** | Como estudante, quero realizar simulados cronometrados. | Alta (Must) | RF05, RN01-03 | Sprint 2 |
| **US06** | Como professor/coordenador, quero acessar o painel de monitoramento e retorno prévio para identificar lacunas da turma antes do ENADE. | Alta (Must) | RF10, RN06 | Sprint 2 |
| **US07** | Como estudante, quero postar sugestões de estudo e responder dúvidas de colegas na aba Tira-Dúvidas para manter o estudo colaborativo e dinâmico. | Média (Should) | RF06, RF07, RN07 | Sprint 2 |
| **US08** | Como professor administrador, quero revisar periodicamente as respostas e sugestões dos alunos para validar conteúdos corretos e manter a qualidade acadêmica. | Média (Should) | RF08, RN07, RNF04 | Sprint 2 |
| **US09** | Como estudante, quero acumular metas e respostas validadas para gerar comprovantes de horas complementares e bonificação. | Média (Should) | RF11, RN05, RN08 | Sprint 3 |
| **US10** | Como estudante, quero visualizar gráficos do meu desempenho individual. | Média (Should) | RF09 | Sprint 3 |

---

## 7. Diagramas UML

### 7.1. Diagrama de Casos de Uso
~~~mermaid
flowchart LR
    Est(["👤 Estudante"])
    Prof(["👨‍🏫 Professor (Admin Revisor)"])
    Coord(["📊 Coordenador"])
    Adm(["🛠️ Administrador Técnico"])

    subgraph Sistema de Apoio ao ENADE - Web e Mobile
        UC1("UC01 - Autenticar Usuário (Web/Mobile)")
        UC2("UC02 - Filtrar e Resolver Questões")
        UC3("UC03 - Consultar Gabarito Comentado")
        UC4("UC04 - Realizar Simulado Cronometrado")
        UC5("UC05 - Postar Sugestões e Responder na Aba Tira-Dúvidas")
        UC6("UC06 - Revisar e Validar Dúvidas/Sugestões Periodicamente")
        UC7("UC07 - Acompanhar Metas e Emitir Horas Complementares")
        UC8("UC08 - Monitorar Retorno Prévio da Turma")
        UC9("UC09 - Gerenciar Questões e Gabaritos")
    end

    Est --> UC1 & UC2 & UC4 & UC5 & UC7
    UC2 -.->|"<<extend>>"| UC3
    Prof --> UC1 & UC5 & UC6 & UC8 & UC9
    UC5 -.->|"<<extend>>"| UC6
    Coord --> UC1 & UC8
    Adm --> UC1 & UC6 & UC9
~~~

### 7.2. Diagrama de Componentes
~~~mermaid
flowchart TB
    subgraph Front-end Multiplataforma
        Web["[Componente] Portal Web (Estudo, Curadoria & Gestão Docente)"]
        Mob["[Componente] App Mobile (Prática, Tira-Dúvidas & Gamificação)"]
    end
    subgraph Back-end API
        API["[Componente] API Gateway"]
        Auth["[Componente] Autenticação"]
        BancoQ["[Componente] Banco de Questões & Gabaritos"]
        Sim["[Componente] Simulados Cronometrados"]
        TiraDuvidas["[Componente] Aba Tira-Dúvidas, Sugestões & Revisão Docente"]
        Monit["[Componente] Motor de Monitoramento & Retorno Prévio"]
        Gamif["[Componente] Módulo de Gamificação & Horas Complementares"]
    end
    subgraph Persistência
        DB[("PostgreSQL")]
    end

    Web & Mob -->|HTTPS/REST| API
    API --> Auth & BancoQ & Sim & TiraDuvidas & Monit & Gamif
    Auth & BancoQ & Sim & TiraDuvidas & Monit & Gamif --> DB
~~~

### 7.3. Diagrama de Implantação
~~~mermaid
flowchart LR
    subgraph Cliente ["«device» Dispositivos dos Usuários"]
        Nav["«executionEnvironment» Navegador Web (PC/Notebook)"]
        App["«executionEnvironment» App Mobile (Android/iOS)"]
    end
    subgraph Nuvem ["«node» Servidor de Aplicação Cloud"]
        Container["«executionEnvironment» Container Docker (API ENADE)"]
    end
    subgraph BaseDados ["«node» Servidor de Banco de Dados"]
        PG["«executionEnvironment» PostgreSQL Server"]
    end

    Nav -- "HTTPS (443)" --> Container
    App -- "HTTPS (443)" --> Container
    Container -- "TCP/IP (5432)" --> PG
~~~
