# Instalação {#installation}

Ao nos referirmos a "Python 3" neste livro, estaremos sempre referindo a qualquer versão de Python igual ou maior que versão [Python {{ book.pythonVersion }}](https://www.python.org/downloads/).

## Instalação no Windows

Visite https://www.python.org/downloads/ e baixe a última versão. No momento da escrita deste livro, era a versão 3.7.1. A instalação é como qualquer outra instalação de software para Windows.

Atente que se sua versão é anterior ao Vista, você deverá  [baixar o Python 3.4 exclusivamente](https://www.python.org/downloads/windows/) uma vez que  as útimas versões exigem versões mais recentes do Windows.

ATENÇÃO: Certifique-se que marcar a opção `Adicionar Python 3.7 ao PATH`.

Para altera o local da instalação, clique em `Personalizar instalação`, então `Próximo` e informe `C:\python37` (ou outro local adequado) como local de instalação.

Se você não marcou a opção `Adicionar Python 3.7 ao PATH` anteriormente, marque `Adicionar Python às variáveis de ambiente`. Isto faz exatamente o mesmo que a opção `Adicionar Python 3.7 ao PATH` presente na primeira tela da instalação.

Você pode escolher instalar o Lançador para todos os usuários ou não. Isso não importa muito. O Lançador é usado para alterar entre as diversas versões de Python instaladas no sistema.

Se o seu _path_ não foi definido corretamente (marcando a opção `Adicionar Python 3.7 ao Path` ou (`Adicionar Python às variàveis de ambiente`), siga os passos na próxima seção (`prompt DOS`) para corrigí-lo. Caso contrário, vá para a seção `Executando o prompt do Python no Windows` neste documento.

NOTA: Para pessoas que já sabem programação, se você tiver familiaridade com o Docker, veja [Python emno Docker](https://hub.docker.com/_/python/) e [Docker no Windows](https://docs.docker.com/windows/).

### Prompt DOS {#dos-prompt}

Se você quer usar o Python a partir da linha de comando do Windows, isto é, o  prompt DOS, você precisa definir a variável PATH apropriadamente.

Para WIndows 2000, XP, 2003 clique em `Painel de Controle` -> `Sistema` -> `Avançado` -> `Variáveis de Ambiente`. Clique na variável chamada `PATH` em _Variáveis de sistema_, selecione `Alterar` e adicione `;C:Python37` (por favor confirme a existência da para, será diferente para as novas versões do Python) no fim do texto já definido lá. Obviamente, use o nome de diretório adequado.

<!-- The directory should match pythonVersion variable in book.json -->
Para versões anteriores do Windows, abra o arquivo `C:\AUTOEXEC.BAT` e acrescente a linha `PATH=%PATH%;C:\Python37` e reinicie o sistema. Para Windows NT, use o arquivo `AUTOEXEC.NT`.

Para Windows Vista:

- Clique Iniciar e selecione `Painel de Controle`
- Clique em Sistema, à direita você verá "Exibir informaç`oes básicas sobre seu computador"
- À esquerda há uma lista de tarefas, a última é `Configuração avançada de sistema`. CLique nela.
- A aba `Avançado` da caixa de diálogo `Propriedades do Sistema` é exibida. Clique no botão `Variáveis de Ambiente` exibido na parte inferior à direita.
- Na caixa menor intitulada `Variáveis de Sistema` role até encontra Path e clique no botão `Alterar`.
- Altere seu _path_ como for necessário.
- Reinicie seu sistema. O Vista não reconhecerá o novo _path_ até que seja reiniciado.

Para Windows 7 e 8:

- Clique com o botão direito no ícone Computador em sua área de trabalho e selecione `Propriedades` ou clique em `Iniciar` e selecione `Painel de Controle` -> `Sistema e Segurança` -> `Sistema`. Clique em `Configurações avançadas do sistema` no lado esquerdo e então clique na aba `Avançado`. Na parte inferior clique em `Variáveis de Ambiente`, procure pela variável `PATH`, selecione-a e então pressione `Alterar`.
- Vá para o fim da linha no campo Variável e acrescente `;C:\Python37` (por favor certifique-se da existência desta pasta, será diferente em versões mais recentes do Python) ao conteúdo que já estiver lá. Use um nome adequado para a pasta.
- Se o valor era `%SystemRoot%\system32;` será agora `%SystemRoot%\system32;C:\Python37` <!-- The directory should match pythonVersion variable in book.json -->
- Clique `OK` e está feito. Não é necessário reiniciar, mas você terá de fechar e reabrir a linha de comandos.

Para Windows 10:

Menu Iniciar do Windows > `Configurações` > `Sobre` > `Informações do Sistema` > `Configurações Avançadas de Sistema` > `Variáveis de Ambiente` (fica próximo a parte inferior da tela) > (destaque a variável `Caminho` e clique em `Alterar`) > `Novo` > (digite conforme seja a localização de sua instalação do Pytho. Por exemplo, `C:\Python37\`)


### Executando o prompt do Python no Windows

Para usuários Windows, você pode executar o interpretador na linha de comando se você tiver [definido a variável `PATH` adequadamente](#dos-prompt).

Para abrir o terminal no Windows, clique o botão iniciar e clique `Executar`. Na caixa de diálogo, digite `cmd` e pressione a tecla `[enter]`.

Em seguida, digite `python` e verifique se não há erros.

## Instalação no Mac OS X

Para usuários Mac OS x, use [Homebrew](http://brew.sh): `brew install python3`.

Para verificar, abra o terminal pressionado as teclas `[Command + Space]` (para abrir a busca Spotlight), digite `Terminal` e veja se não há erros.

## Instalação em GNU/Linux

Para usuários GNU/Linux, use o gerenciador de pacotes da sua distribuição para instalar o Python3, por exemplo, no Debian & Ubuntu: `sudo apt-get update && sudo apt-get install python3`.

Para verificar, abra o terminal executando a aplicação `Terminal` ou pressionando `Alt + F2` e informando `gnome-terminal`. Se não funcionar, por gentileza, consulte a documentação da sua distribuição GNU/Linux. Agora, execute `python3` e veja se não há erros.

Você pode ver a versão do Python na tela executando:

<!-- The output should match pythonVersion variable in book.json -->
```
$ python3 -V
Python 3.6.0
```

NOTA: `$` é o prompt do shell. Será diferente para você dependendo das definicções do sistema operacional em seu computador, por isso indicarei o prompt usando apenas o símbolo `$`.

CUIDADO: A saída poderá ser diferente em seu computador dependendo da versão do Python instalada em seu computador.

## Sumário

Daqui em diante, assumiremos que você possui o Python instalado em seu sistema.

A seguir, escreveremos nosso primeiro programa em Python.
