# Sistema de Apoio ao ENADE (Web & Mobile) - Unifor
**Disciplina:** Requisitos e Modelagem de Sistemas
**Sprint 1 (Milestone M1):** 19/10/2026 a 01/11/2026

---

## 1. Documento de Visão
* **Contexto:** O ENADE é componente curricular obrigatório e indicador fundamental da qualidade do ensino superior brasileiro.
* **Problemática (Visão do Estudante):** Os estudantes enfrentam dificuldades no preparo devido à falta de materiais organizados, ausência de treino focado em questões discursivas, falta de rastreamento automático dos próprios erros para revisão direcionada, escassez de canais dinâmicos para tirar dúvidas entre colegas e formatos de estudo cansativos que desestimulam o hábito diário.
* **Problemática (Visão Docente, Coordenação e Controle Populacional):** Professores, coordenadores e administradores enfrentam dificuldades para mapear e controlar com precisão o universo de alunos aptos ao ENADE no ano vigente, além de carecerem de monitoramento contínuo e de um **retorno prévio (diagnóstico antecipado)** sobre o nível de preparo objetivo e discursivo das turmas antes do exame oficial.
* **Objetivo Geral:** Especificar uma plataforma integrada **Web e Mobile** de questões comentadas (objetivas e discursivas) e simulados do ENADE (seguindo o padrão IEEE 830), integrada diretamente ao **AVA Unifor** para controle populacional automático, geração de planilhas gerenciais de alunos do ano e monitoramento pedagógico prévio.
* **Estratégia de Atração e Engajamento dos Alunos (Como despertar o interesse real sem bonificações externas?):**
  1. **Microlearning de Bolso (Desafios Rápidos de 3 Minutos):** Em vez de exigir horas seguidas de estudo em PDFs estáticos, o app mobile oferece pílulas diárias de 1 a 3 questões rápidas com feedback instantâneo para o aluno resolver no intervalo entre aulas.
  2. **Estudo "Dois em Um" (Conexão com as Disciplinas e Mercado):** As trilhas de questões são alinhadas pelos professores aos conteúdos cobrados nas avaliações regulares do semestre e em processos seletivos/concursos da área, fazendo com que o aluno estude para as provas da faculdade e para o ENADE ao mesmo tempo.
  3. **Radar de Competências Profissionais:** Os gráficos de desempenho são traduzidos em um mapa visual de domínio técnico por área da profissão, ajudando o aluno a identificar seus pontos fortes para entrevistas de estágio e trabalho.
  4. **Gamificação de Hábito e Reconhecimento ("Aluno Mentor"):** Sistema de ofensivas diárias (*streaks* de estudo contínuo) e destaque no perfil da comunidade para os estudantes cujas dicas e respostas na aba Tira-Dúvidas recebem o selo *"Validado pelo Professor"*.
* **Escopo do Sistema:** Integração com o AVA Unifor (login institucional SSO e importação da base de alunos elegíveis no ano), exportação de planilhas/dados nominais para professores e administradores, banco de questões objetivas e **treino de questões discursivas** (com espelho de correção do INEP), **caderno automático de erros** para revisão personalizada, gabarito comentado, aba dinâmica de tira-dúvidas e sugestões aluno-para-aluno com revisão periódica docente, simulados cronometrados, painel de retorno prévio e gamificação de hábito de estudo.

---

## 2. Identificação de Stakeholders
| Stakeholder | Papel / Perfil | Interesse e Responsabilidade no Sistema |
| :--- | :--- | :--- |
| **Estudantes de Graduação** | Usuário Primário (App Mobile / Web) | Acessar via AVA Unifor, realizar desafios rápidos e simulados, treinar questões discursivas, revisar pendências no Caderno Automático de Erros, acompanhar seu Radar de Competências e interagir na aba Tira-Dúvidas. |
| **Professores (Admin Pedagógico)** | Apoio Pedagógico e Revisor (Web/Mobile) | Receber retorno prévio sobre dificuldades da turma, alinhar listas aos conteúdos de sala de aula, exportar planilhas dos alunos aptos ao ENADE, avaliar discursivas e revisar periodicamente a aba Tira-Dúvidas. |
| **Coordenações de Curso** | Gestor Acadêmico (Portal Web) | Controlar a população de estudantes enquadrados no ENADE daquele ano, exportar planilhas gerenciais completas e planejar intervenções pedagógicas prévias. |
| **Administradores do Sistema** | Gestão Técnica e Operacional | Gerenciar a sincronização com o AVA Unifor, extrair relatórios/planilhas globais de alunos elegíveis, moderar a comunidade e alimentar o banco de questões e espelhos do INEP. |
| **AVA Unifor (Sistema Acadêmico)** | Sistema Externo Integrado | Fornecer autenticação institucional (SSO) e dados de matrícula, curso, turmas e percentual de integralização curricular. |

