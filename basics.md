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

Se você precisa especificar algumas cadeias de caracteres onde nenhum processamento especial precisa ser feito, como manipulação de sequências de escape, então tudo que você precisa é especificar uma cadeia de caracteres bruta (_raw_) prefixando-a com `r` ou `R`. Um exemplo é:

```python
r"Novas linhas são indicadas por \n"
```

> **Nota para Usuários de Expressões Regulares**
> 
> Sempre utilize cadeias de caracteres brutas ao lidar com expressões regulares. De outra forma, um número excessivo de barras invertidas será necessário. Por exemplo, _backreferences_ podem ser referidas como `\\'1` ou `\1'`.

## Variável

Utilizar somente constantes literais pode tornar-se rapidamente tedioso - necessitamos de algum meio para armazenar qualquer informação e manipular esses valores. Nesse momento as _variáveis_ entram em cena. Variáveis são exatamente o que o nome implica - seu valor pode variar, isto é, você pode armazenar qualquer coisa utilizando uma variável. Variáveis são apenas partes da memória de seu computador onde você armazena alguma informação. Ao contrário de constantes literais, você precisa de algum método para acessar estas variáveis e assim elas recebem nomes.

## Nomeação de Identificadores

Variáveis são exemplos de identificadores. _Identificadores_ são nomes dados para identificar _algo_. Há algumas regras que você tem de seguir para nomear identificadores:

- O primeiro caractere do identificador deve ser uma letra do alfabeto (caracteres ASCII maiúsculos e minúsculos ou caracteres Unicode) ou um sublinha (`_`).
- O restante do nome do identificador pode consistir de letras (caracteres ASCII maiúsculos e minúsculos ou caracteres Unicode), sublinhas (`_`) ou dígitos (0-9).
- Nomes de identificadores diferenciam maiúsculas de minúsculas. Por exemplo, `meunome` e `meuNome` não são a mesma coisa. Note o `n` minúsculo no primeiro e o `N` maiúsculo no último.
- Exemplos de nomes de identificadores _válidos_ são `i`, `nome_2_3`. Exemplos de nomes de identificadores _inválidos_ são `2coisas`, `isto está espaçado`, `meu-nome` e `>a1b2_c3`.


## Tipos de Dados

