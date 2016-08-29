# Flex-box

Estudo sobre o flex-box

## Display

## flex-direction
[row (default) / row-reverse / column / column-reverse ]
Controla a posição e a direção dos eixos

## Como alinhar os elementos
Quando colocamos um texto diretamente estamos criando um **flex-item** anonimamente

primeiro que a propriedade `display` não é herdada pelos filhos, então tem que colocar uma nova propriedade `flex` no filho para poder manipular os seus os elementos

### justify-content
center | flex-start (default) | flex-end | space-between | space-around

serve para distribuir os elementos filhos ao eixo principal (main axis)

- center: centraliza elemento
- flex-start: deixa alinhado a esquerda ou ao topo dependo se a propriedade flex-direction for row ou column
- flex-end: o inverso-do flex-start
- space-between: distribui os espaços entre os elementos por igual
- space-around: distribui os espaços ao redor dos elementos por igual

### align-items
center | flex-start | flex-end | baseline | stretch (default)

serve para distribuir os elementos filhos ao eixo secundario (cross axis)

- stretch: estica todo o tamanho pelo espaço disponível do container-flex
- center: elementro centraliza pelo eixo secundario do container-flex
- flex-end: alinha ao final do eixo
- flex-start: alinha ao inicio do eixo
- baseline: alinha os elementos filhos do container a uma linha na base dos elementos

### align-self
 sobreescreve os valores de align-items para um unico elemento

## flex-itens
Quando não especificamos o `align-items` ele por padrão vem como `stretch` então quando mudamos e colocamos como `center` ou `flex-start` o elementeo vai pegar o tamanho do conteudo ao inves de esticar pelo total de tamanho disponível

MAIN SIZE -> MAIN AXIS (DEFAULT: WIDTH)
CROSS SIZE -> CROSS AXIS (DEFAULT: HEIGHT)

### flex-basis
funciona como `width` enquando o `flex-direction` esta como `row` mas quando é mudado para `column` então passa a ser `height` por causa da mudança dos eixos.

Quando utilizamos o f`lex-basis` o `width` perde o seu valor ou seja ele não funciona mas o `height` sim, mas isso se o `flex-direction` for `row`, caso seja `column` então o `height` que não funciona mas o `width` então funcionara

o valor padrão é auto;

### flex-grow
 utiliza um numero que é um fator de crescimento então ele pega o valor disponível e divide pela soma dos fatores de crescimento de todos os items.

Com isso podemos dividir o tamanho total dispoivel por igual dos entre os elementos. Muito mais prático e nem precisa de ficar dividindo utilizando calculadora.


### flex-shrink
é o oposto do flex-grow. E ele utiliza quando o espaço disponivel é negativo

### flex
é a propriedade agrupa as 3 anteriores na seguinte ordem: flex-grow, flex-shrink e flex-basis

caso precisamos utilzar as tres de uma vez ficaria assim:
```
flex: 1 1 100px;
```
é o mesmo que
```
flex-grow: 1;
flex-shrink: 1;
flex-basis: 100px;
```

o valor padrão é `flex: 0 1 auto;`

Lembrar que dependo do valor por vausa do `flex-basis` o width ou height dependendo do flex-direction não vai funcionar
