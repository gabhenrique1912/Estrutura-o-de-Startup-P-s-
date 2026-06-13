# Estrutura-o-de-Startup-P-s-
Apresenta uma versão focada em sprints para a criação do MVP de um software de gestão de alunos e treinos. O objetivo principal é lançar um produto enxuto rapidamente para validar a proposta de valor com profissionais reais e iniciar a monetização.


ID,Sprint,Titulo,Papel,Historia de Usuario,MoSCoW,StoryPoints,Criterios de Aceitacao
US01,Sprint 1,Cadastro de Personal,Personal Trainer,"Como Personal, quero cadastrar minha conta para ter um espaço de trabalho próprio",Must,5,"UUID tenant_id único gerado no banco; dados cadastrais salvos corretamente."
US02,Sprint 1,Autenticação de Usuário,Usuário,"Como Usuário, quero fazer login com e-mail e senha para acessar o app com segurança",Must,5,"Token JWT emitido no login; senhas criptografadas com bcrypt no banco de dados."
TS01,Sprint 1,Isolamento de Banco de Dados,Time de Devs,"Como Time de Devs, preciso configurar o PostgreSQL para aplicar o tenant_id nas consultas",Must,8,"Middleware ORM aplica automaticamente o filtro WHERE tenant_id em todas as queries."
TS02,Sprint 1,Ambiente Cloud e CI/CD,Time de Devs,"Como Time de Devs, preciso automatizar o deploy para facilitar testes e entregas",Should,5,"Código integrado ao repositório é testado e publicado automaticamente em ambiente de homologação."
QA01,Sprint 1,Testes de Isolamento de Dados,QA,"Como QA, preciso validar o isolamento de dados para garantir que um personal não veja dados de outro",Must,3,"Criação de testes automatizados simulando acessos com tokens de inquilinos diferentes."
US03,Sprint 2,Gestão de Alunos,Personal Trainer,"Como Personal, quero convidar e gerenciar minha lista de alunos para organizar minha consultoria",Must,5,"Link de convite enviado por e-mail/WhatsApp; aluno vinculado corretamente ao ID do personal."
US04,Sprint 2,Construtor de Treinos,Personal Trainer,"Como Personal, quero montar fichas de treino personalizadas para enviar aos meus alunos",Must,8,"Interface simples para adicionar exercícios, número de séries, repetições e carga."
US05,Sprint 2,Visualização e Registro de Treino,Aluno,"Como Aluno, quero ver meu treino do dia e marcar as séries feitas para registrar minha atividade",Must,5,"Exibição do treino do dia; botão de check para cada série realizada; salvamento de peso utilizado."
US06,Sprint 2,Chat Integrado,Usuário,"Como Aluno/Personal, quero trocar mensagens rápidas no app para manter a comunicação ativa",Should,5,"Mensagens enviadas em tempo real com histórico visível por aluno."
QA02,Sprint 2,Testes do Fluxo de Exercícios,QA,"Como QA, preciso testar a montagem e marcação de treinos para evitar bugs de exibição",Must,3,"A validação ponta a ponta simula a criação de um treino e sua execução pelo app do aluno."
US07,Sprint 3,Cobrança Automática,Personal Trainer,"Como Personal, quero cobrar mensalidades via PIX ou Cartão de forma integrada para evitar calotes",Must,8,"Integração com Stripe Connect operando; geração de chave Pix copia e cola e checkout de cartão."
US08,Sprint 3,Notificações via WhatsApp,Aluno,"Como Aluno, quero receber alertas de treinos e vencimento de mensalidade no WhatsApp para não esquecer",Should,5,"Integração com API de WhatsApp enviando lembretes automáticos baseados no cronograma."
US09,Sprint 3,Gráficos de Evolução Física,Aluno,"Como Aluno, quero registrar peso e fotos para visualizar meu progresso em gráficos",Could,5,"Tela de entrada de peso e medidas; exibição de gráfico de linha com a evolução do peso."
TS03,Sprint 3,Ambiente de Produção e Ajustes,Time de Devs,"Como Time de Devs, preciso migrar as tabelas e preparar o app para o público real",Must,5,"Banco de dados de produção criado com índices otimizados; certificados digitais SSL ativos."
QA03,Sprint 3,Testes Finais de Homologação,QA,"Como QA, preciso validar todo o fluxo financeiro e de notificações para certificar a entrega",Must,3,"Testes manuais e automáticos de ponta a ponta simulando pagamento, liberação de treino e disparos."
