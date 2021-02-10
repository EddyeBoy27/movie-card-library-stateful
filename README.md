# Boas vindas ao repositório do projeto de Movie Cards Library Stateful!

## O que foi desenvolvido

Desenvolvido uma aplicação que consiste em uma biblioteca de cartões de filmes dinâmica utilizando React. A biblioteca é composta por:

* Um cabeçalho;

* Uma barra de busca, utilizada pra filtrar quais cartões serão exibidos na lista de cartões;

* Uma lista de cartões, onde cada cartão representa um filme e possui uma imagem, título, subtítulo, sinopse e avaliação;

* Um formulário para adicionar um novo cartão na biblioteca.

Um preview da implementação dessa biblioteca consta abaixo.

![image](preview.gif)

---

## Requisitos do projeto

#### 1. Crie um componente chamado `SearchBar`

- Esse componente renderizará uma barra com filtros acima da listagem de cartões. Quais cartões serão mostrados no componente `MovieList` dependerá dos filtros escolhidos. `SearchBar` deve receber como props:

  - `searchText`, uma string
  - `onSearchTextChange`, uma callback
  - `bookmarkedOnly`, um boolean
  - `onBookmarkedChange`, uma callback
  - `selectedGenre`, uma string
  - `onSelectedGenreChange`, uma callback

#### 2. Renderize um formulário dentro de `SearchBar`

- Dentro desse formulário haverá campos usados na filtragem de cartões.

#### 3. Renderize um input do tipo texto dentro do formulário em `SearchBar`

- O input deve ter uma label associada com o texto: **"Inclui o texto:"**;

- A propriedade `value` do input deve receber o valor da prop `searchText`;

- A propriedade `onChange` do input deve receber o valor da prop `onSearchTextChange`.

#### 4. Renderize um input do tipo checkbox dentro do formulário em `SearchBar`

- O input deve ter uma label associada com o texto: **"Mostrar somente favoritos"**;

- A propriedade `checked` do input deve receber o valor da prop `bookmarkedOnly`;

- A propriedade `onChange` do input deve receber o valor da prop `onBookmarkedChange`.

#### 5. Renderize um select dentro do formulário em `SearchBar`

- O select deve ter uma label associada com o texto: **"Filtrar por gênero"**;

- A propriedade `value` do select deve receber o valor da prop `selectedGenre`;

- A propriedade `onChange` do input deve receber o valor da prop `onSelectedGenreChange`;

- O `select` deve renderizar quatro tags `option`, com as opções de filtragem por gênero, na seguinte ordem:
   - `Todos`, com o valor `""`;
   - `Ação`, com o valor `action`;
   - `Comédia`, com o valor `comedy`;
   - `Suspense`, com o valor `thriller`.

#### 6. Crie um componente chamado `AddMovie`

- Esse componente renderizará um formulário que permite adicionar na biblioteca um novo cartão de filme, dadas as seguintes informações do novo filme:

  - subtítulo
  - título
  - caminho da imagem
  - sinopse
  - avaliação
  - gênero

`AddMovie` deve receber como props:

  - `onClick`, uma callback

#### 7. Estado

- O componente `AddMovie` possui como estado as seguintes propriedades:

  - `subtitle`: guarda o subtítulo preenchido no formulário por quem usa a aplicação;
  - `title`: guarda o título preenchido no formulário por quem usa a aplicação;
  - `imagePath`: guarda o caminho da imagem preenchido no formulário por quem usa a aplicação;
  - `storyline`: guarda a sinopse do filme escrita no formulário por quem usa a aplicação;
  - `rating`: guarda a nota de avaliação dada no formulário por quem usa a aplicação;
  - `genre`: guarda o gênero do filme selecionado no formulário por quem usa a aplicação.

 - Ou seja, o estado de `AddMovie` contém as informações do novo filme que foram inseridas por quem usa a aplicação.

- O estado inicial do componente `AddMovie` deve ser:

  - `subtitle`: '';
  - `title`: '';
  - `imagePath`: '';
  - `storyline`: '';
  - `rating`: 0;
  - `genre`: 'action'.

#### 8. Renderize um formulário dentro de `AddMovie`

- Dentro desse formulário haverá campos usados para preencher informações do novo cartão a ser adicionado na biblioteca.

#### 9. Renderize um input do tipo texto dentro do formulário em `AddMovie` para obter o título do novo filme

- O input deve ter uma label associada com o texto: **"Título"**;

- O input deve ter seu valor inicial provido pelo estado inicial do componente, via `title`;

- A propriedade `onChange` deve atualizar o estado de `AddMovie`, atribuindo a `title` o atual título contido no input.

#### 10. Renderize um input do tipo texto dentro do formulário em `AddMovie` para obter o subtítulo do novo filme

- O input deve ter uma label associada com o texto: **"Subtítulo"**;

- O input deve ter seu valor inicial provido pelo estado inicial do componente, via `subtitle`;

- A propriedade `onChange` deve atualizar o estado de `AddMovie`, atribuindo a `subtitle` o atual subtítulo contido no input.

#### 11. Renderize um input do tipo texto dentro do formulário em `AddMovie` para obter o caminho da imagem do novo filme

- O input deve ter uma label associada com o texto: **"Imagem"**;

- O input deve ter seu valor inicial provido pelo estado inicial do componente, via `imagePath`;

