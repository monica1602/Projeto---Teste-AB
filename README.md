# Projeto de Análise de Dados Loja Online Internacional

## Descrição do Projeto
O projeto é uma tarefa analítica de uma loja online internacional. Ele visa trabalhar com dados realizando uma análise com foco no resultado de um teste A/B, onde o grupo a é de controle e o grupo B é o do funil de novos pagamentos. Para a realização do teste A/B, foi utilizado alguns dados:
- Data de início: 07/12/2020
- Data de quando pararam de receber novos usuários: 21/12/2020
- Data de término: 01/01/2021
- Público: 15% de novo usuários da região da UE
- Número esperado de partivipantes do teste: 6000
O propósito do teste é testar mudanças relacionadas à introdução de uma recomendação do sistema melhorado. O resultado esperado com o teste A/B é em até 14 dias após o cadastro, usuários mostram uma conversão melhor nas visualizações de página do produto, ao adicionar itens ao carrinho e compras. A cada etapa do funil terá ao menos 10% de aumento

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

## Imagens

### Tabela eventos
<img src="https://github.com/user-attachments/assets/c6d8a48b-091e-421f-9c65-f79583684350" alt="Projeto AB"/>

### Tabela novos usuários
<img src="https://github.com/user-attachments/assets/b962a854-85ad-48c8-8d1b-9786e3fbbddc" alt="Projeto AB"/>

### Tabela data novos usuários
<img src="https://github.com/user-attachments/assets/1ebd59c6-6da1-4412-a9db-d1eb0433733c" alt="Projeto AB"/>

### Data novos usuários
<img src="https://github.com/user-attachments/assets/cd2d9dac-f539-45a6-8cb5-72bf3ce962a6" alt="Projeto AB" width="200"/>

### Região novos usuários
<img src="https://github.com/user-attachments/assets/05a41e9e-760e-4091-bdc7-e9664facc206" alt="Projeto AB" width="200"/>

### Dispositivo novos usuários
<img src="https://github.com/user-attachments/assets/9289b5ed-0e1e-4785-8be4-f204f6a93c8d" alt="Projeto AB" width="200"/>

### Cadastro por região em cada tipo de dispositivo
<img src="https://github.com/user-attachments/assets/d77d4333-6c15-4866-964b-f66afa9ba020" alt="Projeto AB" width="200"/>

### Tabela quantidade de usuários por tipo de evento
<img src="https://github.com/user-attachments/assets/ecb2bb11-bbfe-49b5-923d-a4c7a68d9582" alt="Projeto AB"/>

### Quantidade de eventos por data
<img src="https://github.com/user-attachments/assets/883fcb0a-0f7b-4dd3-8f8f-e1e9dc5d8b9e" alt="Projeto AB" width="200"/>

### Quantidade de dados adicionais por data
<img src="https://github.com/user-attachments/assets/727849ee-83de-4e49-90b2-f0c70513b1eb" alt="Projeto AB" width="200"/>

### Quantidade de eventos por data 2
<img src="https://github.com/user-attachments/assets/2bad6e63-ccb7-4cba-a25c-69b2f19177cf" alt="Projeto AB" width="200"/>

### Tabela grupo AB
<img src="https://github.com/user-attachments/assets/02e27517-1c30-4102-9c01-861534a5f34f" alt="Projeto AB"/>

### Grupo AB
<img src="https://github.com/user-attachments/assets/29693c5f-e2b3-4c4d-a184-8763b4e8d403" alt="Projeto AB" width="200"/>

### Quantidade de cada grupo teste AB
<img src="https://github.com/user-attachments/assets/87946a94-26d9-4a32-a038-9d3e70289518" alt="Projeto AB" width="200"/>

### Quantidade de cada grupo e teste AB
<img src="https://github.com/user-attachments/assets/3b4a9c76-fa18-4a26-bde8-a59fcfa365f5" alt="Projeto AB" width="200"/>

### Número de participantes por grupo no teste recomendado pelo sistema
<img src="https://github.com/user-attachments/assets/14daf424-150b-4bc8-8fa7-9c36b28b4f2b" alt="Projeto AB" width="200"/>

### Número de participantes por grupo no teste de interface
<img src="https://github.com/user-attachments/assets/2cdcaee4-3b3e-476d-8c50-e3ab487f10a5" alt="Projeto AB" width="200"/>

### Quantidade de usuários efetivos por mês, por semana e por dia
<img src="https://github.com/user-attachments/assets/b611a6b7-d9ba-4209-b33e-a0c900db3444" alt="Projeto AB"/>

### Média de eventos por usuários em cada dia
<img src="https://github.com/user-attachments/assets/3dc28d63-308e-4f2c-b28e-aa6cd00d8016" alt="Projeto AB" width="200"/>

