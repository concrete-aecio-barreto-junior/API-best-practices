# API - Melhores práticas p/ criação (segundo Dr Roy Fielding)

## O que é uma API?

`"Application Programming Interface - API"`: Como o próprio acrônimo sugere trata-se de uma interface destinada a interoperabilidade entre sistemas híbridos. Através de API's uma linguagem comum é assegurada para comunicação entre aplicações de diferentes tipos de plataformas tecnológicas. A "API" é uma dentre tantas outras protagonistas responsáveis pela Transformação digital. Ela cumpre papel importante no mercado digital.

Ela fornece uma camada de abstração entre sistemas de maneira a garantir a portabilidade do código p/ diversas linguagens.

## API Rest

Dentre tipos de API destacamos a REST = "REpresentational State Transfer". Sua principal característica é não precisar manter informações de estado do cliente, sendo então uma API stateless. Esta caraterística assegura ser uma API leve, pois todas as informações necessárias p/ serem processadas pelo servidor estarão contidas na requisição feita pelo cliente.

Diferente da SOAP, (que funciona através de métodos invocados diretamente através de URI's publicadas como verbos que indicam ações), a RESTful obtém/submete (request/response) representações de dados através de métodos/verbos HTTP (GET, PUT, POST, DELETE) p/ operações equivalentes ao CRUD.

As representações de dados são muitas vezes em formatos xml, html, rss e muitas vezes JSON e até JavaScript widgets a serem processados pelo cliente.

Alguns dos benefícios de se usar uma API rest são: performance, escalabilidade, simplicidade, flexibilidade, visibilidade, portabilidade e confiabilidade.

Destacamos duas das vantagens: `"performance"` e a `"escalabilidade"`. `"Performance"`, pois ela garante mínimo custo p/ o servidor pois no método http invocado estarão contidas todas as informações necessárias.  `"Escalabilidade"` pois, uma vez sendo "stateless", não há necessidade de propagar as sessões entre servidores.

## Constraints:

## Funcionamento

P/ o consumo de uma API rest

## Segurança



## Melhores práticas


Centenas de milhares API's públicas e privadas respondem a infinitas possibilidades na web. Dessa maneira não restam dúvidas sobre o fundamental papel da API durante a transformação digital. Para o desenvolvimento de API's que agreguem valor e que que sejam eficientes em suas propostas, é fundamental considerar e adotar melhores praticas para seu desenvolvimento.

Construir API's eficientes, flexíveis e escaláveis tem sido uma tarefa árdua mediante a demanda e mediante também a infinidade de frameworks disponíveis. Embora muitos dos frameworks sejam projetados de maneira coerente com as melhores praticas, estas são negligenciadas por muitos desenvolvedores em detrimento a emergente demanda pelo desenvolvimento da API.

Literaturas extensas comumente são mantidas TL;DR. Para tanto, seguem uma compilação de boas práticas obtidas de artigos

############################ INICIO DAS PRATICAS #########################

# Planejamento da API:
## Entender qual propósito da API:

Antes de começar a construir sua API é vital a compreensão dos aspectos a nível de negócio acerca da API. Deve ser bem esclarecido sobre quais métodos deverão ser construídos, assim como também como serão utilizadas e por quem.

Essa compreensão irá garantir que o desenvolvimento seja feito sobre medida p/ a necessidade. Desde a escolha da tecnologia adequada até XXXXX.

Após compreender o porque da API, é importante elencar e reunir os artefatos, como user stories, que descrevam detalhadamente as funcionalidades requeridas pelo cliente, que pode ser envolvido nesse momento descrevendo assim as funcionalidades necessárias e suas repectivas prioridades, de modo agilista inclusive.

## Definir o tipo da API

Quanto ao tipo de API deverá ser adotado, muito dependerá das necessidades do cliente, comentadas no parágrafo anterior. Dentre tipos comuns de API temos a RESTful, a SOAP, e até mesmo a JSON-RPC. Embora cada uma tenha sua peculiaridades e diferentes aplicabilidades, a REST possuí "padrões"  bem definidos e atuais. A REST apresenta diversas vantagens sobre as demais. Vide imagem.

## Long term

API's devem ser construídas de maneira a serem extensíveis e sobre padrões e principalmente para serem duráveis. Por seguirem padrões requerem a manutenção constante dela de maneira a otimizar, extentender suas funcionalidades. O esforço investido na API deve ser focado na extensão das possibilidades e otimização dela e não em correção de bugs. Isto irá garantir que ela atenda aos seus objetivos e do cliente sobretudo. Para o devido lançamento de melhorias, extensões e/ou correções deve-se adotar a estratégia de versionamento, boa prática esta que será melhor abordada adiante. Porém, em poucas palavras como vantagens do versionamento é a garantia de um melhor gerenciamento de suporte e manutenção, principalmente quando se tem níveis diferentes em seus clientes. Além de que garante transições controladas entre atualizações e migrações.

Um grande desafio, durante o ciclo de vida da API, é lancar versões que consigam manter a compatibilidade entre os níveis ao mesmo tempo que atualizações sejam promovidas. Assim, este é o grande motivo que nos obriga a construir API's com foco no logo prazo da sua duração.

## Desenvolva baseado em especificações

A definição da API durante seu desenvolvimento pode tornar a construção mais rápida inicialmente, porém inconsistente durante o decorrer da fase de codificação. Para garantir então que voce desenvolva uma API consistente e com padrões reutilizáveis existem especificações de modelagemns como RAML.

Quando o desenvolvimento é baseado em especificações demais benefícios são garantidos sobretudo a rapidez, padronização e universalidade dos métodos, que serão facilmente implementados pelos desenvolvedores. Assim é necessário planejar, desenhar e especificar a API antes de construí-la.

 


## links úteis
https://youtu.be/llpr5924N7E - Todd Frederick Intro to REST (aka. What Is REST Anyway?)
http://www.restapitutorial.com/
http://www.ics.uci.edu/~fielding/pubs/dissertation/rest_arch_style.htm
https://raml.org/
