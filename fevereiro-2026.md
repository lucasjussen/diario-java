# 📅 02-02 -    
📌 (Aula 7 e 18)

Revisei uns conteúdos da semana passada e pra ser mais especifico foram Lógicos AND e OR, que não é tão dificil é mais lógica de pensamento .


📌 (Aula 19)

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

📌 AULA 19 - ATRIBUIÇÃO: 

int contador = 0;
contador += 1; // contador = contador +1
contador++;
contador--;
++contador;
--contador;
int contador2 = 0;
System.out.println(++contador2);

SOBRE HOJE: Confesso que não consegui estudar muito porque to muito ansioso pro meu suporte chegar, vai ficar insano quando estudar

#  📅 03-02 

📌 (Aula 20) - Estudei Sobre Estruturas Condicionais PT01 - IF
” IF(true) “ - obrigatoriamente o resultado ou oque eu pôr dentro dos parenteses precisa ser true
IF só é executado se a condição de dentro do if ser true.
tem uma maneira de executar se for false que é fazendo comparação
ou usando “ ! “ EXEMPLO:

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
 ¹Se a idade fosse int idade = 17;  Executaria somente esse  porque o primeiro ali que é true não irá mostrar porque o resultado final seria abaixo dos 18.
Obs: esse ==false poderia ser substituído no início da frase como:
if(!isAutorizadoComprarBebida);
usar ! (MELHOR prática ⭐)
Mais limpo e profissional.

if tem que voltar um booleano.

##  📅 0602 (Aula 21) - Else:

if (isAutorizadoComprarBebida) {         //     Aqui é verdadeira
System.out.println("Autorizado a comprar bebida alcóolica");
}else {
System.out.println("Não autorizado a comprar bebida");

if(!isAutorizadoComprarBebida) {  // Aqui é false¹
System.out.println("Não Autorizado a comprar bebida alcóolica");
 }

A diferença de um false( ! ) pro outro( else ), é que else vai se basear na condição de if e ! sempre vai executar.

o else precisa de um if, não pode fazer aleatório(Tipo Romeo e Julieta)

Exercício que foi passado na aula:

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
Como o DevDojo fez:

int idade = 17;
if(idade < 15 ) {
System.out.println("Categoria infantil");
}else if(idade >= 15 && idade < 18) {
System.out.println("Categoria juvenil");
}else {
System.out.println("Categoria adulto");
}

nesse ultimo else não precisa dizer explicitamente pro compilador que ele é maior de idade, pois senão é um e não é outro, obviamente vai oque sobrou que é a Categoria Adulto.

e teve uma maneira que ele fez que eu achei muito interessante:

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

Ele criou uma string como categoria, e armazenou os valores tudo dentro dela, deixando p imprimir somente no fim, muito boa essa lógica






Hoje não estudei Java, mas estudei legal sobre Git :) isso que eu fui treinar ainda! amanha eu pego firme mas só pra deixar registrado aqui.

## 10-02 (22 - Estruturas Condicionais pt 03 - Operador ternário) - Ele ainda passou mais uma atividade de if e else e eu fiz de uma maneira e ele fez de outra com o código muito mais limpo, vamos analisar:

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

veja oque eu coloquei para imprimir, a forma… Agora veja do DevDojo

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

Veja como ficou bem mais logico, ele criou uma string com o nome resultado, e depois utilizou para armazenar o valor, e só no final que ele usa o system para imprimir somente a string

Agora vamos para o operadore ternário, aplicando o mesmo exercício:

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

Aplicando com o operador ternário, acaba se tornando muito mais fácil, e muito mais bonito… limpo.
fórmula:

(condicao) = (salario > 6000) ?
verdadeiro = mensagemDoar
falso = mensagemNaoDoar


E tem uma forma MUITO mais limpa

package academy.devdojo.maratonajava.introducao;

public class Aula05EstruturaCondicionais03 {
public static void main(String[] args) {
double salario = 6000;
// (condicao) ? verdadeiro : falso

String resultado = salario > 6000 ? "Eu vou doar 500 pro DevDojo" : "Ainda não tenho condições, mas vou ter!";

System.out.println(resultado);
}
}



Hoje eu vi apenas essa aula, estava morto de sono mas mesmo assim não desisti.. vi uma informação no twitter e queria deixar registrado aqui:

23 - Estruturas Condicionais pt 04 - Tabela Verdade e exercício:
quando utilizar && será verdadeiro se tudo for Verdadeiro, se utlizar || será falso se tudo for falso e o todo resto for verdadeiro


Ele passou uma atividade também, confesso que no começo eu me bati porque era pra mostrar uma coisa e acabei fazendo outra, era pra eu calcular o valor do imposto e coloquei pra mostrar a taxa que ele ia pagar… fiz totalmente errado, mas refiz e precisei que a IA me ajudasse a compreender oque eu fiz de errado, não deveria ter visto isso e sim ter me virado, mas não copiei o código inteiro, apenas para compreensão oque era pra fazer de fato..

resumindo: Tentei sozinho, errei a interpretação, refleti sobre o erro, busquei entender o conceito, refiz, não copiei..
Usei a IA para entender o problema e não para fazer pra mim

📅 12-02 - Fiquei estudando Estruturas Condicionais, mais especificamente IF/Else, pedi pro chatgpt me mandar uns exercícios sobre, e ele me passou um que eu me bati bastante…

2️⃣ Desconto em produto
Um produto custa R$ 200.
Se o cliente pagar à vista → 10% de desconto

Se parcelar → sem desconto
Mostre o valor final a pagar.
⚠️ O problema quer o valor final, não a porcentagem.

me bati muito porque eu tava ja querendo solucionar o problema no começo com as variaveis.. mas aqui está a solução que eu fiz sozinho depois de 1hr tentando e pensando:

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


Estudei MUITO hoje, MUITO mesmo, peguei uma boa parte de lógica e entendimento sobre if/else
