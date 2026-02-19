# 📅 02-02    
📌 Aula 17 e 18

Revisei uns conteúdos da semana passada e pra ser mais especifico foram Lógicos AND e OR, que não é tão dificil. É mais lógica de pensamento.


📌 Aula 19

Foi sobre Atribuição, a forma como atribuir operadores é muito mais fácil doque ficar digitando e ao longo do tempo conforme eu for me familiarizando a tendência é eu melhorar isso.. 


EXEMPLO:
`
// = += -= *= /= %=
`


Eu poderia digitar por exemplo:

`
double bonus = 1800;
bonus = 1800 + 1000;
System.out.println(bonus);
`


MASS….


``
double bonus = 1800;
bonus += 1000;
System.out.println(bonus);
``


Fica muito mais fácil, muito mais organizado e prático, principalmente a longo prazo, imagine que eu tivesse que mudar o bonus toda hora, dessa forma a longo a prazo.
esse bonus (variavel), o espaço em memoria recebeu oque ele já tinha, mais mil.

📌 ATRIBUIÇÃO: 
```
int contador = 0;

contador += 1; // contador = contador +1

contador++;

contador--;

++contador;

--contador;

int contador2 = 0;

System.out.println(++contador2);
```
#  📅 03-02 

📌 Aula 20 -  Estruturas Condicionais PT01



``IF(true)`` - obrigatoriamente o resultado ou oque eu pôr dentro dos parenteses precisa ser true
IF só é executado se a condição de dentro do if ser true.
tem uma maneira de executar se for false que é fazendo comparação
ou usando ``!``


EXEMPLO:


```
public class Aula05EstruturasCondicionais {
public static void main(String[] args) {
int idade = 20;
boolean isAutorizadoComprarBebida = idade >= 18;

if (isAutorizadoComprarBebida) {         //     Aqui é verdadeira
System.out.println("Autorizado a comprar bebida alcóolica");
}

// !
if(isAutorizadoComprarBebida == false) {  // Aqui é false¹
System.out.println("Não Autorizado a comprar bebida alcóolica");
}
}

```
 ¹Se a idade fosse int idade = 17;  Executaria somente esse  porque o primeiro ali que é true não irá mostrar porque o resultado final seria abaixo dos 18.
Obs: esse `==false` poderia ser substituído no início da frase como:
if(!isAutorizadoComprarBebida);
usar ! (MELHOR prática ⭐)
Mais limpo e profissional.

if tem que voltar um booleano.

#  📅 06-02


📌 Aula 21 - Else:


```
if (isAutorizadoComprarBebida) {         //     Aqui é verdadeira
System.out.println("Autorizado a comprar bebida alcóolica");
}else {
System.out.println("Não autorizado a comprar bebida");

if(!isAutorizadoComprarBebida) {  // Aqui é false¹
System.out.println("Não Autorizado a comprar bebida alcóolica");
 }
```


A diferença de um false( ! ) pro outro( else ), é que else vai se basear na condição de if e ! sempre vai executar.

o else precisa de um if, não pode fazer aleatório(Tipo Romeo e Julieta)



Exercício que foi passado na aula:


```
public class Aula05EstruturaCondicionais02 {
public static void main(String[] args) {
// idade < 15 categoria infantil
// idade > 15 && idade < 18 categoria juvenil
// idade >= 18 categoria adulto
Eu Fiz dessa forma sozinho(Não tinha aprendido o else if):
int idade = 17;
if(idade < 15 ) {
System.out.println("Categoria infantil");
}if(idade < 18) {
System.out.println("Categoria juvenil");
}else {
System.out.println("Categoria adulto");
             }
      }
}

```
Como o DevDojo fez:


```
int idade = 17;
if(idade < 15 ) {
System.out.println("Categoria infantil");
}else if(idade >= 15 && idade < 18) {
System.out.println("Categoria juvenil");
}else {
System.out.println("Categoria adulto");
}
```



nesse ultimo else não precisa dizer explicitamente pro compilador que ele é maior de idade, pois senão é um e não é outro, obviamente vai oque sobrou que é a Categoria Adulto.

e teve uma maneira que ele fez que eu achei muito interessante:


```
package academy.devdojo.maratonajava.introducao;

public class Aula05EstruturaCondicionais02 {
public static void main(String[] args) {
// idade < 15 categoria infantil
// idade > 15 && idade < 18 categoria juvenil
// idade >= 18 categoria adulto
int idade = 17;
String categoria;

if(idade < 15 ) {
categoria = "Categoria infantil";
}else if(idade >= 15 && idade < 18) {
categoria = "Categoria juvenil";
}else {
categoria = "Categoria adulto";
}
System.out.println(categoria);
}
}
```

Ele criou uma string como categoria, e armazenou os valores tudo dentro dela, deixando p imprimir somente no fim, muito boa essa lógica