Variáveis podem armazenar valores de tipos diferentes chamados _tipos de dados_. Os tipos básicos são números e cadeias de caracteres, sobre os quais já discutimos. Em capítulos posteriores, veremos como criar nossos próprios tipos usando [classes](./oop.md#classes).

## Objetos

Lembre-se, Python refere-se a tudo que é utilizado em um programa como um _objeto_. Isto é entendido em sentido genérico. Ao invés de dizer "o _alguma coisa_", dizemos "o _objeto_".

> **Nota para usuários de Programação Orientada a Objetos**:
>
> Python é fortemente orientado a objetos no sentido de que tudo é um objeto incluindo números, cadeias de caracteres e funções.

Veremos agora como usar variáveis juntamente com constantes literais. Salve o exemplo seguinte e execute o programa.

## Como escrever programas em Python

Daqui em diante, o procedimento padrão para salvar e executar um programa em Python é o seguinte:

### Para PyCharm

1. Abra o [PyCharm](./first_steps.md#pycharm).
2. Crie um novo arquivo com o nome informado.
3. Digite o código do programa dado no exemplo.
4. Clique com o botão direito e execute o arquivo corrente.

NOTA: Sempre que você tiver que fornecer [argumentos de linha de comando](./modules.md#modules), clique em `Run` -> `Edit Configurations` e digite o tipo dos argumentos na seção `Script parameters:` e clique no botão `OK`:

![argumentos de linha de comando no PyCharm](./img/pycharm_command_line_arguments.png)

### Para outros editores

1. Abra seu editor de preferência.
2. Digite o código do programa dado no exemplo.
3. Salve-o como um arquivo com o nome mencionado.
4. Execute o interpretador com o comando `python program.py` para executar o programa.

### Exemplo: Usando Variáveis e Constantes Literais

Digite e execute o seguinte programa:

```python
# Arquivo : var.py
i = 5
print(i)
i = i + 1
print(i)

s = '''Isto é uma cadeia de caracteres de múltiplas linhas.
Esta é a segunda linha.'''
print(s)
```

Saída:

```
5
6
Isto é uma cadeia de caracteres de múltiplas linhas.
Esta é a segunda linha.
```

**Como Funciona**

Aqui está como o programa funciona. Primeiro, atribuímos a constante literal `5` à variável `i` usando o operador de atribuição (`=`). Esta linha é chamada uma declaração porque ela declara que algo deve ser feito e neste caso, conectamos a variável de nome `i` ao valor `5`. Em seguida, exibimos o valor de `i` usando o comando `print`, o qual, surpreendentemente, apenas exibe o valor da variável na tela.

Após isso, adicionamos `1` ao valor armazenado em `i` e armazenamos o valor novamente. Então imprimimos o valor e de forma esperada, obtemos o valor `6`.

De maneira similar, atribuímos a cadeia de caracteres literal à variável `s` e a exibimos.

> **Nota para programadores de linguagens estáticas**
> 
> Variáveis são usadas pela simples atribuição de um valor a elas. Nenhuma declaração ou definição de tipo de dados é necessária/utilizada.

## Linha Lógica e Linha Física

Uma linha física é o que você _vê_ quando escreve o programa. Uma linha lógica é o que _Python vê_ como um simples comando. Python implícitamente assume que cada _linha física_ corresponde a uma _linha lógica_.

Um exemplo de uma linha lógica é um comando como `print 'hello world'` - se isto estiver em uma única linha (assim como você vê no editor), então isso corresponde também a uma linha física.

Implícitamente, Python encoraja o uso de um simples comando por linha o que torna o código mais legível.

Se você quer especificar mais de uma linha lógica em uma simples linha física, então você tem de especificar explícitamente isto usando um ponto e vírgula (`;`) que indica o fim de uma linha/comando lógico. Por exemplo:

```python
i = 5
print(i)
```

efetivamente é o mesmo que

```python
i = 5;
print(i);
```

o qual é também o mesmo que

```python
i = 5; print(i);
```

e o mesmo que

```python
i = 5; print(i)
```

Porém, eu *recomendo fortemente* que você fique com *escrever o máximo de uma simples linha lógica em cada simples linha física*. A ideia é que você nunca deve usar o ponto e vírgula. De fato, eu _nunca_ usei ou vi um ponto e vírgula em um programa Python.

Há um tipo de situação onde este conceito é realmente útil: se você tiver uma linha longa de código você pode quebrá-la em múltiplas linhas físicas usando a barra invertida. Isto é referido como _agrupamento de linha explícita_:

```python
s = 'Isto é uma cadeia de caracteres. \
Isto continua a cadeia de caracteres.'
print(s)
```

Saída:

```
Isto é uma cadeia de caracteres. Isto continua a cadeia de caracteres.
```

De forma análoga,

```python
i = \
5
```

é o mesmo que

```python
i = 5
```

Às vezes, há uma suposição implícita onde você não precisa utilizar uma barra invertida. Este é o caso onde a linha lógica possui um parêntese inicial, um colchete inicial ou uma chave inicial mas sem um no final. Isto é chamado *agrupamento implícito de linha*. Você pode ver isso em ação quando escrevemos programas usando [list](./data_structures.md#lists) em capítulos posteriores.

## Indentação

Espaço em branco é importante em Python. Na realidade, *espaço em branco no início da linha é importante*. Isto é chamado _indentação_. Espaço em branco inicial (espaços e tabulações) no início de uma linha lógica é usado para determinar o nível de indentação da linha lógica, o qual por sua vez é utilizado para determinar o agrupamento dos comandos.

Isto significa que comandos que seguem juntos _devem_ ter a mesma indentação. Cada conjunto de comandos é chamado *bloco*. Veremos exemplos de como os blocos são importantes em capítulos posteriores.

Uma coisa que você deve lembrar é que indentação errada pode dar origem a erros. Por exemplo:

```python
i = 5
# Erro abaixo! Perceba um espaço simples no início da linha
 print('Valor é', i)
print('Eu repito, o valor é', i)
```

Ao executar isso, você obtem o seguinte erro:

```
  File "whitespace.py", line 3
    print('Value is', i)
    ^
IndentationError: unexpected indent
```

Perceba que há um espaço simples no início da segunda linha. O erro indicado pelo Pythonnos informa que a sintaxe do programa está inválida, isto é, o programa não foi escrito adequadamente. O que isso significa para você é que _você não pode iniciar de forma arbitrária novos blocos de comandos_ (exceto para o bloco principal que você esteja usando, obviamente). Os casos onde você pode usar novos blocos será detalhado em capítulos posteriores como no [controle de fluxo](./control_flow.md#control_flow).

> **Como indentar**
> 
> Use quatro espaços para indentação. Esta é a recomendação oficial da linguagem Python. Bons editores automaticamente farão isso por você. Certifique-se de usar um número consistente de espaços para indentação, ao contrário seu programa não irá rodar ou apresentará um comportamento anormal.

<!-- -->

> **Nota para programadores de linguagens estáticas**
> 
> Python sempre usa indentação para e blocos e nunca usará chaves. Execute `from __future__ import braces`para aprender mais.

## Sumário

Agora que seguimos através de muitos detalhes minuciosos, podemos mover-nos para coisas mais interessantes como comandos para controle de fluxo. Certifique-se de estar confortável com o que você leu neste capítulo.
