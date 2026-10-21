# Portfólio — Gabriel Haga

Site estático publicado em <https://gth14.github.io/>.

## Estrutura

```text
index.html        página inicial e resumo do portfólio
projetos.html     projetos acadêmicos e técnicos
trajetoria.html   formação e experiência profissional
styles.css        identidade visual e layout das três páginas
```

O menu no topo de cada página liga esses arquivos entre si. Ao adicionar uma nova página, inclua o respectivo link nos três menus para manter a navegação consistente.

## Como alterar os textos

1. Abra o arquivo desejado no GitHub.
2. Clique no ícone de lápis (`Edit this file`).
3. Use `Ctrl + F` para localizar o texto.
4. Altere somente o conteúdo entre as tags HTML.
5. Clique em `Commit changes` e confirme.
6. Aguarde cerca de um minuto e atualize o site com `Ctrl + F5`.

Evite apagar os sinais `<`, `>` e `/`, pois eles estruturam a página.

## Como adicionar as imagens dos projetos

Em `projetos.html`, cada projeto contém um bloco como este:

```html
<figure class="project-figure">
  <figcaption>Imagem do projeto · a inserir</figcaption>
</figure>
```

Depois de enviar a imagem ao repositório, preferencialmente para uma pasta `images`, substitua o conteúdo por:

```html
<figure class="project-figure">
  <img src="images/nome-da-imagem.webp" alt="Descrição objetiva do que aparece na imagem">
</figure>
```

Use nomes sem espaços e imagens em `.webp` ou `.jpg`. Uma proporção próxima de 16:9 funciona melhor no layout atual.

## Como adicionar um novo projeto

1. Em `projetos.html`, copie um bloco completo de `<article class="project-entry">` até `</article>`.
2. Cole-o antes do fechamento do contêiner principal.
3. Altere o `id`, o número, o título, os metadados, os textos e as tags.
4. Se quiser destacá-lo na página inicial, copie também um bloco `project-preview` de `index.html` e aponte o link para o novo `id`.

Exemplo de link para uma seção específica:

```html
<a href="projetos.html#novo-projeto">Novo projeto</a>
```

## Identidade visual

As cores ficam no início de `styles.css`, dentro de `:root`. A cor principal é:

```css
--blue: #0065bd;
```

As outras variáveis controlam fundo, texto, linhas e tons auxiliares. A maior parte do site pode ser ajustada alterando apenas essas variáveis.

## Imagem principal

O eVTOL da página inicial permanece incorporado no próprio `index.html` como uma imagem WebP em Base64. As imagens futuras dos projetos podem ser mantidas como arquivos separados na pasta `images`, o que facilita a atualização.