---

## 3. Roteiro e Resultados de Entrevistas
### Roteiro Aplicado (Estudantes, Professores e Coordenação)
1. Quais dificuldades você encontra ao buscar provas anteriores do ENADE no portal do INEP?
2. Qual a importância de visualizar um gabarito comentado e ter um **Caderno Automático de Erros** que separe tudo o que você errou para revisar em poucos minutos pelo celular?
3. Como você se prepara hoje para as **questões discursivas** do ENADE e qual o valor de ter o espelho de correção do INEP junto à revisão de um professor?
4. Você acharia útil uma aba dinâmica onde os próprios colegas pudessem responder suas dúvidas e deixar sugestões de estudo, com revisão periódica docente?
5. O que tornaria o aplicativo interessante para uso voluntário no dia a dia: desafios rápidos de 3 minutos no celular, alinhamento com os assuntos das provas da faculdade ou um mapa das suas competências profissionais?
6. **(Para Professores/Coordenação/Admin):** Qual o impacto de ter o sistema integrado ao AVA Unifor gerando automaticamente uma planilha pronta com todos os alunos que farão o ENADE naquele ano e o respectivo status de preparo?

### Síntese dos Resultados Elicitados
* **89% dos estudantes** relataram que provas soltas em PDF dificultam o estudo, preferindo um aplicativo Mobile/Web integrado ao login do AVA Unifor com questões rápidas filtradas por ano, curso e componente.
* **94% dos entrevistados** apontaram o **Gabarito Comentado** e o **Caderno Automático de Erros** como essenciais para otimizar o tempo e focar apenas no que ainda não dominam.
* **82% dos estudantes** afirmaram nunca treinar para as **questões discursivas** por falta de parâmetros claros de correção, validando o módulo discursivo com espelho oficial do INEP e feedback docente.
* **86% dos estudantes** destacaram que aprendem mais rápido com **dicas e sugestões de outros alunos** e uma aba **Tira-Dúvidas aberta à comunidade**, desde que revisada periodicamente por um professor.
* **88% dos estudantes** afirmaram que usariam a plataforma espontaneamente se ela funcionasse em formato de **estudo rápido diário (Microlearning)** e ajudasse diretamente a revisar conteúdos para as **provas regulares das disciplinas e processos seletivos**.
* **100% dos Coordenadores e Professores** apontaram que a **integração com o AVA Unifor** para controle populacional e a **exportação de planilhas (`.xlsx`/`.csv`) dos alunos que farão o ENADE no ano** permitem acompanhar de perto a evolução real da turma antes do exame.

---

