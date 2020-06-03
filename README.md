# O projeto
Projeto de tcc que tem por objetivo realizar o estudo da linguagem Python e suas
bibliotecas de raspagem de dados na internet, em específico, de comentários públicos em sites
brasileiros de notícias, a fim de realizar a classificação dos dados capturados como ofensivos
ou não ofensivos, e se ofensivos, qual é a sua categoria (tipo de ofensa).

Para tal classificação, será implementado um sistema de contribuição colaborativa ou
coletiva, na qual diversos usuários visualizarão os comentários de forma aleatória e indicarão
se o comentário é ofensivo ou não, assim como sua categoria, quando necessário. Uma vez
capturado os dados, serão armazenados em um banco de dados NoSQL.
A partir dos dados inseridos no banco de dados, serão utilizadas bibliotecas de
PNL/Machine Learning da linguagem Python, onde técnicas estatísticas de tais bibliotecas
serão aplicadas nos dados armazenados de forma a treinar a máquina para que ela possa
futuramente identificar novos dados automaticamente se os mesmo são ofensivos.

## Estrutura
Root:
  -> ambiente (Pasta com ambientes para importação e instalação de dependecias)
  -> dados_scrap_converted (Pasta com dados capturados no webscrapping, trabalhos de transformações de csv, json, SQL, NoSQL)
  - convert_toscv_ibm_autoai.ipynb (Arquivo para python notebook, que converte o arquivo json de dados do banco NoSQL - Mongo - para csv que pode ser colocado na plataforma auto ai da IBM que fornece para nós as melhores opções de técnicas e modelos de ML)
  - generate_results_model_training.ipynb (Arquivo para python notebook, onde ocorre todo o trabalho de treinamento, modelagem, visualizações, tratamentos de dados do trabalho)
  - scrap_g1_front_page_json.ipynb (Arquivo para python notebook, onde é feita toda a parte de webscrapping do site g1.com.br)
  - arquivos .pkl são (Arquivos de modelagem)
  - dataset_for_modeling.ipynb (Arquivo para python notebook, realiza o tratamento do definedcommentsdf.json)
  - arquivos Tableau Workbook (Arquivos de workbook do Tableau, para visualização de dados)
  - csv_file_merge.ipynb (Automação de junção de arquivos .csv)

## Necessário para replicação

#### Replicação do machine learning
Anaconda 3, pip, python3.7.x
Dentro da pasta de ambiente, temos um enviroment_ml.yml para importação direta para o anaconda
Outros pacotes não trazidos pelo anaconda, necessita usar o pip install:
spacy
spacy.load("pt_core_news_sm") --> arquivo .rar no root do projeto
xgboost

#### Replicação do webscrapping
Anaconda 3, chromium para o selenium
Dentro da pasta de ambiente, temos um enviroment_wsc.yml para importação direta para o anaconda

##### !- Não foi replicado em linux ou em MacOs -!

## Contribua e entre em contato
Qualquer proposta de melhoria, façam um fork ou falem comigo aqui no github!

## Open Source
Os dados aqui são públicos, fiquem a vontade em usar!
