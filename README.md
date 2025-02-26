# Projeto de Análise de Dados - Loja Online Internacional

## Descrição do Projeto
Este projeto visa realizar uma análise de dados de um teste A/B aplicado em uma loja online internacional. O teste tem como objetivo avaliar o impacto de uma nova recomendação do sistema em relação à conversão dos usuários nas diversas etapas do funil de vendas. Os dados utilizados no teste são os seguintes:
- Data de início: 07/12/2020
- Data de término: 01/01/2021
- Data em que pararam de receber novos usuários: 21/12/2020
- Público-alvo: 15% de novos usuários da região da União Europeia (UE)
- Número esperado de participantes: 6.000
A expectativa do teste A/B é que, com a introdução da recomendação do sistema melhorada, os usuários apresentem um aumento de pelo menos 10% nas conversões em cada etapa do funil: desde a visualização das páginas de produto até a adição de itens ao carrinho e finalização da compra.
O principal objetivo é testar a eficácia das mudanças na experiência do usuário e determinar se o novo sistema de recomendação contribui para a melhoria das métricas de conversão.

## As tarefas são:
- Análise exploratória de dados:
  - Entender a estrutura dos dados e as distribuições antes de realizar o teste A/B.
  - Verificar se existem padrões ou anomalias que possam influenciar os resultados do teste.
- Conversão em diferentes etapas do funil:
  - Avaliar como os usuários estão avançando nas etapas do funil: visualização de página de produto, adição ao carrinho e finalização da compra.
  - Comparar as taxas de conversão entre o grupo A (controle) e o grupo B (teste) para verificar a eficácia das mudanças.
- Responder às seguintes perguntas:
  - O número de eventos por usuário é distribuído igualmente entre as amostras?
    - Verificar se os grupos A e B têm distribuições semelhantes em relação ao número de eventos por usuário. Isso ajuda a garantir que a comparação entre os grupos seja justa.
  - Os usuários de ambas as amostras estão presentes?
    - Confirmar se a divisão dos usuários foi feita de forma aleatória e equilibrada entre os dois grupos, para evitar qualquer viés na amostra.
  - Como o número de eventos é distribuído entre os dias?
    - Analisar a distribuição de eventos ao longo do período do teste (de 07/12/2020 a 01/01/2021), observando se há variações significativas que possam afetar os resultados.
  - Existem qualquer particularidade nos dados que você deve considerar antes de começar o teste A/B?
    - Investigar se há fatores como sazonalidade, variações de tráfego, ou outros comportamentos dos usuários que podem afetar a eficácia do teste.
- Realizar e avaliar os resultados do teste A/B:
  - Aplicar o teste A/B com base nos dados coletados, comparar as métricas de conversão entre os grupos e avaliar se a mudança no sistema de recomendação teve o impacto esperado nas taxas de conversão

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
- Python: Linguagem principal utilizada para análise dos dados e implementação de modelos estatísticos.
- Pandas: Biblioteca essencial para manipulação e análise de dados, sendo fundamental para realizar operações de limpeza e transformação de dados.
- Matplotlib: Biblioteca utilizada para criação de gráficos e visualizações dos dados, ajudando a representar os resultados de forma clara e compreensível.
- Datetime: Biblioteca para manipulação de datas e horas, fundamental para trabalhar com as séries temporais de eventos no teste A/B.
- Statsmodels.stats.proportion.ztest: Função utilizada para realizar o teste z de proporções, comparando as taxas de conversão entre os grupos de controle e teste, para verificar se há diferença significativa entre eles.
- Scipy.stats.mannwhitneyu: Teste de Mann-Whitney U, utilizado para comparar as distribuições entre os grupos, especialmente quando os dados não seguem uma distribuição normal, ajudando a avaliar se há diferenças significativas nas métricas de conversão entre os grupos A e B.

## Imagens

### Tabela eventos
<img src="https://github.com/user-attachments/assets/c6d8a48b-091e-421f-9c65-f79583684350" alt="Projeto AB"/>

### Tabela novos usuários
<img src="https://github.com/user-attachments/assets/b962a854-85ad-48c8-8d1b-9786e3fbbddc" alt="Projeto AB"/>

### Tabela data novos usuários
<img src="https://github.com/user-attachments/assets/1ebd59c6-6da1-4412-a9db-d1eb0433733c" alt="Projeto AB"/>

### Gráfico - Data novos usuários
<img src="https://github.com/user-attachments/assets/cd2d9dac-f539-45a6-8cb5-72bf3ce962a6" alt="Projeto AB" width="800"/>

### Gráfico - Região novos usuários
<img src="https://github.com/user-attachments/assets/05a41e9e-760e-4091-bdc7-e9664facc206" alt="Projeto AB" width="800"/>

