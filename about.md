# Apêndice: Colofão {#colophon}

Quase todo o software que eu utilizei na criação deste livro é [FLOSS](./floss.md#floss).

## Nascimento do Livro

No primeiro esboço deste livro, eu utilizei o Red Hat Linux 9.0 como base para minha configuração e no sexto esboço, eu utilizei o Linux Fedora Core 3 como base de minha configuração.

Inicialmente, eu utilizei KWord para escrever o livro (como explicado em [lição de história](./revision_history.md#history-lesson)).

## Anos da Adolescência

Mais tarde, eu mudei para DocBook XML utilizando Kate mas achei muito tedioso. Então, eu mudei para OpenOffice que foi excelente como o nível de controle que proporcionou para formatação bem como geração de PDF, mas o HTML produzido era bem desleixado.

Finalmente, eu descobri XEmacs e reescrevi o livro do zero em DocBook XML (novamente) após eu decidir que este formato foi a solução de longo prazo.

No sexto esboço, eu decidi usar Quanta+ para fazer toda a edição. O estilos XSL base que vinham com o Fedora Core 3 Linux foram utilizados. Todavia, escrevi um documento CSS para dar cor e estilo às páginas HTML. Eu também escrevi um anlisador léxico bruto, em Python óbvio, que automaticamente proporcionou destaque de sintaxe para toda a listagem de programa.

Para o sétimo esboço, eu utilizei [MediaWiki](http://www.mediawiki.org) como base de minha configuração. Eu costumava editar tudo online e os leitores podiam ler/editar/discutir diretamente no site wiki, mas acabei gastando mais tempo lutando contra spam que escrevendo.

Para o oitavo esboço, eu utilizei [Vim]({{ book.vimBookUrl }}), [Pandoc](http://johnmacfarlane.net/pandoc/README.html), e Mac OS X.

Para o nono esboço, eu troquei para [formato AsciiDoc](http://asciidoctor.org/docs/what-is-asciidoc/) e utilizei [Emacs 24.3](http://www.masteringemacs.org/articles/2013/03/11/whats-new-emacs-24-3/),
[tomorrow theme](https://github.com/chriskempson/tomorrow-theme),
[Fira Mono font](https://www.mozilla.org/en-US/styleguide/products/firefox-os/typeface/#download-primary) e [adoc-mode](https://github.com/sensorflo/adoc-mode/wiki) para escrever.

## Agora

2016: cansei de diversas pequenas falhas de renderização em AsciiDoctor, como o `++` em `C/++` desaparecer e era muito difícil manter controle de escapar tais coisas mínimas. Ademais, tornei-me relutante em alterar o texto devido à complexidade do formato Asciidoc.

Para o décimo esboço, eu troquei para o formato Markdown + [GitBook](https://www.gitbook.com), usando o [editor Spacemacs](http://spacemacs.org).

## Sobre o Autor

Veja {{ book.authorUrl }}
