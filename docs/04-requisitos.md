# 4. Requisitos do Sistema (Padrão IEEE 830)

## 4.1. Requisitos Funcionais (RF)
* **RF01 - Autenticação Integrada (SSO AVA Unifor):** Permitir login unificado utilizando as credenciais institucionais do AVA Unifor para estudantes, professores, coordenadores e administradores nas plataformas Web e Mobile.
* **RF02 - Sincronização e Controle Populacional via AVA:** Importar e sincronizar automaticamente via API do AVA Unifor a relação de estudantes matriculados, identificando o grupo populacional que realizará o ENADE no ano vigente.
* **RF03 - Exportação de Planilhas de Alunos do ENADE do Ano:** Permitir que professores, coordenadores e administradores exportem planilhas estruturadas (`.xlsx` e `.csv`) contendo a lista nominal dos alunos que farão o ENADE naquele ano, matrícula, turma, simulados realizados, média de acertos e alerta de inatividade.
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
* **RF15 - Módulo de Gamificação, XP, Ofensivas e Rankings:** Contabilizar pontos de experiência (XP) por atividades concluídas, manter o controle de ofensivas de estudo diário, atribuir insígnias de perfil (como o selo de *"Aluno Mentor"*) e calcular as classificações dos 4 rankings semanais de R$ 500,00 (10 ganhadores cada) e do ranking mensal de R$ 500,00 (restrito ao Top 3).

## 4.2. Requisitos Não Funcionais (RNF)
* **RNF01 (Arquitetura Web e Mobile):** Aplicação Web responsiva (foco em simulados completos, redação discursiva, curadoria docente e exportação de planilhas) e aplicativo Mobile (foco em microlearning diário, ofensivas de estudo, Caderno de Erros e tira-dúvidas dinâmico).
* **RNF02 (Segurança e Conformidade LGPD):** Senhas/tokens autenticados via OAuth2/JWT com o AVA Unifor e controle de acesso restrito na exportação de planilhas nominais de alunos, em conformidade com a LGPD.
* **RNF03 (Desempenho):** Tempo de resposta inferior a 2 segundos para filtragem de questões, atualização do Caderno de Erros e pontuação de XP, e inferior a 5 segundos para geração da planilha consolidada de alunos do ano.
* **RNF04 (Interoperabilidade):** Comunicação automatizada via API RESTful com os serviços acadêmicos do AVA Unifor para atualização diária de matrículas e aptidão ao ENADE.
* **RNF05 (Usabilidade):** Interface limpa com elementos visuais de gamificação (barras de progresso de XP, distintivos de ofensivas, posições nos rankings e diferenciação de posts validados por professores), além de salvamento automático (*auto-save*) nas questões discursivas.
