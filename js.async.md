# Assincronicidade em JS: Três abordagens

## Eventos
Nativo navegador

listener ouvir eventos
eventos são disparados quando algyuma coisa específica acontece
e você pode ouvir estes eventos e executar funções quando eles acontecerem
funções são CALLBACKS

### Pró
* ele pode lidar com eventos diferentes em um listener só


## Abordagem baseada em Callbacks
Nativo do Node

Padrão do Node de funções assíncronas elas recebem um últmo parâmetro que é um callback para ser chamado quando elas retornarem.

fs.open('./test.txt', function(){

})


## Promises
Nativo do ES6/ES2015
.then()


async/await: única coisa aqui que não tem callbacks, deixa o código com uma ilusão de execuçao linear



### Calbacks
São funções para serem executadas posteriormente; geralmente quando um EVENTO acontecer
Linguagens de scripts e com funções anônimas usam muito callback

