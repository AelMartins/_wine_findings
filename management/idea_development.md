## Projeto: Wine Findings

### Descrição Geral
Wine Findings é uma aplicação multiplataforma que permita aos usuários prever a qualidade de um vinho e receber recomendações de harmonizações baseadas em seus gostos pessoais através de técnicas de mineração de dados que agrupam padrões e criam dashboards interativos a fim de explicar as relações dos dados com suas preferencias palativas, oferecendo assim uma experiência de descoberta e certeza de uma boa escolha, ajudando o usuário a encontrar vinhos que realmente correspondam ao seu perfil.

---

### Dados Utilizados
O sistema usa um modelo de Machine Learning treinado com o dataset "[Portuguese Wines Blog os Vinhos](https://www.kaggle.com/datasets/mariazhokhova/portuguese-wines-blog-os-vinhos)" disponível no [Kaggle](https://www.kaggle.com/).

> [!NOTE]
> Se estamos enganados e o seu tipo de licensa não permite usá-lo ou compartilhá-lo desta maneira, iremos remover o conteúdo caso requisitado.

<!-- É interessante pesquisar permissão e maneiras de coletar mais dados diretamente do site, eles estão mais atualizados e em maior quantidade -->

São quase três mil avaliações de vinhos coletados diretamente do blog "[Os Vinhos](https://osvinhos.blogspot.com/)" de diversos tipos e diversas regiões do mundo.

Algumas colunas possuem conteúdo em português e os valores "-1", "null" ou "-" correspondem a dados não encontrados no blog. O álcool é calculado em porcentagem e os preços dos vinhos em euros. A pontuação da qualidade de cada vinho fica entre 0 e 20. 

---

### Como o Projeto Será Desenvolvido e o que Será Levado em Conta

#### 1. Disponibilidade da Plataforma
- **Web, Mobile e Desktop**  
  - Interface responsiva utilizando frameworks como React, Angular ou Vue, React Native ou Flutter para mobile, Electron ou tecnologia similar para desktop.
  - Permite que o usuário insira dados (ex.: região, produtor, tipos de safra, etc.) e visualize as previsões.

#### 2. Interação do Usuário
- **Definição de Preferências e Exploração dos Dados:**  
  - O usuário pode configurar suas preferências ou selecionar parâmetros específicos para explorar as relações entre os dados.
- **Dashboard Interativo:**  
  - Apresenta insights e visualizações dinâmicas que permitem explorar, por exemplo, como variáveis como o tipo de safra e as descrições avaliativas do gosto influenciam a qualidade do vinho.  
  - A interface educa o usuário, auxiliando na descoberta de perfis que se alinham com seus gostos pessoais.

#### 3. Mineração de Dados
- **Pré-processamento:**  
  - Limpeza dos dados, tratamento de valores ausentes e normalização dos atributos.
- **Análises Exploratórias:**  
  - Identificação das variáveis que mais influenciam a qualidade do vinho.
  - Agrupamento dos vinhos para identificar padrões, clusters e associações entre as variáveis.
- **Recomendações Baseadas em Padrões:**  
  - Sugestão de características valorizadas de acordo com os padrões identificados, permitindo ao usuário conhecer melhor seu perfil.

#### 4. Aprendizagem de Máquina
- **Treinamento do Modelo:**  
  - Desenvolvimento de um modelo de Machine Learning (utilizando técnicas de regressão ou classificação) para prever a qualidade do vinho.
- **Integração de Métodos Supervisionados e Não Supervisionados:**  
  - Utilização de algoritmos supervisionados para predições e técnicas de agrupamento (clustering) para identificar segmentos de vinhos e gerar recomendações personalizadas.
- **Validação do Modelo:**  
  - Aplicação de validação cruzada e uso de métricas como RMSE ou acurácia para assegurar a eficácia do modelo.

#### 5. Armazenamento de Dados
- **Banco de Dados:**  
  - Utilização de um SGBD (como PostgreSQL ou MongoDB) para armazenar registros de consultas, feedback dos usuários e histórico de previsões.
  - Implementação de técnicas de indexação e otimização para garantir desempenho mesmo com grandes volumes de dados.

#### 6. Comunicação do Sistema
- **Comunicação Síncrona:**  
  - Utilização de API REST (HTTP) ou WebSockets para interações diretas, onde o usuário espera respostas imediatas.
- **Comunicação Assíncrona via Mensageria:**  
  - Emprego de mensageria (por exemplo, RabbitMQ, Kafka ou MQTT) para:
    - Processar tarefas pesadas (como treinamento do modelo ou análise de dados) em segundo plano.
    - Enfileirar solicitações de previsão ou de atualização do dashboard, permitindo que os resultados sejam processados e enviados posteriormente à interface.
    - Enviar notificações e atualizações em tempo real (ex.: quando um novo insight ou cluster for identificado), sem depender de requisições HTTP diretas.
    - Registrar eventos e ações do sistema para monitoramento e análise contínua de performance, aumentando a escalabilidade e resiliência do sistema.

#### 7. Disponibilidade Remota
- **Implantação na Nuvem:**  
  - Configuração da aplicação em um ambiente na nuvem (AWS, Azure ou Google Cloud).
  - Garantia de alta disponibilidade por meio de balanceamento de carga e escalabilidade automática.
  - Implementação de políticas de segurança (controle de acesso, criptografia, monitoramento constante) e análises para otimização de custos.

#### 8. Documentação e Gestão do Projeto

- **Testes:**  
  - Implementação de testes unitários e de integração para garantir a robustez da API e das funcionalidades críticas.
- **Documentação:**  
  - Cada linha de código será documentada de forma clara.  
  - Todas as análises e decisões serão registradas com justificativas baseadas em fatos e métricas.
- **Controle de Versão:**  
  - Organização do projeto com Git, utilizando um repositório no GitHub para versionamento, gestão de branches e colaborações.
