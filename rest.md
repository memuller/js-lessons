## REST

É uma forma de arquitetura de aplicativos (tanto pra usuário final quanto de APIs) baseada no conceito de RECURSOS e VERBOS HTTP.

REST é uma forma de arquitear um aplicativo/API de forma a deixar clara a estrutura de dados dela, e deixar óbvio como manipular estes dados.

Dada uma URI e um request com um verbo, fica claro a natureza da operação desejada na solicitação.

Várias frameworks usam REST por padrão (Django, Rails, Laravel), e tende a ser o jeito mais intutivo e natural de montrar e acessar APIs.



## Recursos
Uma entidade representada por uma URL única (URI, Unique Resource Identifier).



## Hierarquia

Presume-se que as URLs vão estar organizadas de forma hierárquica refletindo a estrutura dos dados do aplicativo.

/products/
/products/id-do-produto
/category/
/category/id-category

/products/id-do-produto/variations/cor-do-produto


## Verbos HTTP

HTTP 1.1 possuem VERBOS diferentes que especificam quais ações devem ser feitas quando uma URL é solicitada.

### GET
Padrão, acessar/ler um recurso.


### POST
Alterar um recurso com dados presentes na solicitação


### PUT
Adiciona os dados presentes ao recurso; geralmente usada para criar um novo recurso.

eg. criando um novo produto
PUT /products/
ou
POST /products?action=create

Nem sempre presente, neste caso usa-se o POST

### DELETE
Exclui o recurso especificado

Nem sempre presente, caso ausente usa-se o POST (passando uma variável adicional)

POST /products/cardigan-verde?action=delete

### CRUD
Create, Read, Update, Delete: cada ação possível com uma entidade de dados é representada por um verbo HTTP.


## Alternativas
XML-RPC, SOAP, GraphQL, Sockets