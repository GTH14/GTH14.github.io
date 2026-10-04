# Portfólio — Gabriel Haga

Site estático publicado em <https://gth14.github.io/>.

## Como alterar os textos

1. Abra o repositório no GitHub e clique em `index.html`.
2. Clique no ícone de lápis (`Edit this file`).
3. Procure o texto com `Ctrl + F` e altere somente o conteúdo entre as tags HTML.
4. Clique em `Commit changes`, escreva uma descrição curta e confirme.
5. Aguarde cerca de um minuto e atualize o site com `Ctrl + F5`.

Exemplo:

```html
<h1>Transformo problemas complexos em engenharia que <em>avança.</em></h1>
```

Pode ser alterado para:

```html
<h1>Engenharia mecânica, aerodinâmica e <em>simulação.</em></h1>
```

Os principais textos estão nestas classes:

- `hero h1`: título principal;
- `hero-intro`: apresentação abaixo do título;
- `section-heading`: títulos e introduções das seções;
- `project-card`: nome, resumo e detalhes de cada projeto;
- `timeline-item`: formação e experiência profissional;
- `site-footer`: frase final.

Evite apagar os sinais `<`, `>` e `/`, pois eles estruturam a página. Para adicionar um novo projeto, copie um bloco completo de `<details class="project-card">` até `</details>`, cole abaixo do anterior e então altere os textos.

## Como criar mais páginas

Cada arquivo `.html` pode ser uma página independente. Por exemplo:

```text
index.html       página inicial
projetos.html    página de projetos
sobre.html       página de apresentação
contato.html     página de contato
```

O processo mais simples é:

1. No repositório, abra `index.html` e copie o conteúdo.
2. Use `Add file` → `Create new file`.
3. Digite o nome, como `projetos.html`, cole o conteúdo e remova as seções que não serão usadas.
4. Ajuste o título da aba dentro de `<title>...</title>`.
5. Troque os links do menu para os arquivos correspondentes.

Exemplo de menu entre páginas:

```html
<nav>
  <a href="index.html">Início</a>
  <a href="projetos.html">Projetos</a>
  <a href="sobre.html">Sobre</a>
</nav>
```

Em qualquer página, `href="index.html#trajetoria"` abre diretamente a seção `trajetoria` da página inicial.

## Identidade visual

As cores estão no início do bloco `<style>`, dentro de `:root`. A cor principal atual é:

```css
--acid: #0065bd;
```

Os demais componentes reutilizam essa variável. Portanto, mudar esse único valor altera a maior parte dos destaques do site.

## Imagem principal

O eVTOL está incorporado diretamente no `index.html` como uma imagem WebP em Base64. Essa solução evita arquivos faltando na publicação. Para futuras substituições, a organização mais simples é enviar a nova imagem ao repositório — por exemplo, `nova-imagem.webp` — e trocar todo o atributo `src` da tag `evtol-image` por:

```html
src="nova-imagem.webp"
```
