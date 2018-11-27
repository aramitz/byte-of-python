# Primeiros Passos

Agora veremos como executar o tradicional programa 'Hello World' em Python. Isto ensinará a você como escrever, salvar e executar programas em Python.

Há dois modos de utilização do Python para executar seu programa - usando o prompt do interpretador interativo ou usando um arquivo fonte. Veremos agora como usar ambos.

## Usando o Prompt do Interpretador

Abra o terminal em seu sistema operacional (como discutido previamente no capítulo [Instalação](./installation.md#installation)) e então abra o prompt Python digitando `python3` e pressionando a tecla `[enter]`.

Assim que você tiver iniciado o Python, você deverá ver `>>>`, onde você pode começar a digitar coisas. Isto é chamado _prompt do interpretador Python_.

No prompt do interpretador Python, digite:

```python
print("Hello World")
```

seguindo da tecla `[enter]`. Você deverá ver as palavras `Hello World` exeibidas na tela.

Aqui está um exemplo do que você deverá ver, quando usar um computador com Mac OS X. Os detalhes sobre o software Python serão diferentes conforme seu computador, mas a parte a partir do prompt (isto é, dos caracteres `>>>` em diante) deverão ser os mesmos independentemente de sistema operacional.

<!-- The output should match pythonVersion variable in book.json -->
```python
$ python3
Python 3.6.0 (default, Jan 12 2017, 11:26:36)
[GCC 4.2.1 Compatible Apple LLVM 8.0.0 (clang-800.0.38)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> print("Hello World")
Hello World
```

Perceba que o Python te dá a saída da linha imediatamente! O que você acabou de informar é um simples _comando_ Python. Usamos `print` para (sem surpresa aqui) imprimir qualquer valor que você fornecer para ela. Aqui, fornecemos o texto `Hello World` e isso é rapidamente impresso na tela.

### Como Encerrar a Sessão do Interpretador

Se você estiver usando um shell GNU/Linux ou OS X, você pode encerrar a sessão pressionando `[ctrl + d]` ou digitando `exit()` (nota: lembre-se de incluir os parênteses, `()`) seguindo da tecla `[enter]`.

Caso você esteja usando o prompt de comandos do Windows, pressione `[ctrl + z]` seguido da tecla `[enter]`.

## Escolhendo um Editor

Não podemos digitar todo o nosso programa no prompt do interpretador a cada vez que quisermos executar algo, logo temos de salvá-lo em arquivos e assim poderemos executar nossos programas qualquer número de vezes.

Para criar nossos arquivos-fonte em Python, precisamos de um programa editor onde você consiga digitar e salvar o conteúdo. Um editor de programaçãofacilitará sua vida no momento de escrever os arquivos-fonte. COnsequentemente, a escolha de um editor é de suma importância. Você deve escolher um editor da mesma forma que você escolheria um carro antes de comprá-lo. Um bom editor lhe ajudará a escrever programas em Python facilmente, fazendo com que sua jornada seja mais confortável e auxiliando-lhe a alcançar seu destino (atingir sua meta) de modo muito mais rápido e seguro.

Um dos requisitos mais básicos é o suporte ao _destaque de sintaxe_ onde as diferentes partes de seu programa Python são colorizadas de forma que você _vê_ seu programa e visualiza sua estrutura.

Se você não tem ideia onde começar, recomendo usar a [Edição Educacional do PyCharm](https://www.jetbrains.com/pycharm-edu/) disponível para Windows, Mac OS X e GNU/Linux. Detalhes na próxima seção.

Se você utiliza o Windows, *não use o Notepad* - é uma péssima escolha porque ele não oferece suporte a indentação do texto o que é muito importante como veremos mais tarde. Bons editores fazem isso de forma automática.

If you are an experienced programmer, then you must be already using [Vim](http://www.vim.org) or [Emacs](http://www.gnu.org/software/emacs/). Needless to say, these are two of the most powerful editors and you will benefit from using them to write your Python programs. I personally use both for most of my programs, and have even written an [entire book on Vim]({{ book.vimBookUrl }}).

In case you are willing to take the time to learn Vim or Emacs, then I highly recommend that you do learn to use either of them as it will be very useful for you in the long run. However, as I mentioned before, beginners can start with PyCharm and focus the learning on Python rather than the editor at this moment.

To reiterate, please choose a proper editor - it can make writing Python programs more fun and easy.

## PyCharm {#pycharm}

[PyCharm Educational Edition](https://www.jetbrains.com/pycharm-edu/) is a free editor which you can use for writing Python programs.

When you open PyCharm, you'll see this, click on `Create New Project`:

![When you open PyCharm](./img/pycharm_open.png)

Select `Pure Python`:

![PyCharm New Project](./img/pycharm_create_new_project.png)

Change `untitled` to `helloworld` as the location of the project, you should see details similar to this:

![PyCharm project details](./img/pycharm_create_new_project_pure_python.png)

Click the `Create` button.

Right-click on the `helloworld` in the sidebar and select `New` -> `Python File`:

![PyCharm -> New -> Python File](./img/pycharm_new_python_file.png)

You will be asked to type the name, type `hello`:

![PyCharm New File dialog box](./img/pycharm_new_file_input.png)

You can now see a file opened for you:

![PyCharm hello.py file](./img/pycharm_hello_open.png)

Delete the lines that are already present, and now type the following:

<!-- TODO: Update screenshots for Python 3 -->

```python
print("hello world")
```
Now right-click on what you typed (without selecting the text), and click on `Run 'hello'`.

![PyCharm Run 'hello'](./img/pycharm_run.png)

You should now see the output (what it prints) of your program:

![PyCharm output](./img/pycharm_output.png)

Phew! That was quite a few steps to get started, but henceforth, every time we ask you to create a new file, remember to just right-click on `helloworld` on the left -> `New` -> `Python File` and continue the same steps to type and run as shown above.

You can find more information about PyCharm in the [PyCharm Quickstart](https://www.jetbrains.com/pycharm-educational/quickstart/) page.

## Vim

1. Install [Vim](http://www.vim.org)
    * Mac OS X users should install `macvim` package via [HomeBrew](http://brew.sh/)
    * Windows users should download the "self-installing executable" from [Vim website](http://www.vim.org/download.php)
    * GNU/Linux users should get Vim from their distribution's software repositories, e.g. Debian and Ubuntu users can install the `vim` package.
2. Install [jedi-vim](https://github.com/davidhalter/jedi-vim) plugin for autocompletion.
3. Install corresponding `jedi` python package : `pip install -U jedi`

## Emacs

1. Install [Emacs 24+](http://www.gnu.org/software/emacs/).
    * Mac OS X users should get Emacs from http://emacsformacosx.com
    * Windows users should get Emacs from http://ftp.gnu.org/gnu/emacs/windows/
    * GNU/Linux users should get Emacs from their distribution's software repositories, e.g. Debian and Ubuntu users can install the `emacs24` package.
2. Install [ELPY](https://github.com/jorgenschaefer/elpy/wiki)

## Using A Source File

Now let's get back to programming. There is a tradition that whenever you learn a new programming language, the first program that you write and run is the 'Hello World' program - all it does is just say 'Hello World' when you run it. As Simon Cozens[^1] says, it is the "traditional incantation to the programming gods to help you learn the language better."

Start your choice of editor, enter the following program and save it as `hello.py`.

If you are using PyCharm, we have already [discussed how to run from a source file](#pycharm).

For other editors, open a new file `hello.py` and type this:

```python
print("hello world")
```

Where should you save the file? To any folder for which you know the location of the folder. If you
don't understand what that means, create a new folder and use that location to save and run all
your Python programs:

- `/tmp/py` on Mac OS X
- `/tmp/py` on GNU/Linux
- `C:\py` on Windows

To create the above folder (for the operating system you are using), use the `mkdir` command in the terminal, for example, `mkdir /tmp/py`.

IMPORTANT: Always ensure that you give it the file extension of `.py`, for example, `foo.py`.

To run your Python program:

1. Open a terminal window (see the previous [Installation](./installation.md#installation) chapter on how to do that)
2. **C**hange **d**irectory to where you saved the file, for example, `cd /tmp/py`
3. Run the program by entering the command `python hello.py`. The output is as shown below.

```
$ python hello.py
hello world
```

![Screenshot of running program in terminal](./img/terminal_screenshot.png)

If you got the output as shown above, congratulations! - you have successfully run your first Python program. You have successfully crossed the hardest part of learning programming, which is, getting started with your first program!

In case you got an error, please type the above program _exactly_ as shown above and run the program again. Note that Python is case-sensitive i.e. `print` is not the same as `Print` - note the lowercase `p` in the former and the uppercase `P` in the latter. Also, ensure there are no spaces or tabs before the first character in each line - we will see [why this is important](./basics.md#indentation) later.

**How It Works**

A Python program is composed of _statements_. In our first program, we have only one statement. In this statement, we call the `print` _statement_ to which we supply the text "hello world".

## Getting Help

If you need quick information about any function or statement in Python, then you can use the built-in `help` functionality. This is very useful especially when using the interpreter prompt. For example, run `help('len')` - this displays the help for the `len` function which is used to count number of items.

TIP: Press `q` to exit the help.

Similarly, you can obtain information about almost anything in Python. Use `help()` to learn more about using `help` itself!

In case you need to get help for operators like `return`, then you need to put those inside quotes such as `help('return')` so that Python doesn't get confused on what we're trying to do.

## Summary

You should now be able to write, save and run Python programs at ease.

Now that you are a Python user, let's learn some more Python concepts.

---

[^1]: the author of the amazing 'Beginning Perl' book