Hoje não estudei Java, mas estudei legal sobre Git :) isso que eu fui treinar ainda! amanha eu pego firme mas só pra deixar registrado aqui.

# 📅10-02

📌 Aula 22 - Estruturas Condicionais pt 03 - Operador ternário


Ele ainda passou mais uma atividade de if e else e eu fiz de uma maneira e ele fez de outra com o código muito mais limpo, vamos analisar:
veja como eu fiz para imprimir ⬇️
```
package academy.devdojo.maratonajava.introducao;

public class Aula05EstruturaCondicionais03 {
public static void main(String[] args) {
double salario = 6000;
String mensagemDoar = "Eu vou doar 500 pro DevDojo";
String mensagemNaoDoar = "Ainda não tenho condições, mas vou ter!";
if(salario > 5000){
system.out.println(mensagemDoar);
}else{
system.out.println(mensagemNaoDoar);
}
```

Agora veja do DevDojo ⬇️

```
package academy.devdojo.maratonajava.introducao;

public class Aula05EstruturaCondicionais03 {
public static void main(String[] args) {
double salario = 6000;
String mensagemDoar = "Eu vou doar 500 pro DevDojo";
String mensagemNaoDoar = "Ainda não tenho condições, mas vou ter!";
String resultado;
if(salario > 5000){
resultado = mensagemDoar;
}else{
resultado = mensagemNaoDoar;
}
System.out.println(resultado);
}
```

Veja como ficou bem mais logico, ele criou uma string com o nome resultado, e depois utilizou para armazenar o valor, e só no final que ele usa o system para imprimir somente a string

Agora vamos para o operadore ternário, aplicando o mesmo exercício:

```
package academy.devdojo.maratonajava.introducao;

public class Aula05EstruturaCondicionais03 {
public static void main(String[] args) {
double salario = 6000;
String mensagemDoar = "Eu vou doar 500 pro DevDojo";
String mensagemNaoDoar = "Ainda não tenho condições, mas vou ter!";
// (condicao) ? verdadeiro : falso
String resultado = (salario > 6000) ? mensagemDoar : mensagemNaoDoar;

System.out.println(resultado);
}
}
```

Aplicando com o operador ternário, acaba se tornando muito mais fácil, e muito mais bonito… limpo.
fórmula:
```
(condicao) = (salario > 6000) ?
verdadeiro = mensagemDoar
falso = mensagemNaoDoar
```

E tem uma forma MUITO mais limpa


```
package academy.devdojo.maratonajava.introducao;

public class Aula05EstruturaCondicionais03 {
public static void main(String[] args) {
double salario = 6000;
// (condicao) ? verdadeiro : falso

String resultado = salario > 6000 ? "Eu vou doar 500 pro DevDojo" : "Ainda não tenho condições, mas vou ter!";

System.out.println(resultado);
}
}
```


Hoje eu vi apenas essa aula, estava morto de sono mas mesmo assim não desisti.. vi uma informação no twitter e queria deixar registrado aqui:
<img width="430" height="709" alt="Repeticao" src="https://github.com/user-attachments/assets/3d4f2a0c-2e73-4401-8904-fdc1c943b376" />




📌 Aula 23 - Estruturas Condicionais pt 04


Tabela Verdade e exercício:


quando utilizar && será verdadeiro se tudo for Verdadeiro, se utlizar || será falso se tudo for falso e o todo resto for verdadeiro
<img width="815" height="387" alt="image" src="https://github.com/user-attachments/assets/408457d6-731b-4136-9aee-7bec5619aaa4" />


Ele passou uma atividade também, confesso que no começo eu me bati porque era pra mostrar uma coisa e acabei fazendo outra, era pra eu calcular o valor do imposto e coloquei pra mostrar a taxa que ele ia pagar… fiz totalmente errado, mas refiz e precisei que a IA me ajudasse a compreender oque eu fiz de errado, não deveria ter visto isso e sim ter me virado, mas não copiei o código inteiro, apenas para compreensão oque era pra fazer de fato..

resumindo: Tentei sozinho, errei a interpretação, refleti sobre o erro, busquei entender o conceito, refiz, não copiei..
Usei a IA para entender o problema e não para fazer pra mim

# 📅 12-02 

- Fiquei estudando Estruturas Condicionais, mais especificamente IF/Else, pedi pro chatgpt me mandar uns exercícios sobre, e ele me passou um que eu me bati bastante…

2️⃣ Desconto em produto
Um produto custa R$ 200.
Se o cliente pagar à vista → 10% de desconto

Se parcelar → sem desconto
Mostre o valor final a pagar.
⚠️ O problema quer o valor final, não a porcentagem.

me bati muito porque eu tava ja querendo solucionar o problema no começo com as variaveis.. mas aqui está a solução que eu fiz sozinho depois de 1hr tentando e pensando:


