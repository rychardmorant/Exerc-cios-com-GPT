🔵 NÍVEL 2 — Lógica e Manipulação de Valores

Nesta etapa, começo a combinar os fundamentos aprendidos no Nível 1 com novos operadores e métodos do JavaScript.

O objetivo do Nível 2 é aprender a criar condições mais completas, manipular valores e textos e controlar melhor o comportamento dos programas.

14. else if

O else if é utilizado quando existem mais de duas possibilidades.

No if e else, temos apenas duas possibilidades:

if (condicao) {
// verdadeiro
} else {
// falso
}

Com else if, podemos adicionar novas condições:

if (condicao1) {
// primeira possibilidade
} else if (condicao2) {
// segunda possibilidade
} else {
// caso nenhuma seja verdadeira
}
Exemplo
const idade = 16;

if (idade >= 18) {
console.log("Maior de idade.");
} else if (idade >= 13) {
console.log("Adolescente.");
} else {
console.log("Criança.");
}

O JavaScript verifica as condições de cima para baixo.

idade >= 18?
↓
NÃO

idade >= 13?
↓
SIM

"Adolescente."
Importante

O else não precisa ter uma condição.

Ele funciona como:

Se nenhuma das condições anteriores for verdadeira, faça isso.

15. && — AND

O operador && significa E.

Ele permite verificar se duas ou mais condições são verdadeiras ao mesmo tempo.

if (condicao1 && condicao2) {
// código
}
Exemplo
const nota = 8;

if (nota >= 7 && nota <= 10) {
console.log("Nota válida.");
}

Nesse caso, precisamos ter:

nota >= 7
E
nota <= 10

As duas precisam ser verdadeiras.

Tabela
true && true → true
true && false → false
false && true → false
false && false → false
Exemplo prático
const idade = 20;
const documento = true;

if (idade >= 18 && documento === true) {
console.log("Entrada permitida.");
}

A pessoa precisa:

Ter 18 anos ou mais;
E possuir documento. 16. || — OR

O operador || significa OU.

Diferente do &&, aqui apenas uma das condições precisa ser verdadeira.

if (condicao1 || condicao2) {
// código
}
Exemplo
const idade = 16;
const acompanhado = "sim";

if (idade >= 18 || acompanhado === "sim") {
console.log("Pode entrar.");
}

A entrada será permitida se:

idade >= 18
OU
acompanhado === "sim"
Tabela
true || true → true
true || false → true
false || true → true
false || false → false
Diferença entre && e ||
&& → todas precisam ser verdadeiras

|| → pelo menos uma precisa ser verdadeira 17. ! — NOT

O operador ! significa NÃO.

Ele serve para inverter um valor booleano.

const logado = true;

console.log(!logado);

Resultado:

false

Porque:

true → false
false → true
Exemplo
const logado = false;

if (!logado) {
console.log("Faça login.");
}

Como logado é false, então:

!logado

é true.

Por isso o código será executado.

Resumo
!true → false
!false → true 18. ++

O operador ++ aumenta uma variável em 1.

let contador = 0;

contador++;

Agora:

contador = 1

Se executarmos novamente:

contador++;

Teremos:

contador = 2
Forma completa
contador = contador + 1;

É equivalente a:

contador++;
Exemplo com botão
let contador = 0;

botao.addEventListener("click", function () {
contador++;

    resultado.textContent = contador;

});

Cada clique aumenta o contador em 1.

19. --

O operador -- diminui uma variável em 1.

let contador = 5;

contador--;

Resultado:

contador = 4

É equivalente a:

contador = contador - 1;
Exemplo
let vidas = 3;

vidas--;

console.log(vidas);

Resultado:

2
Diferença
++ → adiciona 1

-- → remove 1 20. .toUpperCase()

.toUpperCase() transforma todas as letras de um texto em maiúsculas.

const nome = "Rychard";

const nomeMaiusculo = nome.toUpperCase();

console.log(nomeMaiusculo);

Resultado:

RYCHARD
Com .value
const nomeDigitado = nome.value;

const nomeMaiusculo = nomeDigitado.toUpperCase();

resultado.textContent = nomeMaiusculo;

Se o usuário digitar:

Rychard

O resultado será:

RYCHARD
Importante

O método não altera o texto original.

const nome = "Rychard";

const resultado = nome.toUpperCase();

Agora:

nome → "Rychard"
resultado → "RYCHARD" 21. .toLowerCase()

.toLowerCase() faz o contrário de .toUpperCase().

Ele transforma o texto em letras minúsculas.

const nome = "RYCHARD";

