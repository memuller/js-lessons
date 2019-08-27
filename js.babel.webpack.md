# Babel

## Transpilador
São programas que transformam código em outro código. Contraste com compiladores que transformam código em instruções de execução.

## Compatibilidade
Babel converte código recente em JS para JS mais "antigo" e consequentemente compatível com mais navegadores/ambientes de execução.

Permite usar recursos novos do Javascript sem se preocupar com eles serem compatíveis com cada ambiente. Compare com Python 2.7/3

## Usando Babel

Vai depender da ferramenta de build (Gulp, Webpack, Browserify, Parcel)
É possivel usar diretamente via CLI mas quase nunca vai ser relevante

## Dialetos
Como babel vai converter seu código para javascript compatível de qualquer jeito, nada impede que você escreva o código com melhorias arbitrárias na sintaxe, desde que exista um plugin do Babel para interpretar esta sintaxe.

Existem várias melhorias (proposals) que podem ser utilizadas desta forma.

Existem também dialetos (Typescript e Flow) que introduzem sintaxes completamente diferentes.

## Polyfill
Implementação "manual" de uma funcionalidade que você deseja e não sabe se vai estar presente.

Existe em outras linguagens também, principalmente se ela não tiver um transpilador como o Babel pois daí este vai ser o seu unico jeito de lidar com features novas.

Na prática:
1) você testa se uma função desejada existe
2) se não existir, você implementa ela "na mão"


# Webpack

## Pacotes
Pega todo o seu código e das suas dependências e gera um "pacote", que um JS só com todo este código.

Vantajoso pois permite que o seu aplicativo seja um arquivo só para ser consumido por navegador/Node.

### Implementação

Webpack vai pegar todos os requires e imports e substituir pelo código relevante

## Transformações

Parecem com o Babel; permitem uso de linguagens diferentes resultar em CSS/JS, ou transformações e imagens etc

eg.
```javascript
import imagem from './image.png' // webpack vai pegar a imagem, ler, converter os bytes em string, colocar dentro de uma data-url(), etc...

import './App.css' // webpack vai ler o arquivo, converter em string, criar uma tag <rel> style, etc
```

# Dependências

No package.json, podem ser especificadas _dependencies_ e _devDependencies_. Somente as _dependencies_ serão instaladas pelo usuário final (gente que der require da sua biblioteca, ou o navegador executando o aplicativo); as devDependencies são coisas para o seu uso como desenvovledor (webpack, babel, ambiente de testes, transformadores de código, plugins do babel)

Geralmente o Babel e Webpack não estarão inclusos como dependências.