# Flex-box

Estudo sobre o flex-box 

## Display

## flex-direction
[row (default) / row-reverse / column / column-reverse ]
Controla a posição e a direção dos eixos

## Como alinhar os elementos
Quando colocamos um texto diretamente estamos criando um **flex-item** anonimamente

primeiro que a propriedade `display` não é herdada pelos filhos, então tem que colocar uma nova propriedade `flex` no filho para poder manipular os seus os elementos

`justify-content`: center | flex-start (default) | flex-end | space-between | space-around

serve para distribuir os elementos filhos ao eixo principal (main axis)

- center: centraliza elemento
- flex-start: deixa alinhado a esquerda ou ao topo dependo se a propriedade flex-direction for row ou column
- flex-end: o inverso-do flex-start
- space-between: distribui os espaços entre os elementos por igual
- space-around: distribui os espaços ao redor dos elementos por igual

`align-items`: center | flex-start | flex-end | baseline | stretch (default)

serve para distribuir os elementos filhos ao eixo secundario (cross axis)

- stretch: estica todo o tamanho pelo espaço disponível do container-flex
- center: elementro centraliza pelo eixo secundario do container-flex
- flex-end: alinha ao final do eixo
- flex-start: alinha ao inicio do eixo
- baseline: alinha os elementos filhos do container a uma linha na base dos elementos

`align-self`: sobreescreve os valores de align-items para um unico elemento

##