## 4. Requisitos do Sistema (Padrão IEEE 830)
### 4.1. Requisitos Funcionais (RF)
* **RF01 - Autenticação Integrada (SSO AVA Unifor):** Permitir login unificado utilizando as credenciais institucionais do AVA Unifor para estudantes, professores, coordenadores e administradores nas plataformas Web e Mobile.
* **RF02 - Sincronização e Controle Populacional via AVA:** Importar e sincronizar automaticamente via API do AVA Unifor a relação de estudantes matriculados, identificando o grupo populacional que realizará o ENADE no ano vigente.
* **RF03 - Exportação de Planilhas de Alunos do ENADE do Ano:** Permitir que professores, coordenadores e administradores exportem planilhas estruturadas (`.xlsx` e `.csv`) contendo a lista nominal dos alunos que farão o ENADE naquele ano, matrícula, turma, simulados realizados, média de acertos (objetivas e discursivas) e alerta de inatividade.
* **RF04 - Banco de Questões Objetivas e Discursivas:** Permitir o cadastro de questões objetivas e discursivas organizadas por ano, curso/área de conhecimento, disciplina correlata e componente (Formação Geral e Conhecimento Específico).
* **RF05 - Busca, Resolução Prática e Desafio Rápido Diário:** Permitir busca personalizada de questões e disponibilizar o modo *"Desafio Rápido do Dia"* (3 questões selecionadas no app mobile para resolução em até 5 minutos).
* **RF06 - Caderno Automático de Erros:** Compilar automaticamente todas as questões que o estudante errou em simulados ou listas avulsas em um caderno inteligente de revisão focada.
* **RF07 - Treino de Questões Discursivas:** Disponibilizar ambiente para redação de respostas discursivas com contagem de linhas/caracteres, exibição do Padrão de Resposta Oficial do INEP (espelho de correção) após o envio e encaminhamento opcional para avaliação de um professor.
* **RF08 - Gabarito Comentado:** Exibir gabarito comentado detalhado após a submissão da resposta objetiva.
* **RF09 - Simulados Cronometrados:** Gerar simulados cronometrados (incluindo questões objetivas e discursivas) para prática realista do exame.
* **RF10 - Aba Tira-Dúvidas Colaborativa:** Disponibilizar uma aba de dúvidas vinculada às questões e temas gerais, onde qualquer estudante pode postar perguntas e os próprios alunos podem respondê-las imediatamente.
* **RF11 - Mural de Sugestões Aluno-para-Aluno:** Permitir que estudantes publiquem dicas de estudo, macetes e resumos estratégicos para auxiliar outros alunos, com sistema de votos positivos (*upvotes*).
* **RF12 - Fila de Revisão Periódica e Correção Discursiva (Professor/Admin):** Disponibilizar um painel de curadoria para que administradores professores revisem periodicamente as respostas/sugestões da aba Tira-Dúvidas (atribuindo o selo *"Validado pelo Professor"*) e avaliem respostas discursivas submetidas pelos alunos.
* **RF13 - Estatísticas e Radar de Competências do Estudante:** Apresentar gráficos de desempenho individual por área de conhecimento, taxa de superação do Caderno de Erros e diagnóstico visual das competências profissionais mais fortes do aluno.
* **RF14 - Monitoramento e Retorno Prévio (Docentes/Coordenação):** Disponibilizar um painel gerencial com alertas antecipados sobre os conteúdos de maior dificuldade da população de alunos do ENADE do ano vigente.
* **RF15 - Gamificação de Hábito e Reconhecimento Comunitário:** Contabilizar ofensivas de estudo diário (*streaks*), conquistas de domínio do Caderno de Erros e insígnias de *"Aluno Mentor"* no perfil para estudantes com respostas validadas por professores.

### 4.2. Requisitos Não Funcionais (RNF)
* **RNF01 (Arquitetura Web e Mobile):** Aplicação Web responsiva (foco em simulados completos, redação discursiva, curadoria docente e exportação de planilhas) e aplicativo Mobile (foco em microlearning diário, revisão do Caderno de Erros e tira-dúvidas dinâmico).
* **RNF02 (Segurança e Conformidade LGPD):** Senhas/tokens autenticados via OAuth2/JWT com o AVA Unifor e controle de acesso restrito na exportação de planilhas nominais de alunos, em conformidade com a LGPD.
* **RNF03 (Desempenho):** Tempo de resposta inferior a 2 segundos para filtragem de questões e atualização do Caderno de Erros, e inferior a 5 segundos para geração da planilha consolidada de alunos do ano.
* **RNF04 (Interoperabilidade):** Comunicação automatizada via API RESTful com os serviços acadêmicos do AVA Unifor para atualização diária de matrículas e aptidão ao ENADE.
* **RNF05 (Usabilidade):** Interface limpa com diferenciação visual clara entre respostas da comunidade e respostas validadas por um professor administrador, além de salvamento automático (*auto-save*) nas questões discursivas.

---

