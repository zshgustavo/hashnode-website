---
title: "Big Data e Machine Learning no Google Cloud Platform — Introdução aos produtos e serviços de…"
seoTitle: "Google Cloud: Big Data & Machine Learning Overview"
seoDescription: "Descubra os produtos e serviços de Big Data e Machine Learning no Google Cloud Platform e como eles transformam a computação em nuvem"
datePublished: 2022-05-21T00:09:41.057Z
cuid: cm6oxueho000k09l89kthh95k
slug: big-data-e-machine-learning-no-google-cloud-platform-introduc3a7c3a3o-aos-produtos-e-servic3a7os-de-54e911fcbf14
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1738580336804/791c0d9b-ce90-4483-a332-d823a2479d0a.jpeg

---

Há três camadas na infraestrutura do Google Cloud:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1738580324758/2f13981c-11e1-44e6-911d-2b0eaa487b42.png)

1\. **Networking & Security**: É a camada base, que estabelece a base de toda a infraestrutura e aplicações da GCP;  
2\. **Compute and Storage**: na segunda camada, está a computação e armazenamento, que independentes um do outro escalam as aplicações e serviços com base na necessidade do cliente, usuário ou serviço;  
3\. **Big Data and ML Products**: na terceira camada está o Big Data e Machine Learning que permitem que você execute tarefas, possa fornecer pipelines de dados e modelos de ML, além de que essas tarefas podem ser realizadas sem a necessidade de gerenciar as infraestruturas implícitas necessárias.

**Compute**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1738580326680/90ba280e-7ff8-40f6-8dc0-f81270ee7e16.png)

O Google Cloud Platform fornece vários serviços de computação, o primeiro que vamos falar sobre é o **Compute Engine**, que é uma oferta ou infraestrutura como um serviço (IaaS) que fornece armazenamento bruto de computação e recursos de rede organizados virtualmente, semelhantes a data centers físicos.

O segundo é o **Google Kubernetes Engine (GKE)** que executa aplicativos e faz a orquestração de containers em um ambiente de nuvem, diferentemente do Compute Engine que utiliza maquinas virtuais (VMs) individuais;

O terceiro é o **App Engine**, uma plataforma como serviço (PaaS), que vincula o código binário a bibliotecas e é focado e dá acessos às necessidades lógicas dos aplicativos de infraestrutura, permitindo que mais recursos sejam focados na lógica do aplicativo.

Já o **Cloud Run**, o quarto dessa lista, é uma plataforma de computação que tem sua execução totalmente gerenciada (por exemplo, você pode escolher qual linguagem de programação prefere usar), sem servidor e que permite executar contêineres. Ele lida propriamente com o provisionamento de recursos para atender as demandas necessárias para o funcionamento adequado, e o pagamento é feito apenas pelos recursos/requisições utilizados.

O quinto é o **Cloud Functions**, que executa código em resposta a eventos como quando um novo arquivo é carregado na nuvem de armazenamento. Ele é, assim como o Cloud Run, um ambiente de execução totalmente sem servidor.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1738580328534/83fe10f2-30b1-40d6-a7ff-8453b9b5f673.png)

**Storage**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1738580330601/d9e200c1-d098-44d5-b106-d3b11f0987ac.png)

Há diversos serviços fornecidos para armazenamento em nuvem, que em vários pontos se torna diferente de armazenamento em data centers físicos, alguns exemplos são **Cloud Storage**, **Cloud BigTable**, **Cloud SQL**, **Cloud Spanner** e o **Firestore**.   
O intuito desses produtos é reduzir o tempo e esforços necessários para armazenar os dados. Para isso, é necessário criar um bucket de armazenamento (diretamente da interface web do google cloud ou por linha de comando). O GCP oferece suporte a bancos de dados relacionais, não relacionais e armazenamento de outros tipos de objetos.   
Escolher a opção correta para armazenar e processar os dados depende do tipo de dado que precisa ser armazenado, como dados estruturados, não-estruturados, etc.

Dados não estruturados são armazenados de forma não tabular, que podem ser músicas, filmes, vídeos, documentos — e um serviço adequado para esse tipo de dados é o **Cloud Storage** — que tem 4 classes de armazenamento primárias:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1738580332103/95374b84-627b-454b-966a-c42c7d7ceaae.png)

1.  **Standard Storage**  
    É o armazenamento padrão. É frequentemente usado para dados que serão acessados com frequência, ou também pode ser utilizado para dados que estão ou serão armazenados por breves períodos de tempo.
2.  **Nearline Storage**  
    Frequentemente usado para armazenar dados acessados com pouca frequência, dados que são acessados, lidos ou modificados em média uma vez por mês, como backups.
3.  **Coldline Storage**  
    Destina-se a dados que serão lidos ou modificados no máximo a cada 90 dias.
4.  **Archive Storage**   
    É a opção mais barata, usada para armazenar dados que você planeja acessar pelo menos uma vez por ano.

Os dados estruturados têm dois tipos de cargas de trabalho: transacionais e analíticas. Dados transacionais são processamentos online que são usados quando inserções e atualizações de dados rápidos são necessários para criar registros em tabelas. Em contrapartida, os dados analíticos são necessários quando um conjunto de dados inteiros precisam ser lidos, modificados e exigem consultas complexas, como por exemplo agregações SQL. Depois de determinar se as cargas serão transacionais ou analíticas, você deverá escolher o melhor sistema para usá-las.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1738580333931/925bed4f-65ef-4602-a24e-71b377227218.png)

Se os seus workloads de dados são transacionais e você precisa utilizar SQL, as melhores opções são o **Cloud SQL** e o **SQL Spanner**, sendo que o Cloud SQL funciona melhor para escalabilidade local, enquanto o Cloud Spanner trabalha melhor em dimensionar um banco de dados globalmente. E se o conjunto de dados for acessado sem SQL, a opção é o **Firestore**, um banco de dados NoSQL transacional orientado a documentos.

Se os seus workloads de dados são analíticos e você precisa usar SQL, a melhor opção é o **BigQuery**, que é propriamente um Data Warehouse, pois ele suporta analisar conjuntos de dados em escalas de até petabytes. Já se o SQL não for necessário, a melhor opção é o **Cloud BigTable** que é melhor para aplicativos de taxa de transferência em tempo real e que exigem latência de milissegundos.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1738580335359/b42f9eb3-816b-48c5-a218-f86d7842c6ad.png)