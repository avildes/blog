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

Para chamar uma imagem dentro do post é preciso seguir o seguinte padrão:

```
<img src="https://{{ site.burl }}caminhodaimagem.extensaodoarquivo" class="image featured" />

ex:
<img src="https://{{ site.burl }}assets/screenshot.jpg" class="image featured" />
```

Uso de links:

Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll’s dedicated Help repository][jekyll-help].

[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help


  - estrutura de um post



**Como chamar links para pastas guardadas no repositorio**

**Como linkar um post a outro post**

**Padrões para imagens e vídeos:**
- tamanho das imagens e gifs
- tamanho da area usada pelo video
- código para fazer o embed sem quebrar o design

**Postar audios**

**Formatação do texto**

**Drafts**

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