## 5. Regras de Negócio (RN)
* **RN01 (Estrutura Padrão do Simulado):** O simulado oficial completo deve espelhar a prova do ENADE, contendo 40 questões (36 objetivas e 4 discursivas, divididas entre Formação Geral e Conhecimento Específico) com limite de 4 horas.
* **RN02 (Bloqueio Durante Simulado):** O gabarito comentado, o espelho de correção discursiva, as sugestões e a aba Tira-Dúvidas ficam bloqueados durante a realização do simulado cronometrado.
* **RN03 (Submissão por Tempo):** O simulado é encerrado e submetido automaticamente quando o cronômetro atinge zero.
* **RN04 (Autoria Oficial):** Somente professores e administradores podem publicar ou editar gabaritos comentados e espelhos de correção oficiais.
* **RN05 (Manutenção de Ofensiva e Selo de Aluno Mentor):** A ofensiva diária (*streak*) é contabilizada quando o aluno conclui o *"Desafio Rápido do Dia"* ou revisa itens do Caderno de Erros; o selo de perfil *"Aluno Mentor"* é concedido automaticamente ao estudante que atingir 5 respostas ou sugestões de estudo chanceladas com o selo *"Verificado pelo Professor"*.
* **RN06 (Alerta de Retorno Prévio):** Sempre que um tópico apresentar taxa de acerto média da turma inferior a 40%, o sistema deve destacar o tema em vermelho no painel de retorno prévio dos professores e coordenadores.
* **RN07 (Dinâmica de Publicação e Revisão Periódica):** As respostas e sugestões enviadas por alunos na aba Tira-Dúvidas são publicadas imediatamente com o status *"Comunidade"*; periodicamente, o professor administrador revisa as postagens, concedendo o selo *"Verificado pelo Professor"* (que fixa a resposta no topo) ou removendo conteúdos inadequados.
* **RN08 (Enquadramento Populacional Automático via AVA Unifor):** O sistema classifica automaticamente como *"Elegível ao ENADE no Ano Vigente"* os estudantes de cursos pertencentes ao ciclo trienal do MEC cujo percentual de integralização curricular no AVA Unifor atinja a faixa regulamentar do edital do INEP.
* **RN09 (Escopo de Exportação da Planilha):** Administradores exportam a planilha populacional de todos os cursos da Unifor; Coordenadores exportam a planilha completa do seu respectivo curso; Professores exportam a planilha filtrada pelos alunos matriculados em suas turmas no AVA Unifor.
* **RN10 (Ciclo de Vida no Caderno Automático de Erros):** Toda questão objetiva respondida incorretamente ingressa automaticamente no Caderno de Erros do estudante com status *"Pendente"*; a questão só muda para *"Dominada"* (saindo da fila prioritária) quando o estudante a acerta em 2 tentativas subsequentes realizadas em dias diferentes.
* **RN11 (Avaliação de Questões Discursivas):** Ao submeter uma resposta discursiva, o sistema libera imediatamente o Padrão de Resposta Oficial do INEP para autoavaliação por critérios e encaminha o texto à fila docente para atribuição de nota diagnóstica (0 a 100) e observações pedagógicas.

---

