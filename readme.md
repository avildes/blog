# {{Em Construção}}

# Documentação

## Postando

**Criar um post no github**

Para criar um novo post basta acessar o github e colocar o arquivo referente ao post na pasta **_posts** presente na raiz do repositorio. A nomenclatura dos posts deve seguir o padrão:

```
padrão:
  ano-mes-dia-titulo-do-post.markdown
exs.:
  2015-11-14-welcome-to-jekyll4.markdown
  2016-07-19-readme.markdown
  2016-07-19-The-Secret-of-Monkey-Island.markdown
```

**Como usar o Front Matter**

Todo post deve começar com um cabeçalho (chamado Front Matter) que define alguns atributos do post. O cabeçalho é delimitado por dois **---** um no começo e um no final e dentro dele a lista de atributos deve ser escrita seguindo o padrão: **nomedavariavel:** **valor**

Possíveis Variáveis:
- **layout**: tipo do arquivo de layout que será carregado, para os posts esse valor sempre fica igual (post)
- **title**:  Titulo do post que vai aparecer na pagina principal na lista de posts, mini-posts e todos os lugares onde o titulo do site vai ser exibido
- **date**: data que será utilizada para ordenar os posts no site. Por exemplo, o post que aparece primeiro quando a pagina principal do blog é aberta é sempre o ultimo post.
- **categories**: lista de categorias a qual o post esta relacionado
- **tags**: lista de tags a qual o artigo esta relacionado
- **image**: imagem que é exibida sempre que um post é exbido no site (pagina inicial, mini-posts, etc). É também a imagem que aparece no topo de um post quando o mesmo é a aberto.


exemplo:

```
  ---
  layout: post
  title:  "The Secret of Monkey Island"
  date:   2016-07-19 21:17:00
  categories: jogos monkey pointnclick island
  tags: monkey jogos pointnclick island
  image: assets/monkey.jpg
  ---
```

**Onde guardar os arquivos que serão usados no post**

As imagens, gifs, audios, etc que serão carregadas nos posts devem ser salvas na pasta chamada **assets** mas nada impede que dentro dessa pasta sejam criadas subpastas. Para reorganizar é preciso apenas ficar atento ao tentar carregar a imagem pois ao invés de preencher:

```
  image: assets/monkey.jpg
```

Vai ser necessário preencher:

```
  image: assets/novapasta/monkey.jpg
```

**Padrões para imagens e vídeos:**

Para chamar uma imagem dentro do post é preciso seguir o seguinte padrão:

```
<img src="https://{{ site.burl }}caminhodaimagem.extensaodoarquivo" class="image featured" />

ex:
<img src="https://{{ site.burl }}assets/screenshot.jpg" class="image featured" />
```

Para chamar um video dentro do post o padrão é:

```
<iframe class="image featured" width="854" height="480" src="https://www.youtube.com/embed/tBPA-TWw1ko" frameborder="0" allowfullscreen></iframe>
```

#### ATENÇÃO

A diferença entre esse 'iframe' e o iframe que o youtube coloca é:

```
class="image featured"
```

é importante não esquecer de adicionar esse atributo ao iframe para garantir que o vídeo é exibido corretamente na página.

--------

**Usar Links**

Para utilizar links na pagina basta colocar o nome que deve ficar em texto entre colchetes e em seguida, sem separação, um nome que defina o link. No fim do arquivo deve existir o seguinte:

```
[nome-que-define-o-link-sem-espacos]: http://link.com

ex:
[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
```

O exemplo completo ficaria:

```
É possível encontrar a [pagina oficial do jekyll][jekyll] e o [projeto][jekyll-gh] nos links.
Mais um [link][jekyll-help].

Texto.
Texto e mais texto.
Fim do post.

[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
```

Vale ressaltar que essas ultimas linhas, as que são referentes aos links, não vão aparecer no post.

**Postar audios**

Para chamar um audio dentro do post o código é o seguinte:

```
<audio controls>
   <source src="https://{{ site.burl }}assets/audio/android.mp3"
           type='audio/mp3'>
   <!-- The next line will only be executed if the browser doesn't support the <audio> tag-->
   <p>Your user agent does not support the HTML5 Audio element.</p>
</audio>
```

De preferência não colocar o audio no github. A melhor opção é usar algum site como host, exemplo:

**https://clyp.it/**

e passar o link da seguinte forma:


```
<audio controls>
   <source src="https://clyp.it/caminho/android.mp3"
           type='audio/mp3'>
   <!-- The next line will only be executed if the browser doesn't support the <audio> tag-->
   <p>Your user agent does not support the HTML5 Audio element.</p>
</audio>
```

**Drafts**

Artigos ainda em desenvolvimento podem ser guardados numa pasta chamada de 'drafts' ou na pasta _posts com o atributo 'published' marcado como 'false'. O atributo 'published' é opcional e caso não seja fornecido será considerado como 'true', ou seja, o arquivo será publicado. Exemplo:

```
Um post dessa forma na pasta '_posts' será publicado: 
  ---
  layout: post
  title:  "The Secret of Monkey Island"
  date:   2016-07-19 21:17:00
  categories: jogos monkey pointnclick island
  tags: monkey jogos pointnclick island
  image: assets/monkey.jpg
  ---
  
  Esse mesmo post escrito da seguinte forma NÃO será publicado:
  ---
  layout: post
  title:  "The Secret of Monkey Island"
  date:   2016-07-19 21:17:00
  categories: jogos monkey pointnclick island
  tags: monkey jogos pointnclick island
  image: assets/monkey.jpg
  published: false
  ---
```

**Como linkar um post a outro post**

## Desenvolvendo

Como funciona o config
 - Quais são as tags que ele reconhece
 - Como criar e usar novas tags
 - Permalinks
 - burl

Como é feita a integração com o analytics

Como é feita a integração com o Disqus

## Links

1. http://jekyllrb.com/
2. http://rodrigocarvalho.blog.br/facilitando-o-uso-do-github-pages/
3. https://mademistakes.com/articles/using-jekyll-2016/
