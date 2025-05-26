## Projeto de Coleta e Análises de Dados da API da Marvel

Este projeto realiza a coleta, tratamento e armazenagem de dados sobre quadrinhos, personagens e eventos do Universo Marvel.

Estes dados são fornecidos pela Marvel a partir da API do desenvolvedor. © 2014 Marvel

Para mais informações, visite o [Marvel Developer Portal](https://developer.marvel.com/).

## Tecnologias Utilizadas

O projeto foi desenvolvido em linguagem Python através do Google Colab. Foi utilizada a biblioteca pandas para manipulação dos dados, SQLite3 para armazenagem em banco de dados e a biblioteca Matplotlib para criação de gráficos exibindo os resultados das análises

## Autenticação na API

Para utilizar a API da Marvel, é necessário autenticar as requisições usando três parâmetros:

- `ts` (timestamp)
- `apikey` (sua chave pública)
- `hash` (MD5 gerado com: `ts + privateKey + publicKey`)

Esses parâmetros são incluídos na URL da requisição para garantir acesso autorizado à API

A autenticação foi configurada no projeto de forma que a chave de acesso não fique disponível no código. Para isso, usamos a biblioteca Userdata através do google colab para acessar a chave pelas variáveis de ambiente do projeto. Assim, para executar o código, é necessário que o usuário insira sua chave de acesso nas variáveis de ambiente.

## Armazenamento dos Dados

As requisições foram realizadas nos endpoints  **`/comics`, `/characters` e `/events`. 
Os dados obtidos no formato JSON foram carregados em dataframes utilizando a biblioteca **Pandas**. Após limpeza e padronização, foram inseridos em um banco de dados Relacional usando SQLite3, respeitando as formas normais.

## Análise dos Dados e Apresentação

Por fim, foram feitas análises em cima dos dados coletados para encontrarmos insights a respeito dos quadrinhos, popularidade dos personagens, eventos importantes para a marca, etc. Estes insights são apresentados no Python Notebook por meio de gráficos e explicações do processo de análise.
