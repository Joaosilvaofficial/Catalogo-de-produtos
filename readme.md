# Catálogo de Produtos com Paginação e Filtro

O projeto tem como objetivo criar um catálogo de produtos dinâmico utilizando HTML, CSS e JavaScript puro. Os produtos são carregados a partir de um arquivo JSON e exibidos em uma interface responsiva que permite busca, filtragem, ordenação, paginação e visualização detalhada dos itens.

Abaixo seguem os principais recursos utilizados:

## HTML (Estrutura e Semântica)

* **Estrutura Padrão:** Utilização correta das tags globais (`<!DOCTYPE html>`, `<html>`, `<head>` e `<body>`).
* **Metadados:** Configuração da codificação UTF-8 e da viewport para garantir compatibilidade e responsividade em diferentes dispositivos.
* **Arquivos Externos:**

  * Inclusão de folha de estilos externa (`style.css`).
  * Inclusão de scripts JavaScript utilizando o atributo `defer`, garantindo que a execução ocorra somente após o carregamento do DOM.
* **Tags Semânticas:**

  * `<header>` para o cabeçalho da aplicação.
  * `<nav>` para os controles de busca, filtros e paginação.
  * `<main>` para o conteúdo principal.
  * `<section>` para agrupamento lógico dos produtos e detalhes.
  * `<footer>` para informações institucionais.
* **Elementos de Formulário:**

  * `<input type="text">` para pesquisa de produtos.
  * `<select>` para filtragem por marca.
  * `<select>` para ordenação dos resultados.
* **Navegação Entre Páginas:**

  * Uso de parâmetros na URL (`produto.html?id=1`) para exibição dinâmica dos detalhes de cada produto.
  * Links internos para navegação entre catálogo e página de produto.

---

## CSS (Estilização e Layout)

* **Reset Global:** Aplicação de reset utilizando o seletor universal (`*`) para normalização de margens, paddings e `box-sizing`.
* **Variáveis CSS (Custom Properties):**

  * Definição de tokens de design através do seletor `:root`.
  * Centralização das cores principais da aplicação para facilitar manutenção e customização.
* **Nesting (Aninhamento Nativo):**

  * Utilização do novo recurso de aninhamento do CSS para organização dos estilos relacionados.
* **Layout Moderno com Flexbox:**

  * Alinhamento dos elementos do cabeçalho.
  * Organização dos filtros.
  * Estrutura do rodapé.
* **Layout Moderno com CSS Grid:**

  * Exibição dos produtos em formato de grade responsiva.
  * Layout da página de detalhes do produto.
  * Organização dos produtos relacionados.
* **Responsividade:**

  * Uso de Media Queries para adaptação em tablets e smartphones.
  * Reorganização automática dos filtros em telas menores.
  * Conversão do layout de detalhes para coluna única em dispositivos móveis.
* **Interatividade Visual:**

  * Efeito hover nos cards de produtos.
  * Destaque visual da página ativa na paginação.
  * Uso de transições suaves para melhorar a experiência do usuário.
* **Unidades Modernas:**

  * Utilização de `rem`, `%`, `min()` e `auto-fill` para criação de layouts fluidos e escaláveis.

---

## JavaScript (Lógica e Manipulação)

### Carregamento Assíncrono

* Uso de funções assíncronas (`async/await`) para carregar os dados do arquivo JSON.
* Consumo dos dados utilizando a API Fetch.

### Manipulação do DOM

* Seleção de elementos através de:

  * `querySelector()`
  * `createElement()`
* Atualização dinâmica da interface utilizando:

  * `innerHTML`
  * `appendChild()`
  * `classList.add()`

### Catálogo de Produtos

* Renderização dinâmica dos produtos a partir do arquivo JSON.
* Criação automática dos cards contendo:

  * Imagem
  * Nome
  * Marca
  * Preço
* Geração dinâmica dos links para a página de detalhes.

### Busca e Filtros

* Pesquisa em tempo real utilizando o evento `input`.
* Filtragem por marca através de listas geradas dinamicamente.
* Uso do método `filter()` para geração da coleção filtrada.
* Utilização de `includes()` para busca parcial por texto.

### Ordenação

* Ordenação alfabética por nome utilizando:

  * `localeCompare()`
* Ordenação numérica crescente e decrescente utilizando:

  * `sort()`

### Paginação

* Divisão automática da lista de produtos em páginas.
* Cálculo dinâmico da quantidade de páginas.
* Geração automática dos botões de navegação.
* Atualização visual da página ativa.

### Página de Produto

* Leitura dos parâmetros da URL através da interface:

  * `URLSearchParams`
* Busca do produto correspondente utilizando:

  * `find()`
* Atualização dinâmica do título da página.
* Exibição completa das informações do produto.

### Produtos Relacionados

* Identificação automática de produtos da mesma marca.
* Exclusão do produto atualmente visualizado.
* Limitação da quantidade exibida através de:

  * `slice()`
* Renderização dinâmica dos cards relacionados.

### Manipulação de Arrays

* Uso dos métodos:

  * `map()`
  * `filter()`
  * `find()`
  * `sort()`
  * `slice()`
  * `forEach()`

---

## Estrutura do Projeto

```text
/
├── index.html
├── produto.html
│
├── css/
│   └── style.css
│
├── js/
│   ├── app.js
│   └── produto.js
│
└── data/
    └── produtos.json
```

---

## Funcionalidades Implementadas

✅ Catálogo dinâmico de produtos

✅ Carregamento de dados via JSON

✅ Busca em tempo real

✅ Filtro por marca

✅ Ordenação por nome

✅ Ordenação por preço crescente

✅ Ordenação por preço decrescente

✅ Paginação automática

✅ Página de detalhes do produto

✅ Produtos relacionados

✅ Layout responsivo

✅ Navegação entre páginas

---

## Conceitos Trabalhados

* HTML Semântico
* CSS Moderno
* CSS Grid Layout
* Flexbox
* CSS Variables
* CSS Nesting
* Media Queries
* JavaScript ES6+
* Manipulação do DOM
* Eventos
* Fetch API
* Async/Await
* Arrays e Métodos Funcionais
* URLSearchParams
* Programação Assíncrona
* Responsividade
* Arquitetura Front-End baseada em dados JSON