# 7. Diagramas UML

## 7.1. Diagrama de Casos de Uso
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
        UC4("UC04 - Resolver Desafio Rápido e Acumular XP (Gamificação)")
        UC5("UC05 - Consultar Gabarito Comentado e Espelho INEP")
        UC6("UC06 - Revisar Questões pelo Caderno Automático de Erros")
        UC7("UC07 - Praticar e Submeter Questões Discursivas")
        UC8("UC08 - Postar Sugestões e Responder na Aba Tira-Dúvidas")
        UC9("UC09 - Revisar Tira-Dúvidas e Avaliar Discursivas Periodicamente")
        UC10("UC10 - Monitorar Retorno Prévio da Turma")
        UC11("UC11 - Consultar Rankings Semanais (10 Ganhadores), Mensal Top 3 e Radar")
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

## 7.2. Diagrama de Componentes
~~~mermaid
flowchart TB
    subgraph Front-end Multiplataforma
        Web["[Componente] Portal Web (Estudo, Discursivas, Curadoria & Planilhas)"]
        Mob["[Componente] App Mobile (Microlearning, Ofensivas XP & Tira-Dúvidas)"]
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
        Gamif["[Componente] Motor de Gamificação, XP, Rankings Semanais/Mensal & Insígnias"]
    end
    subgraph Sistemas Externos e Persistência
        AVA_API["[Interface Externa] API AVA Unifor (Matrículas & Turmas)"]
        DB[("PostgreSQL")]
    end

    Web & Mob -->|HTTPS/REST| API
    API --> Auth & PopCtrl & BancoQ & Sim & CadErros & TiraDuvidas & Monit & Gamif
    Auth & PopCtrl -->|REST / OAuth2| AVA_API
    Auth & PopCtrl & BancoQ & Sim & CadErros & TiraDuvidas & Monit & Gamif --> DB
~~~

## 7.3. Diagrama de Implantação
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
