# Sobre Python

Python é uma daquelas raras linguagens que pode reivindicar ser ao mesmo tempo _simples_ e _poderosa_. Você se encontrará prazerosamente surpreso em ver como é concentra na solução do problema em vez da sintaxe e estrutura da linguagem em que você está programando.

A introdução oficial para Python é:

> Python é uma linguagem poderosa e fácil para aprender. Ela possui estruturas de dados eficientes de alto nível e uma abordagem simples porém efetiva para programação orientada a objetos. A sintaxe elegante e a tipagem dinâmica do Python, junto com sua natureza interpretada, fazem-na uma linguagem ideal para codificação de script e desenvolvimento rápido de aplicações em muitas áreas na maioria das plataformas.

Eu discutirei a maioria dessas características em mais detalhes na próxima seção.

## A estória por trás do nome

Guido van Rossum, o criador da linguagem Python, nomeou a linguagem após o show da BBC "Monty Python's Flying Circus". Ele particularmente não gosta de cobras que matam animais para comer enrolando seus corpos compridos ao redor deles esmagando-os.

## Caraterísticas do Python

### Simples

Python é uma linguagem simples e minimalista. Ler um programa Python bom é quase como ler em inglês, embora um inglês bem estrito! Essa natureza de pseudo-código do Python é uma de suas maiores forças. Ela permite a você concentrar na solução para o problema em vez da linguagem em si.

### Fácil para Aprender

Como você verá. Python é extremamente fácil para se começar. Python possui uma sintaxe extraordinariamente simple, como já mencionado.

### Livre e de Código Aberto

Python é um exemplo de um _FLOSS_ (Free/Libré e Open Source Software). De modo simples, você pode distribuir cópias deste software livremente, ler seu código fonte, efetuar mudanças e utilizar pedações dele em novos programas livres. FLOSS é baseado no conceito de uma comunidade que compartilha conhecimento. Esta é uma das razões porque Python é tão boa - foi criada e é constantemente aperfeiçoada por uma comunidade que apenas deseja ver uma linguagem Python melhor.

### Linguagem de Alto Nível

Ao escrever programas em Python, você nunca precisará preocupar-se a respeito de detalhes de baixo nível tais como gerenciar a memória utilizada por seu programa, etc.

### Portátil

Dada a sua natureza de código-aberto, Pytho foi portada para (isto é, alterada para fazê-la funcionar em) muitas plataformas. Todos os seus programas em Python podem executar em quaisquer uma dessas plataformas sem mudanças requeridas se você tiver cuidado o suficiente para evitar quaisquer funcionalidades dependentes de sistema específico.

Você pode utilizar Python em GNU/Linux, Windows, FreeBSD, Macintosh, Solaris, OS/2, Amiga, AROS, AS/400, OS/390, z/OS, Palm OS, QNX, VMS, Psion, Acorn RISC OS, VxWorks, PlayStation, Sharp Zaurus, Windows CE e PocketPC!

