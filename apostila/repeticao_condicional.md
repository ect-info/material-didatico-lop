# Repetição Condicional

As estruturas de repetição desempenham um papel crucial na programação quando há a necessidade de executar repetidamente uma mesma sequência de instruções. Em linguagens de programação como JavaScript, temos várias estruturas de repetição à disposição, cada uma com suas próprias características e usos específicos: o **while**, o **do-while** e o **for**. As diferentes estruturas de repetição são semanticamente equivalentes. 
 
O **while** é uma estrutura de repetição que repete um bloco de código enquanto uma condição especificada for verdadeira. Isso significa que o bloco de código dentro do **while** é executado repetidamente enquanto a condição definida for avaliada como verdadeira.

Sintaxe:
```javascript
//Enquanto a condição for verdadeira, execute as instruções.
while ( condição ) {
   // instruções 
}
```

Exemplo de uso do while em JavaScript:
```javascript
let contador = 0;
while (contador < 5) {
    console.log("O contador é: " + contador);
    contador++;
}
```




Sintaxe:
```javascript
do {
   // instruções 
} while ( condição );
```
" Faça as instruções, Enquanto a condição for verdadeira."

## Exemplos 

Execute passo a passo os códigos a seguir: 

Repetição simples: 
```javascript
var x = 10
var y = 40 
while ( x > 3 ) {
   x = y / 3 
   y = x + 2 
}
```
Ver vídeo com este exemplo: https://youtu.be/iAyJvXtGHDs

Repetição com *loop* infinito: 
```javascript
var x = 9
var y = 12 
while ( x > 3 ) {
   x = y - 8 
   y = x * 3 
}
```
Ver vídeo com este exemplo:  https://youtu.be/5nabBOi0rgg

## Exemplos 

**(Exemplo 1)** Implemente um programa que receba a idade de várias pessoas e informa se cada um delas é menor de idade ou idosa. Para encerrar, o usuário deve digitar a idade -1. 

Em problemas de repetição, é preciso os comandos a serem repetidos. Nesta questão as seguintes ações devem ser ressaltadas: 
* Receber a idade da pessoa
* Verificar se a idade é diferente de -1 (condição de parada)
* Avisar se é menor de idade ou idosa

Reflexões importantes: 
* Quais as entradas do programa?
  * Idade de uma  pessoa
* Quais as saídas?
  * Para cada pessoa, “Menor de idade”, “Idosa” ou sem saída.
* O que deve ser repetido?
  * Verificar se a idade é diferente de -1
    * Avisa se é menor de idade ou idosa
  * Receber a idade
* Como controlar as repetições?
  * Valor da idade. Se for -1, o programa deve encerrar  (condição de parada)

```javascript
   var idade = parseInt(prompt("Entre com a idade: "))
   while ( idade !== -1 ){
      if ( idade > 60 ){
         alert("idoso")
      }
      if ( idade < 18 ){
         alert("menor de idade") 
      }
      idade = parseInt(prompt("Entre com a idade: "))
   }
``` 

**(Exemplo 2)** Implemente um programa que recebe as 3 notas de vários alunos e escreve a média parcial de cada um deles até o usuário digitar -1 para a primeira nota.

Reflexões importantes: 
* Quais as entradas do programa?
  * 3 notas de uma quantidade indefinida de alunos
* Quais as saídas?
  * Média parcial dos alunos
* O que deve ser repetido?
  * A leitura das 3 notas
  * O cálculo e a escrita da média parcial
* Como controlar as repetições?
  * Valor da primeira nota. Se for -1, o programa deve encerrar  (condição de parada)

```javascript
   n1 = parseFloat(prompt("Entre com a nota 1"))
   while ( n1 != -1 ){
      n2 = parseFloat(prompt("Entre com a nota 2"))
      n3 = parseFloat(prompt("Entre com a nota 3"))
      media = (n1 + n2 + n3)/3
      alert(media) 
      n1 = parseFloat(prompt("Entre com a nota 1")) 
   }
```


**(Exemplo 3)** Implemente um programa que mostra todos os números de 0 à 100. 

```javascript
x = 0
while ( x <= 100 ) {
    console.log(x)
    x++ 
}
```

## Aplicações 

### Repetição Simples 