### Tabela quantidade grupo AB
<img src="https://github.com/user-attachments/assets/a7d9031c-6e9a-460c-890e-162d4f821434" alt="Projeto AB"/>

### Quantidade de usuários por dia e o acumulado
<img src="https://github.com/user-attachments/assets/9733be92-baa3-46a4-bb32-677e58f042a2" alt="Projeto AB" width="200"/>

### Quantidade de usuários entre as etapas
<img src="https://github.com/user-attachments/assets/76fa8da5-d909-4a76-a479-41b7d1884ff3" alt="Projeto AB" width="200"/>

### Data de quando não recebe mais usuários entre os grupos
<img src="https://github.com/user-attachments/assets/2a97b49a-3d4e-4d2d-9b2c-e2d3ae2f12fe" alt="Projeto AB" width="200"/>

### Data de quando não recebe mais usuários entre os grupos depois da data base
<img src="https://github.com/user-attachments/assets/920c19be-f808-4dd1-80a7-6614bf0e4530" alt="Projeto AB" width="200"/>

### Funil de eventos
<img src="https://github.com/user-attachments/assets/726b1d70-6d7d-4633-8558-110629b474d9" alt="Projeto AB" width="200"/>

### Quantidade de eventos por data
<imgh src="https://github.com/user-attachments/assets/6576f7e9-1a4c-43f9-b667-37dea47b96aa" alt="Projeto AB" width="200"/>

### Nome do evento de marketing por região
<img src="https://github.com/user-attachments/assets/fd2ea49c-2c5e-477c-a530-7a49f675cda9" alt="Projeto AB" width="200"/>

### Quantidade de eventos de marketing por região
<img src="https://github.com/user-attachments/assets/8e520b44-7d1d-46fe-bc91-79cd29ce96fa" alt="Projeto AB" width="200"/>

### Tabela número de registros em cada data EU
<img src="https://github.com/user-attachments/assets/51cc8815-43a6-4440-ad65-8d350be9febb" alt="Projeto AB"/>

### Tabela de aumento em relação ao valor anterior EU
<img src="https://github.com/user-attachments/assets/81603f36-0f09-4537-a599-b98b6d3bbe10" alt="Projeto AB"/>

### Tabela número de registros em cada data NA
<img src="https://github.com/user-attachments/assets/3ff337d3-42ac-42fa-8eba-4d0e041cd67f" alt="Projeto AB"

### Tabela de aumento em relação ao valor anterior NA
<img src="https://github.com/user-attachments/assets/cbfbdd7d-b274-4620-be60-a7e0450dd0bc" alt="Projeto AB"/>

### Tabela número de registros em cada data APAC
<img src="https://github.com/user-attachments/assets/1a6c89ec-7ee9-443d-b50a-3c81b6d5cfdb" alt="Projeto AB"/>

### Tabela de aumento em relação ao valor anterior APAC
<img src="https://github.com/user-attachments/assets/83bf8c73-e877-4772-81a3-2da96f07d01f" alt="Projeto AB"/>

### Tabela número de registros em cada data CIS
<img src="https://github.com/user-attachments/assets/aa9cd73d-23bd-4c2f-81b6-17d4fbb712a0" alt="Projeto AB"/>

### Tabela de aumento em relação ao valor anterior CIS
<img src="https://github.com/user-attachments/assets/38d17c4d-ed9b-4a15-98e1-fed2609a8051" alt="Projeto AB"/>

## Resultados
- Data de quando pararam de receber novos usuários não ocorreu em 21/12/2020, mas sim dia 23/12/2020
- O público da região EU realmente teve um aumento de mais de 15% assim como nas demais regiões
- O propósito do teste de introduzir mudanças realmente aconteceu, porém não houve um aumento de pelo menos 10% a cada nova etapa, que era o resultado esperado
- O número de participantes no teste foi de 6311, porém vários participantes estavam nos dois grupos. E excluindo os valores duplicados, a quantidade vai para 5800, menos que o esperado
- Existe diferença estatística entre os grupos
- A partir de um determinado dia, o teste aparentemente não vale mais a pena
- Foi possível analisar o comportamento dos usuários e a quantidade que perdemos durante o processo

## Aprendizados
- Análise de dados
- Limpeza dos dados
- Manipulação de tabelas
- Análise de funil de vendas
- Construção e análise de gráficos
- Comparação estatística de grupos de teste

## Contexto real
- Qualquer empresa que deseja entender melhor o comportamento de seus usuários
- Empresas que desejam melhorar o desempenho
- Empresas contratadas que realizam análises, como análises de funil, para entender as empresas que a contrataram e como e onde melhorar
- Escolas ou instituições de ensino que desejam entender o porque seus alunos estão abandonando os estudos
  
## Como executar o Proejto
- Clone o resporitório
- Navegue até o diretório do projeto
- Abra o projeto no seu IDE favorito
- Instale as dependências
- Execute o script principal