- A propriedade `onChange` deve atualizar o estado de `AddMovie`, atribuindo a `imagePath` o atual caminho da imagem contido no input.

#### 12. Renderize uma `textarea` dentro do formulário em `AddMovie` para obter a sinopse do novo filme

- A `textarea` deve ter uma label associada com o texto: **"Sinopse"**;

- A `textarea` deve ter seu valor inicial provido pelo estado inicial do componente, via `storyline`;

- A propriedade `onChange` deve atualizar o estado de `AddMovie`, atribuindo a `storyline` a sinopse atual continda na `textarea`.

#### 13. Renderize um `input` do tipo `number` dentro do formulário em `AddMovie` para obter a avaliação do novo filme

- O `input` deve ter uma label associada com o texto: **"Avaliação"**;

- O `input` deve ter seu valor inicial provido pelo estado inicial do componente, via `rating`;

- A propriedade `onChange` deve atualizar o estado de `AddMovie`, atribuindo a `rating` a avaliação atual continda no input.

#### 14. Renderize um `select` do formulário em `AddMovie` para selecionar o gênero do novo filme

- O `select` deve ter uma label associada com o texto: **"Gênero"**;

- O `select` deve ter seu valor inicial provido pelo estado inicial do componente, via `genre`;

- A propriedade `onChange` deve atualizar o estado de `AddMovie`, atribuindo a `genre` o gênero atual selecionado;

- O `select` deve renderizar três tags `option`, com as opções de filtragem por gênero, na seguinte ordem:
   - `Ação`, com o valor `action`;
   - `Comédia`, com o valor `comedy`;
   - `Suspense`, com o valor `thriller`.

#### 15. Renderize um botão do formulário em `AddMovie` para fazer uso dos dados do novo filme, contidos no estado de `AddMovie`

- O botão precisa ter escrito o seguinte texto: **"Adicionar filme"**;

- A propriedade `onClick` do botão invoca uma função definida por você, em `AddMovie`, que:
  - Executa a callback passada para o componente `AddMovie` via props, chamada `onClick`, que recebe como parâmetro o estado atual de `AddMovie`;
  - Reseta o estado de `AddMovie`, voltando para o inicial, conforme mencionado anteriormente.

#### 16. Crie um componente chamado `MovieLibrary`

- Esse componente renderizará a biblioteca de filmes, com a possiblidade de filtrar por filmes e adicionar um filme à biblioteca.

- `MovieLibrary` deve receber como props:

  - `movies`, um array

#### 17. Estado

- O componente `MovieLibrary` possui como estado as seguintes propriedades:

  - `searchText`: guarda o texto de busca por filmes;
  - `bookmarkedOnly`: um _boolean_ que guarda se é para filtrar por filmes favoritados ou não;
  - `selectedGenre`: guarda o gênero do filme selecionado para poder fazer a filtragem;
  - `movies`: guarda a lista de filmes.

- Ou seja, o estado de `MovieLibrary` contém a lista de filmes e os filtros a serem aplicados sobre a listagem.

- O estado inicial do componente `MovieLibrary` deve ser:

  - `searchText`: '';
  - `bookmarkedOnly`: false;
  - `selectedGenre`: '';
  - `movies`: a lista de filmes passadas pela props `movies`.

#### 18. Renderize `SearchBar` dentro de `MovieLibrary`

- `searchText` oriundo do estado de `MovieLibrary` deve ser passado para a prop `searchText` de `SearchBar`;

- A callback para atualizar o estado de `MovieLibrary` em `searchText` precisa ser passada para `SearchBar`;

- `bookmarkedOnly` oriundo do estado de `MovieLibrary` deve ser passado para a prop `bookmarkedOnly` de `SearchBar`;

- A callback para atualizar o estado de `MovieLibrary` em `bookmarkedOnly` precisa ser passada para `SearchBar`;

- `selectedGenre` oriundo do estado de `MovieLibrary` deve ser passado para a prop `selectedGenre` de `SearchBar`;

- A callback para atualizar o estado de `MovieLibrary` em `selectedGenre` precisa ser passada para `SearchBar`.

#### 19. Renderize `MovieList` dentro de `MovieLibrary`

- Deve passar para a prop `movies` de `MovieList` todos os filmes filtrados;

- Quando o estado para `bookmarkedOnly` é falso, não é alterada a listagem de filmes a ser renderizada;

- Quando o estado para `bookmarkedOnly` é verdadeiro, deve ser renderizado por `MovieList` somente filmes favoritados;

- Quando o estado para `selectedGenre` é vazio, não é alterada a listagem de filmes a ser renderizada;

- Quando o estado para `selectedGenre` não é vazio, deve ser renderizado somente filmes com o mesmo gênero;

- Quando o estado para `searchText` é vazio, não é alterada a listagem de filmes a ser renderizada;

- Quando o estado para `searchText` não é vazio, deve ser renderizado por `MovieList` filmes que satisfaçam a uma das condições abaixo:
  - Filmes cujo título contém o que está presente em `searchText`, **ou**;
  - Filmes cujo subtítulo contém o que está presente em `searchText`, **ou**;
  - Filmes cuja sinopse contém o que está presente em` searchText`.

#### 20. Renderize `AddMovie` dentro de `MovieLibrary`

- A callback que permite adicionar um novo filme ao final da lista precisa ser passada para `AddMovie`.

---
