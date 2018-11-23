# Básico

Apenas exibir `hello world` não é suficiente, é? Você quer fazer mais que isso - você quer obter alguma entrada, manipulá-la e produzir algo disso. Podemos alcançar isso em Python usando constantes e variáveis, e aprenderemos outros conceitos neste capítulo.

## Comentários

_Comentário_ é qualquer texto à direita do símbolo `#` e é principalmente útil como nota para o leitor do programa.

Por exemplo:

```python
print('hello world') # Note que print é uma função
```

ou:

```python
# Note que print é uma função
print('hello world')
```

Utilize quantos comentários você puder em seu programa para:

- explicar suposições
- explicar decisões importantes
- explicar detalhes importantes
- explicar problemas que você está tentando solucionar
- explicar problemas que você está tentando superar em seu programa, etc.

[*O código lhe diz o como, os comentários devem dizer o porquê*](http://www.codinghorror.com/blog/2006/12/code-tells-you-how-comments-tell-you-why.html).

Isto é útil para os leitores de seu programa para que eles possam facilmente compreender o que o programa está fazendo. Lembre-se, essa pessoa pode ser você após seis meses!

## Constantes Literais

Um exemplo de uma constante literal é um número como `5`, `1.23`, ou uma cadeia de caracteres como `'This is a string'` ou `"It's a string!"`.

É chamado de literal porque ela é _literal_ - você utiliza seu valor literalmente. O número `2` sempre representa ele mesmo e nada mais - ele é uma _constante_ porque seu valor não pode ser modificado. Assim, todos eles são referidos como constantes literais.

## Números

Números são principalmente de dois tipos - inteiros e de ponto flutuante.

Um exemplo de um inteiro é `2` que á apenas um número inteiro.

Exemplos de números de ponto flutuante (ou _floats_ para simplificar) são `3.23` e `52.3E-4`. A notação `E` indica potências de 10. Neste caso, `52.3E-4` representa `52.3 * 10^-4^`.

> **Nota para Programadores Experientes**
> 
> Não há um tipo separado `long`. O tipo `int` pode ser um inteiro de qualquer tamanho.

## Cadeias de Caracteres (_string_)

Uma cadeia de caracteres (_string_) é uma _sequência_ de _caracteres_. Cadeias de caracteres são basicamente apenas um bando de palavras.

Você utilizará cadeias de caracteres em quase todo programa Python que você escrever, logo preste atenção na parte a seguir.

### Aspa Simples

Você pode especificar cadeias de caracteres utilizando aspas simples tais como `'Quote me on this'`.

Todo espaço em branco, isto é, espaços e tabulações, são preservados como estão.

### Aspas Duplas

Cadeias de caracteres em aspas duplas operam exatamente da mesma maneira que cadeias de caracteres entre aspas simples. Um exemplo é `"Qual é o seu nome?"`.

### Aspas Triplas {#triple-quotes}

Você pode especificar cadeias de caracteres em múltiplas linhas utilizando aspas triplas - (`"""` ou `'''`). Você pode utilizar aspas simples ou aspas duplar livremente dentro das aspas triplas. Um exemplo é:

```python
'''Esta é uma cadeia de caracteres de múltiplas linhas. Esta é a primeira linha.
Esta é a segunda linha.
"Qual é o seu nome?," eu perguntei.
Ele disse "Bond, James Bond."
'''
```

### Cadeias de Caracteres são Imutáveis

Isto significa que uma vez que tenha criado a cadeia de caracteres, você não pode modificá-la. Embora isso possa parecer uma coisa ruim, realmente não é. Veremos porque isto não é uma limitação nos vários programas que observaremos adiante.

> **Nota para Programadores C/C++**
> 
> Não há um tipo `char` separado em Python. Não necessidade real para ele e tenho certeze que você não sentirá falta.

<!-- -->

> **Nota para Programadores Perl/PHP**
> 
> Lembre-se que cadeias de caracteres entre aspas simples e aspas duplas representam a mesma coisa - não diferem de forma nenhuma.

### O método format

Ás vezes queremos construir cadeias de caracteres a partir de outra informação. Isto é onde o método `format()` é útil.

Salve as seguintes linhas como um arquivo `str_format.py`:

```python
idade = 20
nome = 'Swaroop'

print('{0} tinha {1} anos quando ele escreveu este livro'.format(nome, idade))
print('Por que {0} está brincando com aquela píton?'.format(nome))
```

Saída:

```
$ python str_format.py
Swaroop tinha 20 anos quando ele escreveu este livro
Por que Swaroop está brincando com aquela píton?
```

**Como Funciona**

Uma cadeia de caracteres pode utilizar certas especificações e subsequentemente, o método `format` pode ser chamado para substituir estas especificações que correspondam à argumentos no método `format`.

Observe o primeiro uso onde utilizamos `{0}` e isso corresponde à variável `nome` que é o primeiro argumento do método format.
De forma similar, a segunda especificação é `{1}` correspondendo à `idade` que é o segundo argumento para o método format. Note que Python começa contando de 0 que significa que a primeira posição está no índice 0, a segunda posição no índice 1, e assim por diante.

Perceba que poderíamos alcançar o mesmo utilizando concatenação de cadeia de caracteres:

```python
nome + ' é ' + str(idade) + ' anos'
```

mas isso é muito feio e sujeito a erros. Segundo, a conversão para cadeia de caracteres poderia ser feita automaticamente pelo método `format` ao invés da conversão explícita necessária para cadeia de caracteres neste caso. Terceiro, ao usar o método `format`, podemos modificar a mensagem sem ter de manipular as variáveis utilizadas e vice-versa.

Note também que os número são opcionais, logo você poderia também ter escrito como:

```python
idade = 20
nome = 'Swaroop'

print('{} tinha {} anos quando ele escreveu este livro'.format(nome, idade))
print('Por que {} está brincando com aquela píton?'.format(nome))
```

que dará a mesma saída que a do programa anterior.


Podemos também nomear os parâmetros:

```python
idade = 20
nome = 'Swaroop'

print('{nome} tinha {idade} anos quando ele escreveu este livro'.format(nome=nome, idade=idade))
print('Por que {nome} está brincando com aquela píton?'.format(nome=nome))
```

que dará a mesma saída que o programa anterior.

Python 3.6 introduziu um atalho para parâmetros nomeados, chamado "f-strings":

```python
idade = 20
nome = 'Swaroop'

print(f'{nome} tinha {idade} quando ele escreveu este livro')  # perceba o  'f' antes da cadeia de caracteres
print(f'Por que {nome} está brincando com aquela píton?')  # perceba o  'f' antes da cadeia de caracteres
```

que dará a mesma saída que o programa anterior.


O que Python faz no método `format` é que substitui cada valor de argumento no local da especificação. Existem mais especificações detalhadas tais como:

```python
# decimal (.) precisão de 3 para o ponto flutuante '0.333'
print('{0:.3f}'.format(1.0/3))
# preencher com underscores (_) com o texto centralizado
# (^) até 11 caracteres de largura '___hello___'
print('{0:_^11}'.format('hello'))
# base em palavras chave 'Swaroop wrote A Byte of Python'
print('{nome} escreveu {livro}'.format(nome='Swaroop', livro='A Byte of Python'))
```

Saída:

```
0.333
___hello___
Swaroop escreveu A Byte of Python
```

Uma vez que estamos discutindo formatação, note que `print` sempre termina com um caractere invisível de "nova linha" (`\n`) de forma que chamadas repetidas a `print` exibirão o resultado em linhas distintas. Para evitar este caractere de nova linha ser exbido, você pode definir que deve terminar (`end`) com um branco:

```python
print('a', end='')
print('b', end='')
```

Saída é:

```
ab
```

Ou você pode encerrar (`end`) com um espaço:


```python
print('a', end=' ')
print('b', end=' ')
print('c')
```

Saída é:

```
a b c
```

### Sequências de Escape

Suponha que você quer ter uma cadeia de caracteres que contenha uma aspa simples (`'`), como você especifica essa cadeia de caracteres? Por exemplo, a cadeia de caracteres é `"Qual é o seu nome?"`. Você não pode especificar `'Qual é o seu 'nome''` porque Python ficará confuso sobre onde a cadeia de caracteres começa e termina. Logo, você terá de especificar que está aspa simples não indica o fim da cadeia de caracteres. Isto pode ser feito com a ajuda do que é chamado uma _sequência de escape_. Você especifica a aspa simples como `\'`: perceba a barra invertida. Agora, você pode especificar a cadeia de caracteres como `'Qual o seu \'nome\'?`.

Outra maneira de especificar esta cadeia de caracteres específica seria `"Qual o seu 'nome'?"` entre aspas simples. De forma similar, você deve usar uma sequência de escape ao utilizar aspas duplas em cadeias de caracteres entre aspas duplas. Você também deve indicar a barra invertida usando a sequência de escpae `\\`.

E se você quisesse especificare uma cadeia de caracteres de duas linhas? Um modo é utilizar um cadeia de caracteres de aspas triplas como apresentado [anteriormente](#triple-quotes) ou você pode utilizar uma sequência de escape para o caractere de nova linha - `\n` para indicar o início de uma nova linha. Um exemplo é:

```python
'Isto é a primeira linha\nIsto é a segunda linha'
```

Outra sequência de escape útil em saber é a tabulação `\t`. Há muito mais sequências de escape mas eu mencionei somente as mais úteis aqui.

Uma coisa a considerar é que em uma cadeia de caracteres, uma simples barra invertida no fim da linha indica que a cadeia de caracteres continua na próxima linha, mas nenhuma nova linha é adicionada. por exemplo:

```python
"Esta é a primeira sentença. \
Esta é a segunda sentença."
```

equivale a

```python
"Esta é a primeira sentença. Esta é a segunda sentença."
```

### Cadeia de Caracteres Bruta

If you need to specify some strings where no special processing such as escape sequences are handled, then what you need is to specify a _raw_ string by prefixing `r` or `R` to the string. An example is:

```python
r"Newlines are indicated by \n"
```

> **Note for Regular Expression Users**
> 
> Always use raw strings when dealing with regular expressions. Otherwise, a lot of backwhacking may be required. For example, backreferences can be referred to as `'\\1'` or `r'\1'`.

## Variable

Using just literal constants can soon become boring - we need some way of storing any information and manipulate them as well. This is where _variables_ come into the picture. Variables are exactly what the name implies - their value can vary, i.e., you can store anything using a variable. Variables are just parts of your computer's memory where you store some information. Unlike literal constants, you need some method of accessing these variables and hence you give them names.

## Identifier Naming

Variables are examples of identifiers. _Identifiers_ are names given to identify _something_. There are some rules you have to follow for naming identifiers:

- The first character of the identifier must be a letter of the alphabet (uppercase ASCII or lowercase ASCII or Unicode character) or an underscore (`_`).
- The rest of the identifier name can consist of letters (uppercase ASCII or lowercase ASCII or Unicode character), underscores (`_`) or digits (0-9).
- Identifier names are case-sensitive. For example, `myname` and `myName` are _not_ the same. Note the lowercase `n` in the former and the uppercase `N` in the latter.
- Examples of _valid_ identifier names are `i`, `name_2_3`. Examples of _invalid_ identifier names are `2things`, `this is spaced out`, `my-name` and `>a1b2_c3`.

## Data Types

Variables can hold values of different types called _data types_. The basic types are numbers and strings, which we have already discussed. In later chapters, we will see how to create our own types using [classes](./oop.md#classes).

## Object

Remember, Python refers to anything used in a program as an _object_.  This is meant in the generic sense. Instead of saying "the _something_"', we say "the _object_".

> **Note for Object Oriented Programming users**:
>
> Python is strongly object-oriented in the sense that everything is an object including numbers, strings and functions.

We will now see how to use variables along with literal constants. Save the following example and run the program.

## How to write Python programs

Henceforth, the standard procedure to save and run a Python program is as follows:

### For PyCharm

1. Open [PyCharm](./first_steps.md#pycharm).
2. Create new file with the filename mentioned.
3. Type the program code given in the example.
4. Right-click and run the current file.

NOTE: Whenever you have to provide [command line arguments](./modules.md#modules), click on `Run` -> `Edit Configurations` and type the arguments in the `Script parameters:` section and click the `OK` button:

![PyCharm command line arguments](./img/pycharm_command_line_arguments.png)

### For other editors

1. Open your editor of choice.
2. Type the program code given in the example.
3. Save it as a file with the filename mentioned.
4. Run the interpreter with the command `python program.py` to run the program.

### Example: Using Variables And Literal Constants

Type and run the following program:

```python
# Filename : var.py
i = 5
print(i)
i = i + 1
print(i)

s = '''This is a multi-line string.
This is the second line.'''
print(s)
```

Output:

```
5
6
This is a multi-line string.
This is the second line.
```

**How It Works**

Here's how this program works. First, we assign the literal constant value `5` to the variable `i` using the assignment operator (`=`). This line is called a statement because it states that something should be done and in this case, we connect the variable name `i` to the value `5`. Next, we print the value of `i` using the `print` statement which, unsurprisingly, just prints the value of the variable to the screen.

Then we add `1` to the value stored in `i` and store it back. We then print it and expectedly, we get the value `6`.

Similarly, we assign the literal string to the variable `s` and then print it.

> **Note for static language programmers**
> 
> Variables are used by just assigning them a value. No declaration or data type definition is needed/used.

## Logical And Physical Line

A physical line is what you _see_ when you write the program. A logical line is what _Python sees_ as a single statement. Python implicitly assumes that each _physical line_ corresponds to a _logical line_.

An example of a logical line is a statement like `print 'hello world'` - if this was on a line by itself (as you see it in an editor), then this also corresponds to a physical line.

Implicitly, Python encourages the use of a single statement per line which makes code more readable.

If you want to specify more than one logical line on a single physical line, then you have to explicitly specify this using a semicolon (`;`) which indicates the end of a logical line/statement. For example:

```python
i = 5
print(i)
```

is effectively same as

```python
i = 5;
print(i);
```

which is also same as

```python
i = 5; print(i);
```

and same as

```python
i = 5; print(i)
```

However, I *strongly recommend* that you stick to *writing a maximum of a single logical line on each single physical line*. The idea is that you should never use the semicolon. In fact, I have _never_ used or even seen a semicolon in a Python program.

There is one kind of situation where this concept is really useful: if you have a long line of code, you can break it into multiple physical lines by using the backslash. This is referred to as _explicit line joining_:

```python
s = 'This is a string. \
This continues the string.'
print(s)
```

Output:

```
This is a string. This continues the string.
```

Similarly,

```python
i = \
5
```

is the same as

```python
i = 5
```

Sometimes, there is an implicit assumption where you don't need to use a backslash. This is the case where the logical line has a starting parentheses, starting square brackets or a starting curly braces but not an ending one. This is called *implicit line joining*. You can see this in action when we write programs using [list](./data_structures.md#lists) in later chapters.

## Indentation

Whitespace is important in Python. Actually, *whitespace at the beginning of the line is important*. This is called _indentation_. Leading whitespace (spaces and tabs) at the beginning of the logical line is used to determine the indentation level of the logical line, which in turn is used to determine the grouping of statements.

This means that statements which go together _must_ have the same indentation. Each such set of statements is called a *block*. We will see examples of how blocks are important in later chapters.

One thing you should remember is that wrong indentation can give rise to errors. For example:

```python
i = 5
# Error below! Notice a single space at the start of the line
 print('Value is', i)
print('I repeat, the value is', i)
```

When you run this, you get the following error:

```
  File "whitespace.py", line 3
    print('Value is', i)
    ^
IndentationError: unexpected indent
```

Notice that there is a single space at the beginning of the second line. The error indicated by Python tells us that the syntax of the program is invalid i.e. the program was not properly written. What this means to you is that _you cannot arbitrarily start new blocks of statements_ (except for the default main block which you have been using all along, of course). Cases where you can use new blocks will be detailed in later chapters such as the [control flow](./control_flow.md#control_flow).

> **How to indent**
> 
> Use four spaces for indentation. This is the official Python language recommendation. Good editors will automatically do this for you. Make sure you use a consistent number of spaces for indentation, otherwise your program will not run or will have unexpected behavior.

<!-- -->

> **Note to static language programmers**
> 
> Python will always use indentation for blocks and will never use braces. Run `from __future__ import braces` to learn more.

## Summary

Now that we have gone through many nitty-gritty details, we can move on to more interesting stuff such as control flow statements. Be sure to become comfortable with what you have read in this chapter.