```

package Exercícios;

public class AquecimentoIfElse02 {
public static void main(String[] args) {
// Produto = R$ 200
// Cliente pagar à vista - 10% de desconto
// Se parcelar - sem desconto
//Mostre o valor final a pagar
double produto = 200;
double valorFinal;
int formaPagamento = 1;

if(formaPagamento == 1){
valorFinal = produto - (produto*0.10);
System.out.println(valorFinal);
}else {
valorFinal = produto;
System.out.println(valorFinal);
}

}
}
```


# 📅13-02

Estudei MUITO hoje, MUITO mesmo, peguei uma boa parte de lógica e entendimento sobre if/else
<img width="332" height="144" alt="image" src="https://github.com/user-attachments/assets/c9d82141-9221-4e59-b4bb-f07393f88a71" />



# 📅16-02


### 📌 Aula 25 - Estruturas Condicionais pt 06 - Switch

(estudando de madrugada que foi o único horário que consegui).

Entendi que *switch* é uma estrutura condicional usada quando queremos comparar uma variável com vários valores específicos.

1️⃣ Use switch quando:

Você está comparando uma única variável;<br>
Contra valores fixos;<br>
E existem várias possibilidades;<br>


Exemplo clássico:

````
switch (dia) {
    case 1:
        System.out.println("Domingo");
        break;
    case 2:
        System.out.println("Segunda");
        break;
}
````

3️⃣ Por que ele é melhor que vários if?

Imagine isso com if:
````
if (dia == 1) {
} else if (dia == 2) {
} else if (dia == 3) {
}
````

Funciona igual.

Mas o switch:

✔ Fica mais organizado<br>
✔ Fica mais legível<br>
✔ Mostra claramente que estamos comparando um único valor<br>

🔥 Agora a parte importante

Switch não substitui todos os ifs.

Você NÃO pode fazer:

````
switch (idade > 18)
````

Isso não funciona.



2️⃣ Switch só funciona com:

int;<br>
byte;<br>
short;<br>
char;<br>
String;<br>
enum;<br>


# 📅17-02

### 📌 Aula 26 - Estruturas Condicionais pt 07 - Switch

Hoje finalizei mais uma etapa sobre a estrutura switch em Java.

Foi uma aula muito importante para consolidar meu entendimento sobre estruturas condicionais. Realizei um exercício proposto no curso DevDojo (disponível no repositório) e passei boa parte da tarde testando e “brincando” com o funcionamento do switch.

Durante os testes, explorei:

Como o switch se comporta com diferentes valores

A importância do break

O uso do default

Diferença entre switch e múltiplos if/else

Testes alterando valores diretamente nas cases

Pequenos erros que mudam completamente o resultado

Também pedi para a IA gerar exercícios progressivos para que eu pudesse resolver sozinho, evoluindo a dificuldade aos poucos. Isso me ajudou muito a fixar o conteúdo, principalmente entendendo o porquê das coisas funcionarem, e não apenas copiando código.

### 🧠 Principal aprendizado do dia

O switch é uma forma mais organizada e legível de trabalhar com múltiplas comparações de valores fixos, evitando vários if encadeados quando o cenário envolve escolhas diretas.

Além disso, percebi que:

Pequenos detalhes (como esquecer um break ou errar um cálculo dentro do case) mudam completamente o comportamento do programa.

E isso faz parte do processo.

# 📅18-02

### 📌 Aula 27 Estruturas Condicionais e de Repetição

### 🔄 While

Executa enquanto a condição for verdadeira.

````
int count = 0;
while (count < 10) {
    System.out.println(count);
    count++;
}
````
#### 📌 Pontos importantes:

A condição dentro dos parênteses deve retornar boolean

Se a variável de controle não for alterada, ocorre loop infinito

Primeiro verifica a condição, depois executa

🧠 Tradução mental

Enquanto count for menor que 10 → executar o bloco.

### 🔁 Do-While

Executa o bloco pelo menos uma vez, mesmo que a condição seja falsa.

````
int count = 12;

do {
    System.out.println("Executa pelo menos uma vez");
} while (count < 10);
````
### 📌 Diferença principal:

O while testa antes de executar

O do-while executa antes de testar

### 🔄 For

Estrutura mais utilizada quando sabemos exatamente quantas vezes queremos repetir.
````
for (int i = 0; i < 10; i++) {
    System.out.println("For " + i);
}
````
📌 Estrutura do for:
````
for (inicialização; condição; atualização)
````

Inicialização → executa uma única vez

Condição → verificada a cada repetição

Atualização → executada ao final de cada ciclo

🧠 Tradução mental

Para (começando em 0; enquanto for menor que 10; incrementando de 1 em 1) → executar o bloco.

## 🎯 Principais aprendizados

Sempre traduzir o código mentalmente

Entender a ordem real de execução

Evitar loops infinitos

Saber quando usar *switch*, *while*, *do-while* ou *for*

Pensar na legibilidade e organização do código




