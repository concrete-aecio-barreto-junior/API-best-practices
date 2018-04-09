
__[Concrete Solutions](http://www.concretesolutions.com.br) | DevOps - OnBoarding__

# **Trello (Card):** API - Write a text about the best practices when creating a API

# API - Melhores práticas

Centenas de milhares API's públicas e privadas respondem a infinitas possibilidades na web não restando assim dúvidas sobre o fundamental papel da API's durante a transformação digital. Para o desenvolvimento de API eficientes em suas propostas, a adoção de melhores praticas para o seu desenvolvimento é imprescindível.

Construir API's flexíveis e escaláveis tem sido uma tarefa árdua mediante a demanda e mediante também a infinidade de frameworks disponíveis. Embora muitos dos frameworks sejam projetados de maneira coerente com as melhores praticas, estas são negligenciadas por muitos desenvolvedores em detrimento a emergente demanda pelo desenvolvimento da API.

Literaturas extensas comumente são classificadas como [TL;DR](https://en.wikipedia.org/wiki/TL;DR). Para tanto, segue uma compilação de boas práticas obtida da internet.

## Boas práticas

### Planejamento da API

Antes de começar a construir sua API é vital a compreensão dos aspectos a nível de negócio e qual o propósito da API. Deve ser bem esclarecido sobre quais métodos deverão ser construídos, assim como também como serão utilizadas e por quem.

Essa compreensão irá garantir que o desenvolvimento seja feito sobre medida e com as tecnologias adequadas.

Após compreender o porque da API, é importante elencar e reunir os artefatos, como user stories, que descrevam detalhadamente as funcionalidades requeridas pelo cliente, que pode ser envolvido nesse momento descrevendo assim as funcionalidades necessárias e suas repectivas prioridades, de modo agilista inclusive.

### Definição do tipo da API

Quanto ao tipo de API deverá ser adotado, muito dependerá das necessidades do cliente, conforme comentadas no parágrafo anterior. Dentre tipos comuns de API temos a RESTful, a SOAP, e até mesmo a JSON-RPC. Embora cada uma tenha suas peculiaridades e diferentes aplicabilidades, a REST possuí "padrões" bem definidos e características que fazem dela um dos tipos de API's amplamente adotado.

### Considerações sobre tempo de vida e versionamento

API's devem ser construídas de maneira a serem extensíveis e sobre padrões e principalmente para serem duráveis. Por seguirem padrões requerem a manutenção constante dela de maneira a otimizar e ampliar suas funcionalidades. O esforço investido na API deve ser focado na extensão das possibilidades e otimização dela e não em correção de bugs. Isto irá garantir que ela cumpra seu papel com eficácia e atenda aos objetivos do cliente sobretudo durante seu ciclo de vida.

Para o devido lançamento de melhorias, extensões e/ou correções deve-se adotar a estratégia de versionamento. O versionamento é a garantia de um melhor gerenciamento de suporte e manutenção, principalmente quando se tem em produção níveis diferentes em seus clientes. Além da garantia de transições controladas entre atualizações e migrações.

Um grande desafio, durante o ciclo de vida da API é lançar versões que consigam manter a compatibilidade entre os demais níveis ao mesmo tempo que atualizações sejam promovidas com o mínimo de impacto. Assim, este é o grande motivo que nos obriga a construir API's com foco no longo prazo de sua duração.

### Desenvolvimento baseado em especificações

A definição da API quando realizada durante o seu desenvolvimento pode tornar a construção mais rápida inicialmente, porém inconsistente durante o decorrer da fase de codificação. Para garantir então o desenvolvimento de uma API consistente e com padrões reutilizáveis existem especificações de modelagens como [RAML](https://raml.org/).

Quando o desenvolvimento é baseado em especificações, demais benefícios são garantidos, sobretudo, a rapidez, padronização e universalidade dos métodos, que serão facilmente implementados pelos demais desenvolvedores. Assim é necessário planejar, desenhar e especificar a API antes de construí-la.

### Representações de recursos

De acordo com o modelo de API adotado, os recursos devem ser representados de maneiras diferentes. No caso de um modelo REST, os recursos devem corresponder a substantivos, diferente de modelos como JSON-RPC que fazem uso de verbos, indicando ações. O verbo está diretamente ligado a uma ação geralmente.

Como boa prática a representação de recursos da API estes devem seguir o modelo adotado, sendo no plural, quando tratar-se de substantivos e, no singular, quando representarem ações específicas. Seguem exemplos de ambas abordagens:

- **JSON-RPC**:

```
/adicionarNovoEmpregado/
/atualizarEmpregado/
/deletarEmpregado/
/deletarTodosEmpregados/
```

 - **REST**:

```
/empregado/id/1
/pedido/
```

### CRUD

Da mesma maneira que uso do CRUD é amplamente utilizado independente da plataforma tecnológica, o uso deste modelo é mais uma boa prática recomendada para o desenvolvimento de API's eficientes.

Quanto ao modelo **REST** este apresenta total compatibilidade entre os verbos/métodos HTTP `POST`,`GET`,`PUT|PATCH`,`DELETE` e as operações CRUD `create`, `read`, `update`, `delete` respectivamente. Para uma adequada utilização dos verbos/métodos HTTP se faz necessário também um adequado tratamento dos "exit status", devento então haver coerência na implementação.

  * **POST**: O método `POST` é amplamente utilizado para criar novos recursos, havendo inclusive a possibilidade da criação de recursos subordinados durante uma mesma requisição. Ou seja, através deste método é possível fazer uma associação parental entre o recurso que está sendo criado com algum outro preexistente.

```
POST http://apiurl/empregado/54321/vendas/98765
```


  * **GET**: O método `GET` é utilizado para recuperar ou ler a representação de algum recurso. Como retorno será obtido um exit status que indicará o status do recurso requisitado, podendo ser 400 (NOT FOUND) ou 404 (BAD REQUES) ou 200 (OK), além de uma saída no formado JSON, XML ou outros.

```
GET http://apiurl/empregado/54321
GET http://api.url/empregado/5432/vendas
```

  * **PUT**: De maneira generalista o verbo `PUT` é utulizado para atualizar algum recurso através de um indentificador previamente conhecido. O `PUT` é também utilizado para criação de recursos quando a atributo chave não é definido pelo servidor, mas pelo requisitante.

```
PUT http://apiurl/empregado/54321/vendas/98765
```

  * **PATCH**: Similar ao `PUT`, o `PATCH` é utilizado para atualização "parcial" de algum atributo do recurso. Significa que não há necessidade de atualizar o item por completo.

```
PATCH http://apiurl/empregado/54321/vendas/98765
```

  * **DELETE**: Como o verbo sugere, o `DELETE` é útil para a exclusão de recursos e a eficácia de sua implementação, assim como os demais métodos, se dará pelo adequado tratamento dos códigos de retorno HTTP. Similar ao `POST` este verbo suporta a manipulação de recursos subordinados.

```
DELETE http://apiurl/empregado/54321
DELETE http://api.url/empregado/5432/vendas
```

### JSON

A adoção do padrão JSON como respostas, além da simplicidade e versatilidade, durante a implementação e utilização, garante também performance, baixo custo de rede e eficiência de armazenamento em cache. Estas vantagens colocam o JSON como um padrão diferenciado frente a demais modelos como XML, css, html e até mesmo JavaScript.

Tendencias indicam que o XML tem perdido espaço p/ o JSON:

![Comparsion](https://github.com/concrete-aecio-barreto-junior/API-best-practices/blob/master/images/comparsion.png "Comparsion")
[Comparação xml x json api's (Google Trends)](https://trends.google.com/trends/explore?date=all&q=xml%20api,json%20api)

### Content-Type Header

Construir uma API pensando em garantir flexibilidade e extensibilidade requer que esta seja capaz de lidar com diversos tipos de mensagens, principalmente quando se tem tipos de conteúdos emergentes e concorrentes como `JSON` e `YAML`, ganhando mercado sobre outros que estão se tornando obsoletos. Como exemplo o `XML`, que além de muito verboso e redundante, tem um custo maior de processamento e transmissão.

Mediante a tantas possibilidades de conteúdos, a flexibilidade e extensibilidade apenas são obtidas quando a API consegue dialogar com cliente conforme o padrão requisitado por ele. Para então responder no mesmo formado requisitado é imprescindível utilizar o header "Content-type", responsável determinar o idioma. Uma API que suporta padrões de conteúdos diversos e responde no mesmo "idioma" requisitado se mostra ser flexível e de acordo com boas práticas.

### Tratamento adequado dos status de retorno HTTP (exit status)

O protocolo HTTP dispõe de um incrível pool de exit status quais devem garantir precisão nas respostas as requisições feitas a API, sobretudo, no modelo REST, que realiza as operações de CRUD através dos métodos HTTP.  O adequado uso das saídas garantirá um dialogo perfeito entre a API e a aplicação requisitante, o que assegurará maior controle das operaçÕes nas mãos dos desenvolvedores.

Os exit status garante o status de resposta as operações CRUD requisitadas. Seguem exemplos:

| Método | CRUD            | Exit Status                                    |
|:------:|:---------------:|------------------------------------------------|
| POST   | CREATE          | 201 (created), 404 (not found), 409 (conflict) |
| GET    | READ            | 200 (ok), 404 (not found)                      |
| PUT    | UPDATE/REPLACE  | 405 (not allowed), 200 (ok), 204 (not found)   |
| PATCH  | UPDATE/MODIFY   | 405 (not allowed), 200 (ok), 204 (not found)   |
| DELETE | DELETE          | 405 (not allowed), 200 (ok), 204 (not found)   |

### Filtering, sorting, field selection and paging



### Segurança: Uso do SSL

A segurança da API é mais um aspecto que deve ser considerado criteriosamente independente dela lidar com dados sensíveis. Uma boa prática é fazer uso do SSL, pois este protocolo garante a segurança dos dados enquanto transmitidos através das redes.

O SSL representa uma dos mais importantes artifícios de segurança da web na atualidade por garantir, dente outros aspectos, a autenticidade, integridade e confidencialidade dos dados enquanto transmitidos.

Deve ser considerado que uso o SSL "apenas" não irá garantir a segurança plena da API. Demais artifícios e práticas de "hardening", no código e na infraestrutura (middleware), devem ser aplicados de maneira a mitigar ao máximo os risco e vulnerabilidades de segurança antes da publicação da API.

### HATEOAS

### Caching

### Documentação

## Glossário

### API:

`"Application Programming Interface - API"`: Como o próprio acrônimo sugere trata-se de uma interface destinada a interoperabilidade entre sistemas híbridos. Através de API's uma linguagem comum é assegurada para comunicação entre aplicações de diferentes tipos de plataformas tecnológicas. A "API" é uma dentre tantas outras protagonistas responsáveis pela Transformação digital. Ela cumpre papel importante no mercado digital.

Ela fornece uma camada de abstração entre sistemas de maneira a garantir a portabilidade do código p/ diversas linguagens.

### RESTful:

Dentre tipos de API destacamos a REST = "REpresentational State Transfer". Sua principal característica é não precisar manter informações de estado do cliente, sendo então uma API stateless. Esta caraterística assegura ser uma API leve, pois todas as informações necessárias p/ serem processadas pelo servidor estarão contidas na requisição feita pelo cliente.

Diferente da SOAP, (que funciona através de métodos invocados diretamente através de URI's publicadas como verbos que indicam ações), a RESTful obtém/submete (request/response) representações de dados através de métodos/verbos HTTP (GET, PUT, POST, DELETE) p/ operações equivalentes ao CRUD.

As representações de dados são muitas vezes em formatos xml, html, rss e muitas vezes JSON e até JavaScript widgets a serem processados pelo cliente.

Alguns dos benefícios de se usar uma API rest são: performance, escalabilidade, simplicidade, flexibilidade, visibilidade, portabilidade e confiabilidade.

Destacamos duas das vantagens: `"performance"` e a `"escalabilidade"`. `"Performance"`, pois ela garante mínimo custo p/ o servidor pois no método http invocado estarão contidas todas as informações necessárias.  `"Escalabilidade"` pois, uma vez sendo "stateless", não há necessidade de propagar as sessões entre servidores.

## links úteis
- http://www.restapitutorial.com/lessons/httpmethods.html
- https://www.sslshopper.com/why-ssl-the-purpose-of-using-ssl-certificates.html
- https://phraseapp.com/blog/posts/best-practice-10-design-tips-for-apis/
- https://trends.google.com/trends/explore?date=all&q=xml%20api,json%20api
- https://youtu.be/llpr5924N7E - Todd Frederick Intro to REST (aka. What Is REST Anyway?)
- http://www.restapitutorial.com/
- http://www.ics.uci.edu/~fielding/pubs/dissertation/rest_arch_style.htm
- http://jsonapi.org/
- https://raml.org/
