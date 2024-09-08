# Projeto de Análise de Dados Loja Online Internacional

## Descrição do Projeto
O projeto é uma tarefa analítica de uma loja online internacional. Ele visa trabalhar com dados realizando uma análise com foco no resultado de um teste A/B

## As tarefas são:
- Análise exploratória de dados
- Conversão em diferentes etapas do funil
- Responder as seguintes perguntas:
  - O número de eventos por isuário é distribuído igualmente entre as amostras?
  - Os usuários de ambas as amostras estão presentes?
  - Como o número de eventos é distribuído entre os dias?
  - Existem qualquer particularidade nos dados que você deve considerar antes de começar o teste A/B?
- Realizar e avaliar os resultados do teste A/B

## Dicionário de dados
- ab_project_marketing_events_us.csv: o calendário de eventos de marketing para 2020
  - 'name': nome dos eventos de marketing
  - 'regions': regiões onde a campanha será realizada
  - 'start_dt': data de início da camapanha
  - 'finish_dt': data de término da campanha
- final_ab_new_users_upd_us.csv: todos os usuários que se cadastraram na loja online de 7 de dezembro a 21 de dezembro de 2020
  - 'user_id': identificação deo usuário
  - 'first_date': data de cadastro
  - 'region': região do usuário
  - 'device': dispositivo usado para o cadastro
- final_ab_events_upd_us.csv: todos os eventos dos novos usuários dentro do período de 7 de dezembro de 2020 até 1 de janeiro de 2021
  - 'user_id': identificação do usuário
  - 'event_dt': data e hora do evento
  - 'event_name': nome da fonte do evento
  - 'details': dados adiconais sober o evento
- final_ab_participants_upd_us.csv: tabela contendo os participantes do teste
  - 'user_id': identificação do usuário
  - 'ab_test': nome do teste
  - 'group': o grupo de teste ao qual o usuário pertencia

## Ferramentas e Bibliotecas utilizadas
- Pyhton: Linguagem principal utilizada para a análise
- Pandas: Biblioteca para manipulação e análise de dados
- Matplotlib: Biblioteca para criação de gráficos
- Datetime: Biblioteca para manipulação de datas e horas
- Statsmodels.stats.proportion.ztest: realizar o teste zteste
- Scipy.stats.mannwhitneyu: realizar o teste de Mann-Whitney U

## Resultados
- Existe diferença estatística entre os grupos
- A partir de um determinado dia, o teste aparentemente não vale mais a pena
- Foi possível analisar o comportamento dos usuários e a quantidade que perdemos durante o processo
- Não foi possível concluir se realmente houve um aumento de 15% de novos usuários e nem se tivemos um aumento de 10% nas etapas do funil

## Aprendizados
- Análise de dados
- Limpeza dos dados
- Manipulação de tabelas
- Análise de funil de vendas
- Construção e análise de gráficos
- Comparação estatística de grupos de teste

## Como executar o Proejto
- Clone o resporitório
- Navegue até o diretório do projeto
- Abra o projeto no seu IDE favorito
- Instale as dependências
- Execute o script principal
