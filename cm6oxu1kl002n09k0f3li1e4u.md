---
title: "O que é o BigQuery e para que ele serve?"
seoTitle: "Introdução ao BigQuery: Utilização e Benefícios"
seoDescription: "Descubra como o BigQuery, serviço do Google Cloud, facilita a análise de grandes volumes de dados para gerar insights estratégicos"
datePublished: 2022-05-30T03:16:38.217Z
cuid: cm6oxu1kl002n09k0f3li1e4u
slug: bigquery-pra-que-ele-serve
tags: data, data-science, big-data, data-analysis, google-cloud, google, google-cloud-platform, bigquery, gcp

---

O serviço do Google Cloud Platform, BigQuery, é um data warehouse gerenciado.

Data Warehouse é como um depósito de dados, onde se pode guardar informações relativas às atividades de uma organização em bancos de dados, de forma consolidada. Um data warehouse como o BigQuery favorece a criação de relatórios, a análise de grandes volumes de dados — que podem chegar até peta bytes de dados e que podem ser coletados de diversas fontes — e a obtenção de informações estratégicas que podem facilitar a tomada de decisão.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1738580312373/28154542-133f-4d86-84f9-ef622ba10dc0.png)

Data Warehouse flow

O BigQuery cuida da infraestrutura do DW para que você possa se concentrar nas consultas SQL para lidar com as questões necessárias ao negócio, sem que você tenha que cuidar e gerenciar tópicos de back-end como implantação, escalabilidade e segurança. Ele fornece dois serviços em um só: armazenamento e análise de dados com recursos integrados (como por exemplo, análise geoespacial de *machine learning*, *business intelligence*, entre outros.).

Via de regra, o BigQuery é uma solução *serverless* (sem servidor) totalmente gerenciado, ou seja, isso significa que você pode usar o tradicional SQL para fazer consultas e solucionar os problemas da sua necessidade, usando interfaces como o Console do Google Cloud e a ferramenta de linha de comando do BigQuery, sem ter que lidar com questões de infraestrutura e segurança do DW.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1738580314216/e2c3d529-d452-48ab-be37-5c50664cabfd.png)

BigQuery console on Google Cloud interface

A utilização do BigQuery é em um modelo PaaS, onde a precificação é flexível e é baseada conforme o seu uso, onde você paga pelo número de bytes processados nas suas consultas, e também pelas tabelas armazenadas permanentemente. Por padrão, todos os dados no BigQuery são criptografados, sem que você tenha que fazer algum tipo de configuração ou implementação.

E se tratando de machine learning, o BigQuery também oferece recursos de ML, sendo possível criar modelos de *machine learning* diretamente nele, usando SQL Mas você também pode usar outras ferramentas de ML no BigQuery, como o Vertex AI, e nativamente você pode exportar seus *datasets* criados no BigQuery e integrá-los em outras ferramentas de ML.

**Fluxo básico de um processo de Big Data com o BigQuery**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1738580315843/2cd33035-d8ec-4fd0-872e-6256b67f08c9.png)

A ingestão de dados pode ser de dados em tempo real (*streaming*) ou dados em lote (*batch*). É recomendável que os dados em streaming sejam tratados pelo Pub/Sub, e os dados em *batch*, pelo Cloud Storage. Após essa etapa, essas duas pipelines podem ser carregadas no Dataflow para processá-las e realizar o processo ETL. Feito isso, os dados podem ser carregados e vinculados ao BigQuery, e preparar esses dados para diversos outros fins, como visualização dos dados, modelos de aprendizado de máquina, etc.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1738580317162/b64dfad8-3199-4744-b142-6e7a836cfd5a.png)

As saídas de informações do BigQuery alimentam, geralmente, dois *buckets*: um de *Business Intelligence* e outro de ferramentas de *Machine Learning*. Se você for um analista de negócios, ou analista de dados, você pode se conectar ao *bucket* de BI e usar sua ferramenta de visualização preferida, como por exemplo, Data Studio, PowerBI, Looker, Tableau, entre outros. Já se você for um cientista de dados, ou engenheiro de *machine learning*, você pode diretamente integrar o BigQuery através do Auto ML ou Vertex AI Workbench.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1738580319039/21094c96-68eb-4328-9ae9-aaabe319b812.png)