Você pode até mesmo utilizar uma plataforma como [Kivy](http://kivy.org) para criar jogos para o seu computador _e_ para iPhone, iPad, and Android.

### Interpretada

Isto requer um pouco de explicação.

Um programa escrito em uma linguagem compilada como C ou C\++ é convertida da linguagem fonte, isto é, C ou C++ em uma linguagem que é falada pelo seu computador (código binário, isto é, 0s e 1s) usando um compilador com vários marcadores e opções. Quando você executa o programa, o software ligador/carregador copia o programa do disco rígido para a memória e começa a rodá-lo.

Python, por sua vez, não necessita compilação para binário. Você apenas _roda_ o programa diretamente do código fonte. Internamente, Python converte o código fonte em uma forma intermediária chamada de bytecodes e então traduz isso em uma linguagem nativa do seu computador e então a executa. Tudo isso, na verdade, torna a utilização do Python muito fácil uma vez que você não tem que se preocupar em compilar o programa, certificar-se que as bibliotecas adequadas são ligadas e carregadas, etc. Isso também torna os programas Python muito mais portáveis, uma vez que você pode apenas copiar seu programa em Python para outro computador e ele simplesmente funciona!

### Orientado a Objetos

Python possui suporte a programação procedural bem como a programação orientada a objetos. Em linguagens _orientadas a procedimento_, o programa é construído ao redor de procediemntos e funcções que são nada mais nada menos que peças reutilizáveis dos programas. Em linguagens _orientadas a objetos_, o programa é construído ao redor de objetos que combinam dados e funcionalidade. Python possui um modo muito poderoso porém simples de fazer OOP, especialmente quando comparado com linguagens grandes como C++ ou Java.

### Extensível

Se você precisa de um pedaço crítico de código para executar rapidamente ou que ter algum pedaço de algoritmo não aberto, você pode codificar esta parte de seu programa em C ou C\++ e então utilizá-la em seu programa Python.

### Embarcável

Você pode embarcar Python em seus programas C/C\++ para fornecer funcionalidades de _scripting_ para os usuários de seu programa.

### Extensa Biblioteca

A Biblioteca Padrão do Python é certamente imensa. Ela pode te auxiliar a fazer várias coisas envolvendo expressões regulares, geração de documentação, teste de unidade, threading, bancos de dados, navegadores web, CGI, FTP, email, XML, XML-RPC, HTML, arquivos WAV, criptografia, GUI (interface gráfica de usuário) e outras coisas dependentes de sistema. Lembre-se, tudo isto está sempre disponível onde Python estiver instalado. Isto é chamado de filosofia _Baterias incluídas_ do Python.

Além da biblioteca padrão, há várias outras bibliotecas de alta qualidade que você pode encontrar no [Python Package Index](http://pypi.python.org/pypi).

### Sumário

Python é de fato uma linguagem excitante e poderosa. Ela possui a combinação certa de desempenho e características que fazem escrever programas em Python divertido e fácil.

## Python 3 versus 2

Você pode ignorar esta seção se você não estiver interessado na diferença entre "Python versão 2" e "Python versão 3". Mas por favor esteja ciente da versão que está usando. Este livro foi escrito para a versão 3 do Python.

Lembre-se que uma vez que você tenha compreendido e aprendido adequadamente a utilizar uma versão, você pode facilmente aprender as diferenças e utilizar a outra versão. A parte difícil é aprender programação e compreender o básico da linguagem Python em si. Este é nosso objetivo neste livro, e uma vez que você alcance esse objetivo, você pode facilmete utilizar Python 2 ou Python 3 dependendo de sua situação.

Para detalhes das diferenças entre Python 2 e Python 3, veja (em inglês):

- [O Futuro de Python 2](http://lwn.net/Articles/547191/)
- [Portando Código Python 2 Para Python 3](https://docs.python.org/3/howto/pyporting.html)
- [Escrevendo código que execute tanto em Python2 e 3](https://wiki.python.org/moin/PortingToPy3k/BilingualQuickRef)
- [Fornecendo Suporte à Python 3: Um guia detalhado](http://python3porting.com)

## O que os Programadores Dizem

Você pode achar interessante ler o que grandes hackers como ESR tem a dizer sobre Python:

- _Eric S. Raymond_ é o autor de "The Cathedral and the Bazaar" e também a pessoa que cunhou o termo _Código Aberto_. Ele disse que [Python tornou-se sua linguagem de programação favorita](http://www.python.org/about/success/esr/). Este artigo foi a inspiração real para meu primeiro encontro com Python.
- _Bruce Eckel_ é o autor dos famosos livros 'Thinking in Java' e 'Thinking in C++'. Ele disse que nenhuma linguagem fez ele tão produtivo quanto Python. Ele disse que Python é talvez a única linguagem que foca em tornar as coisas fáceis para o programador. Leia [a entrevista completa](http://www.artima.com/intv/aboutme.html) para maiores detalhes.
- _Peter Norvig_ é um autor bem conhecido de Lisp e Diretor de Pesquisa de Qualidade da Google (agradeço a Guido van Rossum pela informação). Ele disse que [escrever Python é como escrever em pseudocódigo](https://news.ycombinator.com/item?id=1803815). Ele disse que Python foi sempre uma parte integral da Google. Você pode na realidade verificar essa declaração olhando na página [Google Jobs](http://www.google.com/jobs/index.html) que lista conhecimento em Python como um requisito para engenheiros de software.