### Gráfico - Dispositivo novos usuários
<img src="https://github.com/user-attachments/assets/9289b5ed-0e1e-4785-8be4-f204f6a93c8d" alt="Projeto AB" width="800"/>

### Gráfico - Cadastro por região em cada tipo de dispositivo
<img src="https://github.com/user-attachments/assets/d77d4333-6c15-4866-964b-f66afa9ba020" alt="Projeto AB" width="800"/>

### Tabela quantidade de usuários por tipo de evento
<img src="https://github.com/user-attachments/assets/ecb2bb11-bbfe-49b5-923d-a4c7a68d9582" alt="Projeto AB"/>

### Gráfico - Quantidade de eventos por data
<img src="https://github.com/user-attachments/assets/883fcb0a-0f7b-4dd3-8f8f-e1e9dc5d8b9e" alt="Projeto AB" width="800"/>

### Gráfico - Quantidade de dados adicionais por data
<img src="https://github.com/user-attachments/assets/727849ee-83de-4e49-90b2-f0c70513b1eb" alt="Projeto AB" width="800"/>

### Gráfico - Quantidade de eventos por data 2
<img src="https://github.com/user-attachments/assets/2bad6e63-ccb7-4cba-a25c-69b2f19177cf" alt="Projeto AB" width="800"/>

### Tabela grupo AB
<img src="https://github.com/user-attachments/assets/02e27517-1c30-4102-9c01-861534a5f34f" alt="Projeto AB"/>

### Gráfico - Grupo AB
<img src="https://github.com/user-attachments/assets/29693c5f-e2b3-4c4d-a184-8763b4e8d403" alt="Projeto AB" width="800"/>

### Gráfico - Quantidade de cada grupo teste AB
<img src="https://github.com/user-attachments/assets/87946a94-26d9-4a32-a038-9d3e70289518" alt="Projeto AB" width="800"/>

### Gráfico - Quantidade de cada grupo e teste AB
<img src="https://github.com/user-attachments/assets/3b4a9c76-fa18-4a26-bde8-a59fcfa365f5" alt="Projeto AB" width="800"/>

### Gráfico - Número de participantes por grupo no teste recomendado pelo sistema
<img src="https://github.com/user-attachments/assets/14daf424-150b-4bc8-8fa7-9c36b28b4f2b" alt="Projeto AB" width="800"/>

### Gráfico - Número de participantes por grupo no teste de interface
<img src="https://github.com/user-attachments/assets/2cdcaee4-3b3e-476d-8c50-e3ab487f10a5" alt="Projeto AB" width="800"/>

### Gráfico - Quantidade de usuários efetivos por mês, por semana e por dia
<img src="https://github.com/user-attachments/assets/b611a6b7-d9ba-4209-b33e-a0c900db3444" alt="Projeto AB"/>

### Gráfico - Média de eventos por usuários em cada dia
<img src="https://github.com/user-attachments/assets/3dc28d63-308e-4f2c-b28e-aa6cd00d8016" alt="Projeto AB" width="800"/>

### Tabela quantidade grupo AB
<img src="https://github.com/user-attachments/assets/a7d9031c-6e9a-460c-890e-162d4f821434" alt="Projeto AB"/>

### Gráfico - Quantidade de usuários por dia e o acumulado
<img src="https://github.com/user-attachments/assets/9733be92-baa3-46a4-bb32-677e58f042a2" alt="Projeto AB" width="800"/>

### Gráfico - Quantidade de usuários entre as etapas
<img src="https://github.com/user-attachments/assets/76fa8da5-d909-4a76-a479-41b7d1884ff3" alt="Projeto AB" width="800"/>

### Gráfico - Data de quando não recebe mais usuários entre os grupos
<img src="https://github.com/user-attachments/assets/2a97b49a-3d4e-4d2d-9b2c-e2d3ae2f12fe" alt="Projeto AB" width="800"/>

### Gráfico - Data de quando não recebe mais usuários entre os grupos depois da data base
<img src="https://github.com/user-attachments/assets/920c19be-f808-4dd1-80a7-6614bf0e4530" alt="Projeto AB" width="800"/>

### Gráfico - Funil de eventos
<img src="https://github.com/user-attachments/assets/726b1d70-6d7d-4633-8558-110629b474d9" alt="Projeto AB" width="800"/>

### Gráfico - Quantidade de eventos por data
<img src="https://github.com/user-attachments/assets/6576f7e9-1a4c-43f9-b667-37dea47b96aa" alt="Projeto AB" width="800"/>

