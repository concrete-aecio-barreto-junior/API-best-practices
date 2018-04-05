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

A definição da API durante seu desenvolvimento pode tornar a construção mais rápida inicialmente, porém inconsistente durante o decorrer da fase de codificação. Para garantir então que voce desenvolva uma API consistente e com padrões reutilizáveis existem especificações de modelagens como RAML.

Quando o desenvolvimento é baseado em especificações demais benefícios são garantidos sobretudo a rapidez, padronização e universalidade dos métodos, que serão facilmente implementados pelos desenvolvedores. Assim é necessário planejar, desenhar e especificar a API antes de construí-la.

## Representações de recursos

Conforme o modelo de API utilizado os recursos devem ser representados de maneiras diferentes. No caso de um modelo REST os recursos devem corresponder a substantivos, diferente de modelos como JSON-RPC que fazem uso de verbos, indicando ações.

O verbo está diretamente ligado a uma ação geralmente

Seguem ambos exemplos:

- JSON-RPC:

/adicionarNovoEmpregado/
/atualizarEmpregado/
/deletarEmpregado/
/deletarTodosEmpregados/

 - REST:
/empregado/id/1
/pedido/

Como boa prática a representação de recursos devem seguir o modelo da API sendo no plural, quando tratar-se de substantivos e, no singular quando representarem ações específicas.

## CRUD

Da mesma maneira que uso do CRUD é amplamente utilizado independente da plataforma tecnológica o uso deste modelo é mais uma boa prática recomendada para o desenvolvimento de API's eficientes.

Quanto ao modelo REST, este apresenta total compatibilidade entre os `verbos/métodos: HTTP (POST,GET,PUT|PATCH,DELETE)` e as operaçÕes `CRUD (create, read, update, delete)` respectivamente.

## JSON

A adoção do padrão JSON como respostas além da simplicidade e versatilidade, durante a implementação e utilização, garante também performance, baixo custo de rede e eficiência de armazenamento em cache. Estas vantagens colocam o JSON como um padrão diferenciado frente a demais modelos como XML, css, html e até mesmo JavaScript.

Fazer uso deste padrão sempre que possível é aplicar mais uma boa pratica.

## Content-Type Header

Construir uma API pensando em garantir flexibilidade e extensibilidade requer que esta seja capaz de lidar com diversos tipos de mensagens, principalmente quando se tem tipos de conteúdos emergentes e concorrentes como JSON e YAML, ganhando mercado sobre outros que estão se tornando obsoletos. Como exemplo o XML, que além de muito verboso e redundante, tem um custo maior de processamento e transmissão.

Tendencias indicam que o XML tem perdido espaço p/ o JSON: https://trends.google.com/trends/explore?date=all&q=xml%20api,json%20api

Mediante a tantas possibilidades de conteúdos, a flexibilidade e extensibilidade apenas são obtidas quando a API consegue dialogar com cliente conforme o padrão requisitado por ele. Para então responder no mesmo formado requisitado é imprescindível utilizar o header "Content-type", responsável determinar o idioma. Uma API que suporta padrões de conteúdos diversos e responde no mesmo "idioma" requisitado se mostra ser flexível e de acordo com boas práticas.


## HTTP exit status correctly

O protocolo HTTP dispõe de um incrível pool de exit status quais devem garantir precisão nas respostas as requisições. O adequado uso das saídas garantirá um dialogo perfeito entre a API e a aplicação requisitante, o que assegurará maior controle das operaçÕes nas mãos dos desenvolvedores.

Os exit status garante o status de resposta as operações CRUD requisitadas. Seguem exemplos:

## filtering, sorting, field selection and paging



## SSL

A segurança da API é mais um aspecto que deve ser considerado criteriosamente independente dela lidar com dados sensíveis. Uma boa prática é fazer uso do SSL, pois este protocolo garante a segurança dos dados enquanto transmitidos através das redes.

O SSL representa uma dos mais importantes artifícios de segurança da segurança da web na atualidade por garantir, dente outros aspectos, a autenticidade, integridade e confidencialidade dos dados enquanto transmitidos.

Sabendo que não há segurança perfeita, entenda que uso o SSL "apenas" não irá garantir a segurança suficiente a API. Riscos não

## HATEOAS



## Caching

## Forneça documentação

## links úteis
- https://www.sslshopper.com/why-ssl-the-purpose-of-using-ssl-certificates.html
- https://phraseapp.com/blog/posts/best-practice-10-design-tips-for-apis/
- https://trends.google.com/trends/explore?date=all&q=xml%20api,json%20api
- https://youtu.be/llpr5924N7E - Todd Frederick Intro to REST (aka. What Is REST Anyway?)
- http://www.restapitutorial.com/
- http://www.ics.uci.edu/~fielding/pubs/dissertation/rest_arch_style.htm
- http://jsonapi.org/
- https://raml.org/
