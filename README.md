# Scheme-case-study 
 Estudo de caso da linguagem de programação Scheme desenvolvido para a materia de LP
 
 # 📌Historico

Os primórdios da linguagem Scheme ocorreram entre 1975 e 1980, quando foi descrita pela primeira vez no Laboratório de Inteligência Artificial e Ciência da Computação do MIT. Foi criado por Guy Steele e Gerald Sussman a partir da lingugem Lisp com intuito de desenvolver uma lingugem de semantica simples e clara e afim de estudar a teoria dos atores de Carl Hewitt.Sussman e Steele tiveram algumas dificuldades em entender alguns detalhes do modelo de Hewitt e suas consequências, então decidiram experimentá-lo construindo uma implementação de brinquedo da linguagem.
 
 Eles escreveram um pequeno interpretador Lisp e adicionaram os mecanismos necessários para criar atores e enviar mensagens, resultando na linguagem Scheme, originalmente chamada Schemer.

 Scheme é uma versão estática e recursiva da linguagem de programação. Ela foi desenvolvida com intuito de apresentar uma semântica simples e clara, apresentando poucas formas Diferentes de formar expressões. Uma grande variedade de paradigmas de programação são encontrados em Scheme, entre eles, programação funcional, e programação por passagem de mensagens.
 
  Scheme foi uma das primeiras linguagens de programação a introduzir o lambda cálculo nos métodos da classe principal. Também possibilita a usabilidade de regras de escopo estático e estruturas em bloco em uma linguagem tipada.

# 📌Objetivos, Contextualização e Características

Scheme é uma linguagem de programação multiparadigma que suporta programação funcional e procedural.
# Ambiente de programação

Muitas linguagens oferecem um dispositivo chamado “REPL” (Read-Eval-Print Loop).
O REPL é um programa que lê expressões ou trechos de programa, “avalia” (ou “executa”) e mostra o resultado. Python, Ruby, Common Lisp, Haskell e a vasta maioria das implementações de Scheme oferecem um REPL. Na prática, a experiência de usar o REPL é semelhante à de interagir com um computador usando linha de comando em um
terminal


## Algumas Características 
Sua Flexibilidade é garantida devido a ausência de restrições tornando dessa forma seu porder ilimitado.

Utilização de sistemas de recursão.

Fortemente tipada.

Lingugem multiparadigma utilizando o paradigma funcional e procedual. 

Possui boa capacidade de leitura devido a sua simplicidade, por possuir um pequeno conjunto de regras há a capaciadde de compolas assim tornando uma linguagem confiável e poderosa. 

## Paradigma 
Como o Scheme é uma linguagem de programação multiparadigma o paradigma funcional é de ação que trata como uma avaliação de funções matemáticas, ele evita estados mutáveis e enfatiza funções, em contraste da programação imperativa, que reforça mudanças no estado do programa.

O paradigma procedural é utilizado muitas vezes como sinônimo de programação imperativa, que especifica os passos que deve seguir para atingir um estado , mas o termo procedural indica que se baseia no numero de chamadas de procedimentos, também conhecidos como rotinas, sub-rotinas ou funções (diferentes das funções matemáticas). Atenta-se que tais procedimentos são similares à avaliação realizada na programação funcional, sendo um conjunto de passos computacionais a serem executados, podendo ser chamado a qualquer hora durante a execução do programa, através de outros procedimentos e até por si mesmo.

-> Existem dois padrões que definem a lingugem: O padrão IEEE P1178 e um padrão popular chamado RnRs

# Tour pela lingugem 

## Instalação

## Tipos de dados básicos
- Boolean

#t=True - Qualquer coisa diferente de zero e lista vazia 

#f=False - Zero ou lista vazia 

- Numbers

Numero   = ex: 22

Complex  = ex: (2+3i)

Real     = ex: (2,8954)

Racional = ex: (2,8954) (22/2)

Inteiro = ex: 23

Numero=Complex=Real=Racional=Inteiro

- Caracteres 

São representados pelo prefixo #\

#\c = caracatere

#\New Line e  #\space = espaço em branco

- Symbols 

Tratados como identificadores de variaveis, para especificarmos um symbolo usamos a palavra reservada QUOTE ou aspas simples antes do símbolo 

Ex: quote(xyz)  ou `E

- Strings 

Não é um tipo simples, ou seja, primitivo como os anteriores, é composta pela combinação de caracteres sendo assim uma sequencia de caracteres de modo estruturado e ente aspas dulpas "".

Ex: (string #\o #\l #\a) ou "Ola"

- Vetores 
São sequencias como as strings mas seus elementos podem ser uma sequencia de qualquer tipo e não apenas de caracteres 

Ex: (vector 01234)

- Dotted pair 
É composto de dois valores arbritarios, sendo o primeiro chamado de car e o segundo de cdr e sua combinaçaão é realizada com a palavra reservada cons 

Ex: (cons 1 #t)

- Listas 

Podem ser construidas simplismente colocando os valores desejados entre parenteses e utilizando aspa simples antes do primeiro parentese ou utilizando a palvra reservada list

LISTAS PODEM CONTER QUALQUER VALOR INCLUSIVE LISTA DE LISTA 

Ex: >`(246810)  ou >(list 249810)

Assim como os vetores, podemos utilizar car e cdr para acessarmos o primeiro elemento e o restante da lista

Ex:>(car(list 249810))

- Expressões condicionais
Para tomar decisões e escolher uma dentre duas ou mais formas a avaliar, Scheme oferece algumas formas especiais.
IF : (if(<ab)(squarea squareb)) ou  

(if(<x1x2)(>x2x3)
    (if(>x1 x2)(<x2x3)
    
 COND: 
  (Cond (condicao1 consequencia1)
        (condicao2 consequancia2)
        
        .
        .
        .
        (else alternativa))
        
 CASE:
 (case arg expr1 expr2 expr3...)
 
 - Operadores lógicas 
 And, or e not.
 
 - Declarações 
 
 Utilizamos a palavra reservada define para declarar variaveis globais
 E a SET para alterar variaveis.
 
 Ex: (define a 23)
     (set! a 6)
     
- Let
Da mesma forma que os argumentos de um procedimento podem ser usados apenas dentro do corpo do procedimento, é possível criar variáveis temporárias acessíveis apenas
dentro de um trecho de programa Scheme usando a forma especial let.

Ex: ( let (( nome1 valor1)
            ( nome2 valor2)
            ...)

## Palavras-chave

## Operadores

## Sentenças

## Features da linguagem Scheme
• r7rs: a implementação declara implementar corretamente o padrão R7RS.

• exact-closed: todas as operações algébricas com exatos (exceto /) resultam em
números exatos.

• ratios: A operação / com argumentos exatos produz um resultado exato quando o
divisor não é zero (ou seja, a implementação suporta frações exatas).

• exact-complex: a implementação suporta números complexos exatos.

• ieee-float: números inexatos são representados como no padrão IEEE 754.

• full-unicode: todos os codepoints Unicode são suportados como caracteres.

• windows: a implementação de Scheme está rodando em um sistema Windows.

• posix: a implementação de Scheme está rodando em um sistema POSIX.

• unix, darwin, linux, bsd, freebsd, solaris, ... : descreve o tipo de sistema
operacional.

• i386, x86-64, ppc, sparc, jvm, clr, llvm, ... : descvreve a arquitetura da CPU.

• ilp32, lp64, ilp64, ... : descreve o modelo de memória C.

• big-endian, little-endian: descreve a ordem de bytes ao representar palavras.

• nome: o nome da implementação Scheme.

• nome-versao: nome e versão da implementação Scheme.