### Gráfico - Nome do evento de marketing por região
<img src="https://github.com/user-attachments/assets/fd2ea49c-2c5e-477c-a530-7a49f675cda9" alt="Projeto AB" width="800"/>

### Gráfico - Quantidade de eventos de marketing por região
<img src="https://github.com/user-attachments/assets/8e520b44-7d1d-46fe-bc91-79cd29ce96fa" alt="Projeto AB" width="800"/>

### Tabela número de registros em cada data EU
<img src="https://github.com/user-attachments/assets/51cc8815-43a6-4440-ad65-8d350be9febb" alt="Projeto AB"/>

### Tabela de aumento em relação ao valor anterior EU
<img src="https://github.com/user-attachments/assets/81603f36-0f09-4537-a599-b98b6d3bbe10" alt="Projeto AB"/>

### Tabela número de registros em cada data NA
<img src="https://github.com/user-attachments/assets/3ff337d3-42ac-42fa-8eba-4d0e041cd67f" alt="Projeto AB"/>

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
- Data de interrupção de novos usuários: A data de quando pararam de receber novos usuários foi 23/12/2020, e não 21/12/2020, como originalmente mencionado.
- Público da região da UE: O público da região da União Europeia realmente teve um aumento superior a 15%, assim como ocorreu nas demais regiões, o que indica que a amostra foi representativa.
- Propósito do teste: O teste tinha como objetivo introduzir mudanças no sistema de recomendação, e, de fato, essas mudanças foram implementadas. Contudo, os resultados não atingiram o aumento esperado de pelo menos 10% a cada etapa do funil (visualizações de página, adição ao carrinho, compras), o que sugere que a mudança não teve o impacto desejado.
- Número de participantes: Inicialmente, foram registrados 6311 participantes, porém vários usuários estavam presentes em ambos os grupos. Após a remoção de duplicatas, o número de participantes foi reduzido para 5800, o que ficou abaixo da meta de 6000.
- Diferença estatística: Foi constatada uma diferença estatística significativa entre os grupos A e B, indicando que as mudanças no sistema de recomendação afetaram o comportamento dos usuários de forma mensurável, mas não no nível esperado.
- Validade do teste ao longo do tempo: Após determinado dia, os resultados sugerem que o teste já não vale mais a pena, possivelmente devido a mudanças no comportamento dos usuários ao longo do tempo ou à saturação do efeito das mudanças.
- Análise do comportamento do usuário: Foi possível realizar uma análise detalhada sobre o comportamento dos usuários durante o teste, identificando que houve perda de usuários em diferentes etapas do funil, o que pode indicar pontos de atrito ou de frustração no processo de compra.

## Aprendizados
- Análise de dados: Investigação detalhada dos dados coletados, buscando identificar padrões e tendências relevantes.
- Limpeza dos dados: Processamento dos dados para remover ou corrigir inconsistências, como valores ausentes, duplicados e formatação inadequada.
- Manipulação de tabelas: Alteração de estruturas de dados, incluindo transformação de colunas, renomeação, e conversão de tipos de dados para facilitar a análise.
- Análise de funil de vendas: Estudo das diferentes etapas do funil de vendas, observando a conversão de usuários de uma etapa para outra e identificando possíveis perdas ou gargalos.
- Construção e análise de gráficos: Criação de visualizações que ajudam a entender melhor a distribuição e os padrões nos dados, como gráficos de barras, linhas, e dispersão.
- Comparação estatística de grupos de teste: Uso de testes estatísticos (como o teste t ou Mann-Whitney) para comparar o desempenho entre grupos de teste e controle, verificando a significância das diferenças observadas.

## Contexto real
- Empresas que buscam compreender o comportamento de seus usuários: Organizações que analisam detalhadamente as ações e preferências de seus clientes para aprimorar a experiência e maximizar os resultados.
- Empresas que desejam melhorar o desempenho: Negócios que estão focados em aumentar a eficiência, aumentar conversões ou melhorar o processo de vendas, e que precisam de dados para tomar decisões informadas.
- Empresas contratadas que realizam análises, como análises de funil, para entender as empresas que as contrataram e como e onde melhorar: Consultorias e empresas de análise de dados que ajudam outras organizações a identificar gargalos em seus processos e estratégias, com foco em métricas de desempenho como conversões, retenção e outros KPIs.
- Escolas ou instituições de ensino que desejam entender o porquê de seus alunos estarem abandonando os estudos: Instituições que buscam entender fatores que impactam a desistência ou evasão escolar, para implementar estratégias que aumentem a retenção de alunos.
  
## Como executar o Proejto
- Clone o resporitório
- Navegue até o diretório do projeto
- Abra o projeto no seu IDE favorito
- Instale as dependências
- Execute o script principal
