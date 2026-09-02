🟢 NÍVEL 1 — Fundamentos

O Nível 1 apresenta os conceitos básicos necessários para começar a programar em JavaScript.

1. Variáveis

Variáveis são utilizadas para armazenar informações.

const

Usamos const quando o valor da variável não será substituído.

const nome = "Rychard";
let

Usamos let quando o valor pode ser alterado.

let contador = 0;

contador = contador + 1;
Resumindo
const → valor não será reatribuído
let → valor pode ser alterado 2. Tipos de dados

JavaScript possui diferentes tipos de valores.

String

Texto.

const nome = "Rychard";
Number

Número.

const idade = 16;
const preco = 29.90;
Boolean

Representa verdadeiro ou falso.

const logado = true;
const aprovado = false; 3. document.querySelector()

querySelector() permite selecionar um elemento do HTML através de um seletor CSS.

HTML:

<h1 id="titulo">Olá!</h1>

JavaScript:

const titulo = document.querySelector("#titulo");

O # significa que estamos procurando um elemento pelo seu id.

#titulo

Significa:

Procure o elemento que possui id="titulo".

4. .value

.value é utilizado principalmente para pegar aquilo que foi digitado dentro de um <input>.

HTML:

<input id="nome">

JavaScript:

const nome = document.querySelector("#nome");

console.log(nome.value);

Se o usuário digitar:

Rychard

Então:

nome.value

retornará:

"Rychard"
Importante

O valor de um <input> normalmente chega como String.

Por isso, quando queremos fazer contas, precisamos utilizar Number().

5. Number()

Number() transforma um valor em número.

Por exemplo:

const idade = Number(input.value);

Se:

input.value

for:

"18"

Depois de usar:

Number(input.value)

teremos:

18

Isso é importante para operações matemáticas.

const numero1 = Number(input1.value);
const numero2 = Number(input2.value);

const resultado = numero1 + numero2; 6. .textContent

.textContent permite acessar ou alterar o texto de um elemento HTML.

HTML:

<p id="resultado"></p>

JavaScript:

const resultado = document.querySelector("#resultado");

resultado.textContent = "Olá, Rychard!";

O HTML passará a mostrar:

Olá, Rychard!

Também podemos colocar variáveis:

const nome = "Rychard";

resultado.textContent = "Olá, " + nome + "!"; 7. addEventListener()

addEventListener() permite fazer o JavaScript esperar por um evento.

Por exemplo, um clique:

botao.addEventListener("click", function () {
console.log("Botão clicado!");
});

Nesse caso:

addEventListener → fica esperando um evento
"click" → evento de clique
function () → código executado quando acontecer 8. Funções

Funções são blocos de código que podem ser executados quando necessários.

function mostrarMensagem() {
console.log("Olá!");
}

Para executar:

mostrarMensagem();

Também podemos usar funções dentro de eventos:

botao.addEventListener("click", function () {
console.log("Clicou!");
}); 9. if

if significa "se".

Ele permite executar um código somente quando uma condição for verdadeira.

const idade = 18;

if (idade >= 18) {
console.log("Maior de idade.");
}

A condição:

idade >= 18

precisa ser verdadeira para o código ser executado.

10. else

else significa "caso contrário".

É utilizado quando queremos executar outro código caso o if seja falso.

const idade = 16;

if (idade >= 18) {
console.log("Pode entrar.");
} else {
console.log("Não pode entrar.");
}

A estrutura é:

SE a condição for verdadeira
faça isso

CASO CONTRÁRIO
faça aquilo 11. Operadores de comparação

Os operadores de comparação servem para comparar valores.

Maior que
idade > 18
Menor que
idade < 18
Maior ou igual
idade >= 18
Menor ou igual
idade <= 18
Igualdade estrita
idade === 18

O === verifica se os valores são iguais e também considera o tipo do valor.

Exemplo:

18 === 18

Resultado:

true 12. Operadores matemáticos

JavaScript permite realizar operações matemáticas.

Adição
10 + 5

Resultado:

15
Subtração
10 - 5

Resultado:

5
Multiplicação
10 \* 5

Resultado:

50
Divisão
10 / 5

Resultado:

2 13. console.log()

console.log() serve para mostrar informações no console do navegador.

console.log("Olá!");

Também podemos mostrar variáveis:

const idade = 18;

console.log(idade);

É muito útil para verificar o que está acontecendo no código.

Por exemplo:

const valor = Number(input.value);

console.log(valor);

Assim conseguimos verificar se o valor realmente foi convertido para número.

🔵 NÍVEL 2 — Lógica e manipulação de valores

No Nível 2 começamos a combinar os conhecimentos anteriores e aprendemos novos operadores e métodos.

14. else if

else if permite verificar várias condições.

Exemplo:

const idade = 16;

if (idade >= 18) {
console.log("Maior de idade.");
} else if (idade >= 13) {
console.log("Adolescente.");
} else {
console.log("Criança.");
}

A ordem é importante.

O JavaScript verifica:

