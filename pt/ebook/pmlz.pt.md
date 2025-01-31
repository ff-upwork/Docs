{
  "date" : "2021-03-30",
  "keywords" :[ "PMLZ", "Arquivo de linguagem de marcação Palm com compactação", "extensão", "Arquivo", "formato", "eBook", "Linguagem de marcação Palm" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo PMLZ, Palm Markup Language e APIs que podem criar e abrir arquivos PMLZ.",
  "title" :"PMLZ - Arquivo compactado em linguagem de marcação Palm",
  "linktitle" : "PMLZ",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-30"
}

## O que é um arquivo PMLZ?

A Palm Inc introduziu um tipo de arquivo eBook; conhecido como o formato de arquivo PMLZ, que é uma versão compactada do formato de arquivo [PML](/pt/ebook/pml/) é por isso que os arquivos com extensões .pmlz são conhecidos como **Arquivo de linguagem de marcação de palma compactado**. O arquivo PMLZ é apenas um contêiner zip de um arquivo que compila arquivos [PDB](/pt/programming/pdb/) para criar documentos para **eReader** (conhecido como um dispositivo de leitura de e-books, como um tablet). O arquivo PML fornece o layout de um arquivo PDB (contendo vários arquivos de dados) para exibição em um dispositivo Palm. Considerando que um arquivo PDB é um arquivo de banco de dados, que é usado por vários aplicativos, incluindo Quicken, Pegasus, Microsoft Visual Studio e Palm Pilot. Em suma, um PMLZ é um contêiner compactado de arquivos PML e PDB.


## Conhecimento sobre a linguagem de marcação Palm
A tabela a seguir especifica os comandos PML:

|Comando|Descrição|
---|---|
| \p | Nova página |
| \x | Novo capítulo; também causa uma nova quebra de página. Coloque o título do capítulo (e quaisquer códigos de estilo) com \x e \x |
| \Xn | Novo capítulo, recuado n níveis (n entre 0 e 4 inclusive) na caixa de diálogo Capítulo; não causa quebra de página. Coloque o título do capítulo (e quaisquer códigos de estilo) com \Xn e \Xn |
| \Cn="Título do capítulo" | Insira "título do capítulo" na listagem de capítulos, com nível n (como \Xn). O texto não é mostrado na página e não força uma quebra de página. Às vezes, isso pode ser útil para inserir uma marca de capítulo no início de uma introdução ao capítulo, por exemplo. |
| \c | Centralize este bloco de texto; fechar com \c no início da linha |
| \r | Bloco de texto justificado à direita; fechar com \r no início da linha |
| \i | Bloco em itálico; fechar com \i |
| \u | Bloco de sublinhado; fechar com \u |
| \o | Bloqueio de sobreposição; fechar com \o |
| \v | Texto invisível; feche com \v (pode ser usado para comentários) |
| \t | Bloco de recuo. Comece no início de uma linha, feche com \t no final de uma linha |
| \T="50%" | Recua a porcentagem especificada da largura da tela, 50% neste caso. Se a posição de desenho atual já estiver além da localização da tela especificada, esta tag será ignorada. |
| \w="50%" | Incorpore uma régua horizontal de uma determinada largura percentual da tela, neste caso 50%. Essa tag causa uma quebra de linha antes e depois dela. A regra é centralizada. O sinal de porcentagem é obrigatório. |
| \n | Mude para a fonte "normal", que é especificada pelo usuário |
| \s | Mude para stdFont; feche com \s para voltar à fonte normal |
| \b | Mude para boldFont; feche com \b para reverter para fonte normal (obsoleto; use \B em vez disso) |
| \l | Mude para largeFont; feche com \l para reverter para fonte normal |
| \B | Marcar o texto como negrito. Ao contrário da tag \b, \B não altera a fonte, então você pode ter um texto grande em negrito. Você não pode misturar \b e \B no mesmo arquivo PML. |
| \Sp | Marcar o texto como sobrescrito. Não deve ser misturado com outros estilos, como negrito, itálico, etc. Coloque o texto sobrescrito com \Sp. |
| \Sb | Marcar o texto como subscrito. Não deve ser misturado com outros estilos como negrito, itálico, etc. Coloque o texto subscrito com \Sb. |
| \k | Transforme o texto incluído em letras minúsculas; feche com \k. Quaisquer caracteres incluídos em tags \k (incluindo aqueles com acentos) são maiúsculos e são renderizados em um tamanho de ponto menor do que um caractere maiúsculo normal. |
| \\ | Representa uma única barra invertida |
| \aXXX | Insira um caractere não ASCII cujo código Windows-1252 seja decimal XXX. Consulte a tabela de caracteres PML para obter detalhes. |
| \UXXXX | Insira um caractere não ASCII cujo código Unicode seja hexadecimal XXXX. Consulte a tabela de caracteres PML estendida para obter detalhes. |
| \m="nomedaimagem.png" | Insira a imagem nomeada. Veja a seção sobre Imagens abaixo. |
| \q="#linkanchor"Algum texto\q | Referencie uma âncora de link que esteja em outro local no documento. A string após a especificação da âncora e antes do \q à direita é sublinhada ou mostrada como um link ao visualizar o documento. |
| \Q="linkâncora" | Especifique uma âncora de link no documento. |
| \- | Insira um hífen suave. Um hífen suave aparece apenas se for necessário quebrar uma palavra em uma linha. |
| \Fn="nota de rodapé1"1\Fn | Vincule o "1" a uma nota de rodapé cujo nome é footnote1, marcado no final do documento PML. Veja a seção em Notas de Rodapé e Barras Laterais abaixo. |
| \Sd="sidebar1"Barra Lateral\Sd | Vincule o texto "Barra Lateral" a uma barra lateral cujo nome seja sidebar1, marcado no final do documento PML. Veja a seção em Notas de Rodapé e Barras Laterais abaixo. |
| \I | Marcar como um item de índice de referência. Coloque o item de índice (e quaisquer códigos de estilo) com \I e \I.|


## Referências

* [Palm Markup Language - Por MobileRead](https://wiki.mobileread.com/wiki/EReader)
* [E-Reader - Por MobileRead](https://en.wikipedia.org/wiki/E-reader)