const nomeMinusculo = nome.toLowerCase();

console.log(nomeMinusculo);

Resultado:

rychard
Comparação
nome.toUpperCase();

Transforma em:

RYCHARD

Enquanto:

nome.toLowerCase();

Transforma em:

rychard
Quando isso é útil?

Pode ser utilizado para facilitar comparações:

const resposta = input.value.toLowerCase();

if (resposta === "sim") {
console.log("Resposta confirmada.");
}

Assim, entradas como:

SIM
Sim
sim
sIm

podem ser convertidas para:

sim

antes da comparação.

22. .length

.length informa a quantidade de caracteres de um texto.

const nome = "Rychard";

console.log(nome.length);

Resultado:

7

Podemos armazenar esse resultado:

const quantidade = nome.length;

E depois utilizar:

resultado.textContent =
"Seu nome tem " + quantidade + " caracteres.";
Espaços

Os espaços também contam como caracteres.

const texto = "Olá mundo";

console.log(texto.length);

O espaço entre "Olá" e "mundo" também será contado.

Exemplo prático

Podemos verificar se um nome possui poucos caracteres:

const nome = input.value;

if (nome.length < 3) {
console.log("Nome muito curto.");
} 23. .trim()

.trim() remove espaços que estão no começo e no final de uma String.

Exemplo:

const nome = " Rychard ";

const nomeLimpo = nome.trim();

console.log(nomeLimpo);

Resultado:

Rychard
Por que isso é útil?

Imagine um usuário digitando:

Rychard

Sem trim():

nome

contém os espaços.

Com:

nome.trim()

obtemos:

Rychard
trim() não remove espaços entre palavras
const nome = "Rychard Cardoso";

console.log(nome.trim());

Continua:

Rychard Cardoso

O espaço entre as palavras permanece.

24. Math.round()

Math.round() arredonda um número para o inteiro mais próximo.

const numero = 7.6;

const numeroArredondado = Math.round(numero);

console.log(numeroArredondado);

Resultado:

8
Exemplos
Math.round(7.1); // 7
Math.round(7.4); // 7
Math.round(7.5); // 8
Math.round(7.9); // 8

Regra simplificada:

7.0 → 7
7.4 → 7
7.5 → 8
7.9 → 8
Outros métodos parecidos

Ainda não precisamos estudar profundamente esses métodos, mas é importante saber que existem:

Math.floor()

Arredonda para baixo.

Math.ceil()

Arredonda para cima.

Por enquanto, o foco é:

Math.round()
🧠 COMO COMBINAR OS CONCEITOS

O verdadeiro objetivo do Nível 2 é começar a combinar os conhecimentos.

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
        const nomeMaiusculo = nomeLimpo.toUpperCase();

        resultado.textContent =
            "Olá, " + nomeMaiusculo + "!";
    }

});

Aqui estamos usando vários conhecimentos:

querySelector()
↓
.value
↓
.trim()
↓
if / else
↓
.toUpperCase()
↓
.textContent

Esse tipo de combinação é o que começa a transformar os conceitos separados em lógica de programação.

📌 RESUMO DO NÍVEL 2
Nº Conceito Para que serve
14 else if Criar várias possibilidades
15 && Exigir várias condições verdadeiras
16 `	
	` Permitir uma ou outra condição
17 ! Inverter true/false
18 ++ Aumentar 1
19 -- Diminuir 1
20 .toUpperCase() Transformar texto em maiúsculas
21 .toLowerCase() Transformar texto em minúsculas
22 .length Contar caracteres
23 .trim() Remover espaços das extremidades
24 Math.round() Arredondar números
🎯 O QUE PRECISO CONSEGUIR FAZER

Depois de estudar o Nível 2, o objetivo é conseguir olhar para um código e entender coisas como:

const valor = Number(input.value);

if (valor >= 7 && valor <= 10) {
resultado.textContent = "Nota válida.";
} else if (valor >= 5 || valor === 0) {
resultado.textContent = "Verifique sua nota.";
} else {
resultado.textContent = "Nota baixa.";
}

Não é necessário decorar tudo.

O mais importante é conseguir olhar e pensar:

const
↓
cria uma variável

Number()
↓
transforma em número

if
↓
verifica uma condição

&&
↓
as duas condições precisam ser verdadeiras

else if
↓
verifica outra possibilidade

else
↓
caso contrário

.textContent
↓
mostra uma mensagem no HTML

Esse é o principal objetivo do Nível 2:

Parar de apenas reconhecer comandos e começar a entender a lógica por trás deles.
