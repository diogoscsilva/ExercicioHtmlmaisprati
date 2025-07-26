# ExercicioHtmlmaisprati
Exercicio de CSS e HTML


## Estrutura do HTML (`index.html`)

O arquivo `index.html` está organizado com as seguintes seções principais:

* **`<head>`**:
    * `meta charset="UTF-8"` e `lang="pt-BR"`: Define a codificação de caracteres para português do Brasil.
    * `meta name="viewport"`: Garante a responsividade em diferentes dispositivos.
    * `link rel="stylesheet" href="style.css"`: Vincula a folha de estilo CSS.

* **`<header>`**:
    * `<h1>Minha jornada dev</h1>`: Título principal da página.
    * `<input id="hamburger" type="checkbox"/>` e `<label for="hamburger"></label>`: Elementos para criar um menu hambúrguer interativo (usado em dispositivos móveis).
    * `<article>` com `<p>`: Uma breve apresentação que aparece ao clicar no menu hambúrguer em telas menores.

* **`<main>`**: Contém o conteúdo principal da página, dividido em várias seções:
    * **Missão (`<section>`):**
        * `<p>` com `<span class="destaque">`: Parágrafo com uma palavra destacada usando uma classe CSS.
    * **Visão (`<section>`):**
        * `<h2>Visão</h2>`: Título da seção.
        * `<p id="importante">`: Parágrafo com um ID específico para estilização.
    * **Livros de Referência (`<section>`):**
         Contêineres que utilizam Flexbox e Grid para organizar uma galeria de livros.
        * `<div class="card">`: Cada `div` representa um cartão de livro, contendo uma imagem (`<img>`), título (`<h5>`) e autor (`<h6>`).
    * **Formulário de Feedback (`<section>`):**
        * `<form id="feedback">`: Formulário para coletar feedback.
        * `<label>` e `<input type="text"`, `type="email"`, `type="submit"`: Campos de entrada para nome, endereço, e-mail e botão de envio.
        * `<select>` com `<option>`: Um menu drop-down para selecionar o tipo de feedback.
        * `<textarea>`: Campo para o comentário do feedback.
    * **Hobbies e Receita (`<section>` com `<article>`):**
        * `<h3>Hobbies</h3>` e `<ul>` com `<li>`: Uma lista não ordenada de hobbies.
        * `<h3>Receita de feijão carioca</h3>` e `<ol>` com `<li>`: Uma lista ordenada de passos de uma receita.
    * **Livros Gratuitos Online (`<nav class="link-list">`):**
        * `<h3>Livros gratuitos online</h3>`: Título da seção.
        * `<a>` com `href`, `target="_blank"` e `rel="noopener noreferer"`: Links para livros online gratuitos, abrindo em novas abas e com segurança.

* **`<footer>`**:
    * `<p>Copyright: Diogo Santoro Costa da Silva</p>`: Informações de direitos autorais.

## Estilização CSS (`style.css`)


### Seletores e Propriedades Comuns:

* **`body`**: Define o modelo de caixa (`box-sizing`), remove margens e preenchimentos padrão.
* **`header` e `footer`**: 
 O `header` também tem `position: sticky` para ficar fixo no topo ao rolar.

* **`h2`**: Define tamanho da fonte e sublinhado.

incluindo margem, borda, altura mínima e cor de fundo.
* **`section`**: Estilos gerais para as seções, como cor do texto, preenchimento e `border-radius`.

* **`#importante`**: Estilização específica para o parágrafo com `id="importante"`, adicionando uma borda superior.
* **`.destaque`**: Estiliza o texto com a classe `destaque` (itálico e fundo branco).

### Layout da Galeria de Livros (`.flex-conteiner` e `.galery`):

* **`.flex-conteiner`**: Utiliza `display: flex`, `flex-wrap: wrap`, `justify-content: center` e `align-items: center` para centralizar e permitir que os itens quebrem para a próxima linha.
* **`.galery`**: Utiliza `display: grid` para criar um layout de grade para os cartões de livro.
    * `grid-gap`: Espaçamento entre os itens da grade.
    * `grid-template-columns`: Define o número e a largura das colunas (4 colunas de 14vw por padrão).

* **`.card`**: Estilos para cada cartão de livro na galeria, incluindo altura, Flexbox para alinhamento de conteúdo, borda, `border-radius` e preenchimento.

* **`.card img`**: Estilos para as imagens dos livros, definindo altura, largura mínima e máxima.
* **`.card > h5`**: Alinha o título do livro ao final do cartão.

### Formulário de Feedback (`#feedback`):

* **`#feedback`**: Utiliza `displ
### Lista de Links (`nav.link-list`):

* **`nav.link-list`**: Utiliza `display: flex` e `flex-direction: column` para organizar os links verticalmente.

## Responsividade (`@media` queries)


* **`@media (max-width: 600px)`**: Estilos aplicados para telas com largura máxima de 600px
    * O menu hambúrguer é exibido e o texto de apresentação do cabeçalho é ocultado por padrão, aparecendo apenas quando o hambúrguer é clicado.
    * A galeria de livros muda para 3 colunas.

* **`@media (max-width: 420px)`**: Estilos adicionais para telas ainda menores (smartphones menores).
    * A galeria de livros muda para 2 colunas.

* **`@media (max-width: 290px)`**: Estilos para telas muito pequenas.
    * A galeria de livros muda para 1 coluna.
    * O `body` tem uma largura mínima para evitar quebras de layout extremas.
