# Sistema de Apoio ao ENADE - Unifor
**Disciplina:** Requisitos e Modelagem de Sistemas
**Sprint 1 (Milestone M1):** 19/10/2026 a 01/11/2026

---

## 1. Documento de Visão
* **Contexto:** O ENADE é componente curricular obrigatório e indicador fundamental da qualidade do ensino superior brasileiro.
* **Problema:** Estudantes enfrentam dificuldades no preparo devido à falta de materiais organizados, simulados práticos e feedback sobre desempenho.
* **Objetivo Geral:** Aplicar engenharia de requisitos para especificar um sistema web/mobile de questões comentadas do ENADE seguindo os padrões IEEE 830.
* **Escopo do Sistema:** Banco de questões (organizadas por ano, curso/área de conhecimento e componente específico), gabarito comentado, fórum de discussão, simulados cronometrados, estatísticas de desempenho e autenticação segura.

---

## 2. Identificação de Stakeholders
| Stakeholder | Papel / Perfil | Interesse e Responsabilidade no Sistema |
| :--- | :--- | :--- |
| **Estudantes de Graduação** | Utilizador Primário | Realizar simulados cronometrados, resolver questões, consultar gabaritos comentados, interagir no fórum e acompanhar estatísticas. |
| **Professores** | Apoio Pedagógico | Validar gabaritos comentados e apoiar estudantes nos tópicos críticos. |
| **Coordenações de Curso** | Gestor Académico | Acompanhar estatísticas consolidadas de desempenho por área de conhecimento. |
| **Administradores do Sistema** | Gestão Técnica | Gerir autenticação de utilizadores e registar questões do portal INEP. |

---

## 3. Roteiro e Resultados de Entrevistas
### Roteiro Aplicado (Estudantes e Coordenação)
1. Quais dificuldades encontra ao procurar provas anteriores do ENADE no portal do INEP?
2. Qual a importância de visualizar um gabarito comentado logo após errar uma questão?
3. Utilizaria simulados cronometrados e um fórum de discussão por questão para estudar?
4. Como os gráficos de desempenho por área de conhecimento auxiliam a coordenação do curso?

### Síntese dos Resultados Elicitados
* **89% dos estudantes** relataram que provas soltas em PDF dificultam o estudo, validando o banco de questões filtrado por ano, curso e componente.
* **94% dos entrevistados** apontaram o **Gabarito Comentado** como essencial para compreender o conceito das respostas.
* **78% dos estudantes** têm dificuldade com o tempo de prova, confirmando a necessidade de **Simulados Cronometrados**.
* **Coordenações** destacaram a importância de separar os indicadores entre Formação Geral e Conhecimento Específico.

---

## 4. Requisitos do Sistema (Padrão IEEE 830)
### 4.1. Requisitos Funcionais (RF)
* **RF01:** Permitir registo e autenticação segura de estudantes, professores, coordenadores e administradores.
* **RF02:** Permitir o registo de questões organizadas por ano, curso/área de conhecimento e componente (Formação Geral e Conhecimento Específico).
* **RF03:** Permitir pesquisa e filtragem de questões para resolução prática.
* **RF04:** Exibir gabarito comentado com explicações detalhadas após a resposta da questão.
* **RF05:** Gerar simulados cronometrados para prática realista do exame.
* **RF06:** Disponibilizar fórum de discussão em cada questão para interação entre utilizadores.
* **RF07:** Apresentar estatísticas de desempenho por área de conhecimento com visualizações gráficas.

### 4.2. Requisitos Não Funcionais (RNF)
* **RNF01 (Multiplataforma):** Interface web e mobile responsiva.
* **RNF02 (Segurança):** Palavras-passe encriptadas (bcrypt) e autenticação via token JWT.
* **RNF03 (Desempenho):** Tempo de resposta inferior a 2 segundos para filtragem de questões e carregamento de gráficos.
* **RNF04 (Usabilidade):** Exibição clara do cronómetro regressivo durante os simulados.

---