1. if
2. else if
3. else

Quando encontra uma condição verdadeira, executa aquele bloco.

15. && — AND

&& significa E.

Todas as condições precisam ser verdadeiras.

if (nota >= 7 && nota <= 10) {
console.log("Nota válida.");
}

Nesse caso, precisamos ter:

nota >= 7
E
nota <= 10

Exemplo:

8 >= 7 && 8 <= 10

Resultado:

true 16. || — OR

|| significa OU.

Com ||, basta uma das condições ser verdadeira.

if (idade >= 18 || acompanhado === "sim") {
console.log("Pode entrar.");
}

A pessoa pode entrar se:

idade >= 18
OU
acompanhado === "sim"

Exemplo:

16 >= 18 || "sim" === "sim"

Resultado:

true 17. ! — NOT

! significa NÃO e serve para inverter um valor booleano.

Se temos:

const logado = true;

Então:

!logado

será:

false

E:

const logado = false;

Então:

!logado

será:

true
Resumindo
!true → false
!false → true 18. ++

++ aumenta o valor de uma variável em 1.

let contador = 0;

contador++;

Agora:

contador = 1

Se executarmos novamente:

contador++;

Teremos:

contador = 2

É uma forma mais curta de escrever:

contador = contador + 1; 19. --

-- diminui o valor de uma variável em 1.

let contador = 5;

contador--;

Agora:

contador = 4

É equivalente a:

contador = contador - 1; 20. .toUpperCase()

.toUpperCase() transforma um texto em letras maiúsculas.

const nome = "Rychard";

const nomeMaiusculo = nome.toUpperCase();

console.log(nomeMaiusculo);

Resultado:

RYCHARD 21. .toLowerCase()

.toLowerCase() transforma um texto em letras minúsculas.

const nome = "RYCHARD";

const nomeMinusculo = nome.toLowerCase();

console.log(nomeMinusculo);

Resultado:

rychard 22. .length

.length informa a quantidade de caracteres de um texto.

const nome = "Rychard";

console.log(nome.length);

Resultado:

7

Também pode ser usado diretamente:

const quantidade = nome.length;
Importante

Os espaços também podem ser considerados caracteres.

Por exemplo:

"Olá mundo".length

conta também o espaço entre as palavras.

23. .trim()

.trim() remove espaços desnecessários no começo e no final de um texto.

Exemplo:

const nome = " Rychard ";

const nomeLimpo = nome.trim();

console.log(nomeLimpo);

Resultado:

Rychard

O trim() não remove espaços entre palavras.

"Rychard Cardoso"

continua:

"Rychard Cardoso" 24. Math.round()

Math.round() arredonda um número para o inteiro mais próximo.

const numero = 7.6;

const resultado = Math.round(numero);

console.log(resultado);

Resultado:

8

Outro exemplo:

Math.round(7.2)

Resultado:

7

Regra básica:

7.4 → 7
7.5 → 8
7.8 → 8
🧠 Como os conceitos se conectam

Um dos objetivos dos exercícios é aprender a combinar vários conceitos.

Por exemplo:

const nome = document.querySelector("#nome");
const botao = document.querySelector("#botao");
const resultado = document.querySelector("#resultado");

botao.addEventListener("click", function () {

    const nomeDigitado = nome.value;
    const nomeLimpo = nomeDigitado.trim();

    if (nomeLimpo === "") {
        resultado.textContent = "Digite seu nome.";
    } else {
        resultado.textContent = "Olá, " + nomeLimpo + "!";
    }

});

Nesse pequeno programa usamos:

querySelector()
↓
.value
↓
.trim()
↓
if / else
↓
.textContent
↑
addEventListener()

É assim que os conceitos começam a trabalhar juntos.

📋 Resumo completo
Nível 1
Nº Conteúdo
1 const e let
2 Tipos de dados
3 querySelector()
4 .value
5 Number()
6 .textContent
7 addEventListener()
8 Funções
9 if
10 else
11 Operadores de comparação
12 Operadores matemáticos
13 console.log()
Nível 2
Nº Conteúdo
14 else if
15 &&
16 `	
	`
17 !
18 ++
19 --
20 .toUpperCase()
21 .toLowerCase()
22 .length
23 .trim()
24 Math.round()
🎯 Objetivo dos estudos

O objetivo destes exercícios é desenvolver a capacidade de:

Ler código;
Entender o que cada linha faz;
Identificar erros;
Corrigir erros;
Criar condições;
Trabalhar com valores;
Manipular elementos HTML;
Desenvolver lógica de programação;
Resolver pequenos problemas utilizando JavaScript.

A prioridade é entender a lógica, e não simplesmente copiar códigos prontos.

🛠️ Tecnologias
HTML5
JavaScript
DOM
VS Code
Git / GitHub

📈 Progresso
NÍVEL 1
████████████████████ 100%

NÍVEL 2
██████████████████░░ 90%

O próximo objetivo é continuar praticando os conceitos do Nível 2 até conseguir utilizá-los sem depender de exemplos prontos.