## 6. Backlog Priorizado
| ID | História de Usuário | Prioridade | Requisitos | Sprint |
| :--- | :--- | :---: | :---: | :---: |
| **US01** | Como usuário, quero me autenticar via Web ou Mobile usando meu login institucional do AVA Unifor. | Alta (Must) | RF01, RNF01, RNF02 | Sprint 1 |
| **US02** | Como administrador/coordenador, quero que o sistema sincronize com o AVA Unifor para mapear automaticamente a população de alunos que fará o ENADE no ano. | Alta (Must) | RF02, RNF04, RN08 | Sprint 1 |
| **US03** | Como administrador, quero cadastrar questões objetivas e discursivas por ano, curso, disciplina e componente. | Alta (Must) | RF04 | Sprint 1 |
| **US04** | Como estudante, quero filtrar questões por área/disciplina e resolver desafios rápidos diários no celular para estudar sem sobrecarga. | Alta (Must) | RF05, RNF03 | Sprint 1 |
| **US05** | Como professor/coordenador/admin, quero exportar uma planilha (`.xlsx`/`.csv`) com os dados dos alunos que farão o ENADE no ano e seu status de preparo. | Alta (Must) | RF03, RN08, RN09 | Sprint 2 |
| **US06** | Como estudante, quero consultar o gabarito comentado e realizar simulados cronometrados. | Alta (Must) | RF08, RF09, RN01-04 | Sprint 2 |
| **US07** | Como estudante, quero que o sistema salve automaticamente as questões que errei em um Caderno de Erros para revisar apenas meus pontos fracos. | Alta (Must) | RF06, RN10 | Sprint 2 |
| **US08** | Como estudante, quero praticar questões discursivas comparando minha resposta com o espelho oficial do INEP e recebendo avaliação do professor. | Alta (Must) | RF07, RF12, RN11 | Sprint 2 |
| **US09** | Como professor/coordenador, quero acessar o painel de monitoramento e retorno prévio para identificar lacunas da turma antes do ENADE. | Alta (Must) | RF14, RN06 | Sprint 2 |
| **US10** | Como estudante, quero postar sugestões de estudo e responder dúvidas de colegas na aba Tira-Dúvidas para manter o estudo dinâmico. | Média (Should) | RF10, RF11, RN07 | Sprint 3 |
| **US11** | Como professor administrador, quero revisar periodicamente as respostas da aba Tira-Dúvidas e corrigir questões discursivas dos alunos. | Média (Should) | RF12, RN07, RN11 | Sprint 3 |
| **US12** | Como estudante, quero visualizar meu Radar de Competências Profissionais, manter minha ofensiva diária e conquistar o selo de Aluno Mentor na comunidade. | Média (Should) | RF13, RF15, RN05 | Sprint 3 |

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
        UC4("UC04 - Resolver Desafio Rápido e Simulado Cronometrado")
        UC5("UC05 - Consultar Gabarito Comentado e Espelho INEP")
        UC6("UC06 - Revisar Questões pelo Caderno Automático de Erros")
        UC7("UC07 - Praticar e Submeter Questões Discursivas")
        UC8("UC08 - Postar Sugestões e Responder na Aba Tira-Dúvidas")
        UC9("UC09 - Revisar Tira-Dúvidas e Avaliar Discursivas Periodicamente")
        UC10("UC10 - Monitorar Retorno Prévio da Turma")
        UC11("UC11 - Visualizar Radar de Competências e Ofensivas de Estudo")
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
~~~

### 7.2. Diagrama de Componentes
~~~mermaid
flowchart TB
    subgraph Front-end Multiplataforma
        Web["[Componente] Portal Web (Estudo, Discursivas, Curadoria & Planilhas)"]
        Mob["[Componente] App Mobile (Desafio Rápido, Caderno de Erros & Tira-Dúvidas)"]
    end
    subgraph Back-end API - Sistema ENADE
        API["[Componente] API Gateway"]
        Auth["[Componente] Autenticação SSO & Conector AVA Unifor"]
        PopCtrl["[Componente] Controle Populacional & Exportador de Planilhas (XLSX/CSV)"]
        BancoQ["[Componente] Banco de Questões Objetivas, Discursivas & Espelhos INEP"]
        Sim["[Componente] Motor de Simulados & Desafios Rápidos"]
        CadErros["[Componente] Caderno Automático de Erros & Repetição Espaçada"]
        TiraDuvidas["[Componente] Aba Tira-Dúvidas, Sugestões & Revisão Docente"]
        Monit["[Componente] Motor de Monitoramento & Retorno Prévio"]
        Engaj["[Componente] Radar de Competências, Ofensivas & Selo Aluno Mentor"]
    end
    subgraph Sistemas Externos e Persistência
        AVA_API["[Interface Externa] API AVA Unifor (Matrículas & Turmas)"]
        DB[("PostgreSQL")]
    end

    Web & Mob -->|HTTPS/REST| API
    API --> Auth & PopCtrl & BancoQ & Sim & CadErros & TiraDuvidas & Monit & Engaj
    Auth & PopCtrl -->|REST / OAuth2| AVA_API
    Auth & PopCtrl & BancoQ & Sim & CadErros & TiraDuvidas & Monit & Engaj --> DB
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