## 5. Regras de Negócio (RN)
* **RN01:** O simulado padrão deve conter 40 questões (10 de Formação Geral e 30 de Conhecimento Específico) com limite de 4 horas.
* **RN02:** O gabarito comentado e o fórum ficam bloqueados durante a realização do simulado cronometrado.
* **RN03:** O simulado é encerrado e submetido automaticamente quando o cronómetro atinge zero.
* **RN04:** Somente professores e administradores podem publicar ou editar gabaritos comentados oficiais.

---

## 6. Backlog Priorizado
| ID | História de Utilizador | Prioridade | Requisitos | Sprint |
| :--- | :--- | :---: | :---: | :---: |
| **US01** | Como utilizador, quero registar-me e autenticar-me com segurança no sistema. | Alta (Must) | RF01, RNF02 | Sprint 1 |
| **US02** | Como administrador, quero registar questões por ano, curso e componente. | Alta (Must) | RF02 | Sprint 1 |
| **US03** | Como estudante, quero filtrar questões por área e ano para praticar. | Alta (Must) | RF03, RNF03 | Sprint 1 |
| **US04** | Como estudante, quero consultar o gabarito comentado após responder. | Alta (Must) | RF04, RN04 | Sprint 2 |
| **US05** | Como estudante, quero realizar simulados cronometrados. | Alta (Must) | RF05, RN01-03 | Sprint 2 |
| **US06** | Como estudante/coordenador, quero visualizar gráficos de desempenho. | Média (Should) | RF07 | Sprint 2 |
| **US07** | Como estudante, quero interagir no fórum de discussão da questão. | Baixa (Could) | RF06 | Sprint 3 |

---

## 7. Diagramas UML

### 7.1. Diagrama de Casos de Uso
~~~mermaid
flowchart LR
    Est(["👤 Estudante"])
    Prof(["👨‍🏫 Professor"])
    Coord(["📊 Coordenador"])
    Adm(["🛠️ Administrador"])

    subgraph Sistema de Apoio ao ENADE
        UC1("UC01 - Autenticar Utilizador")
        UC2("UC02 - Filtrar e Resolver Questões")
        UC3("UC03 - Consultar Gabarito Comentado")
        UC4("UC04 - Realizar Simulado Cronometrado")
        UC5("UC05 - Interagir no Fórum de Discussão")
        UC6("UC06 - Visualizar Estatísticas de Desempenho")
        UC7("UC07 - Gerir Questões e Gabaritos")
    end

    Est --> UC1 & UC2 & UC4 & UC5 & UC6
    UC2 -.->|"<<extend>>"| UC3
    Prof --> UC1 & UC5 & UC7
    Coord --> UC1 & UC6
    Adm --> UC1 & UC7
~~~

### 7.2. Diagrama de Componentes
~~~mermaid
flowchart TB
    subgraph Front-end
        Web["[Componente] Aplicação Web"]
        Mob["[Componente] Aplicação Mobile"]
    end
    subgraph Back-end API
        API["[Componente] API Gateway"]
        Auth["[Componente] Autenticação"]
        BancoQ["[Componente] Banco de Questões & Gabaritos"]
        Sim["[Componente] Simulados Cronometrados"]
        Forum["[Componente] Fórum de Discussão"]
        Estats["[Componente] Estatísticas de Desempenho"]
    end
    subgraph Persistência
        DB[("PostgreSQL")]
    end

    Web & Mob -->|HTTPS/REST| API
    API --> Auth & BancoQ & Sim & Forum & Estats
    Auth & BancoQ & Sim & Forum & Estats --> DB
~~~

### 7.3. Diagrama de Implantação
~~~mermaid
flowchart LR
    subgraph Cliente ["«device» Dispositivo do Utilizador"]
        Nav["«executionEnvironment» Browser Web / App Mobile"]
    end
    subgraph Nuvem ["«node» Servidor de Aplicação Cloud"]
        Container["«executionEnvironment» Contentor Docker (API ENADE)"]
    end
    subgraph BaseDados ["«node» Servidor de Base de Dados"]
        PG["«executionEnvironment» PostgreSQL Server"]
    end

    Nav -- "HTTPS (443)" --> Container
    Container -- "TCP/IP (5432)" --> PG
~~~
