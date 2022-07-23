# Como funciona o import e o export no JavaScript?

Em JavaScript cada arquivo é considerado como um módulo;

## export default

```jsx
// Modulo.js

const variavel = 'Valor';
const variavel2 = 'Outro valor';

export default variavel;
// Modulo2.js

import Modulo;
console.log(Modulo);
```

⬆️ É uma boa prática referenciar o nome do arquivo ao fazer o import.

## Exportar múltiplos valores de um arquivo

Forma alternativa: ao declarar uma variável.

```jsx
// Modulo.js

export const variavel = 'Valor';
export const variavel2 = 'Outro Valor';
// Modulo2.js 

import { variavel, variavel2 };
console.log(variavel, 'e' ,variavel2);
```

⚠️ Atenção: object destructuring ⬆️

Ou ainda:

```jsx
// Modulo2.js

import * as Modulo
```

🤔 Cada valor exportado será agrupado dentro de um módulo.

# Do Zero para programador front-end

## Trilha a seguir

1. HTML5 e CSS3
2. Lógica de Programação
3. JavaScript
4. Bibliotecas - Ex. Bootstrap, JQuerry;
5. Mais JavaScript
6. Frameworks - Ex. Angular, React
7. Pré-processador - Ex. SASS LESS
8. Ferramenta de Build - Ex. Gulp
9. Noção de Back-end - Dica: PHP

# Organizando o CSS no seu projeto

É uma boa prática criar um arquivo css que contenha estilos comuns a mais de um arquivo html, com suas respectivas classes, bastando referenciá-lo dentro da tag head, em todos os arquivos html que apresentem os mesmos estilos, mantendo-se arquivos específicos para estilos específicos de cada html.

- Guia de boas práticas: SMACSS (https://smacss.com/)

1. Base
2. Layout
3. Module
4. State
5. Theme