Em uma repetição simples, resolvemos um problema específico repetidas vezes
* Identificar o que vai ser repetido
* Identificar quando parar 

**(Questão 1)** Escreva um programa que recebe e calcula o quadrado de vários números. O programa se encerra quando o usuário digitar 0 (zero).

* O que deve ser repetido?
  * Receber número
  * Calcular e imprimir seu quadrado 
* Quando iremos parar? 
  * Quando o programa receber 0 (comando de parada)
    * Logo, enquanto não for 0, o programa deve repetir

Exemplo de solução: 
```javascript
var x = parseFloat(prompt("Entre com um número: "))
while ( x != 0 ){
  var quadrado = Math.pow(x,2) 
  alert(quadrado) 
  x = parseFloat(prompt("Entre com um número: "))
}
``` 

### Validação de dados

O objetivo da validação de dados é garantir que as informações dadas pelo usuário são aceitáveis.
* Enquanto não forem válidas, o programa pede para o usuário digitar novamente

**(Questão 2)** Implemente um programa que lê um número inteiro referente a um dia do mês de setembro. O programa deve verificar se o valor é válido. Se não for, deve apresentar a mensagem “Dia inválido. Tente novamente.” e então receber outro número. O programa só para quando for digitado um dia válido.

* Quais entradas são válidas
  * Números inteiros no intervalo 1 <= dia <= 30 
* E quais são inválidas? 
  * Qualquer número fora do intervalo

Exemplo de solução: 
```javascript
var dia = parseInt(prompt("Entre com o dia: "))
while (dia < 1 || dia > 30 ) {  // dia inválido  
   dia = parseInt(prompt("Dia inválido. Tente novamente: "))
}
```
### Contagem 

Uma contagem visa verificar quantas vezes determinado fenômeno ocorre.

**(Questão 3)** Implemente um programa para receber vários números inteiros e contar quantos são múltiplos de 3 ou de 7. O programa deve encerrar quando receber o número 0.

Para resolver problemas de contagem, devemos identificar:
* Quais os elementos? 
* Qual o fenômeno em observação?
* Como verificar se o fenômeno ocorre em cada elemento?

Exemplo de solução: 
```javascript
 var n = parseInt(prompt("Entre com um número: "))
 var contador = 0 
 while ( n != 0 ) {
     if ( n % 3 == 0 || n % 7 == 0 ) {
         contador = contador + 1 
     }
     n = parseInt(prompt("Entre com um novo número: "))
 }
 alert(contador)
```

## Exercícios 


Implemente um programa que recebe números inteiros positivos como entrada e para quando o número recebido for 22. O seu programa deve escrever todos os números recebidos, com exceção do 22, separados por espaços. O espaço no final da saída é opcional.

```javascript
var x = parseFloat(prompt("Entre com um número: "));
while(x != 22) {
    alert(x+" "); 
    x = parseFloat(prompt("Entre com um número: "));
}
```

Faça um programa que lê a idade de 6 pessoas e diz quantas delas são maiores de 18 anos! Nesse programa você vai precisar criar um segundo contador! O programa precisa de um contador para contar quantas vezes o programa vai repetir. Independente disso, ele vai precisar de um segundo contador para contar quantas vezes foi encontrada uma pessoa com mais de 18 neste grupo. São dois contadores diferentes e portanto duas várias distintas.  


```javascript
cont = 0
contIdade = 0
while ( cont < 6 ){ 
    idade = parseInt(prompt("Entre com a idade: ")) 
    if (idade > 18 ){
        contIdade++ 
    }
    cont++ 
}
alert(contIdade)
```

Faça um programa que leia vários inteiros positivos e mostre, no final, a soma dosnúmeros pares e a soma dos números ímpares. O programa para quando entrar umnúmero maior que 1000.

```javascript
somaPar = 0 
somaImpar = 0 
n = parseInt(prompt("Entre com um número: "))
while (n <= 1000){
    if (n%2===0){
        somaPar = somaPar + n 
    }
    else {
        somaImpar = somaImpar + n 
    }
    n = parseInt(prompt("Entre com um número: "))
}
alert("Soma dos numeros pares: "+somaPar+"\nSoma dos numeros impares: "+somaImpar)
```



