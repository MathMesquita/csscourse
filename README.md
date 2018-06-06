# CSS Master

## Ementa

- [Boxes](#boxes)
- [Rules e declaration blocks](#rules-e-declaration-blocks)
- [box model](#box-model)
- [Margin collapse](#margin-collapse)
- [Seletores](#seletores)
- [Unidades](#unidades)
- [Ordem de preferencia](#ordem-de-preferencia)
- [Debug](#debug)
- [Float](#float)
- [Flexbox](#flexbox)
  - [Flex container](#flex-container)
  - [Flex item](#flex-item)
- [CSS Patterns](#css-patterns)
- [Grid](#grid)
  - [Grid container](#grid-container)
  - [Grid item](#grid-item)

### Boxes

### Rules e declaration blocks

- Rules antes das chaves
- Declaration entre as chaves `{...}`

### Box model

- Box-sizing([`content-box`](https://mdn.mozillademos.org/files/13647/box-model-standard-small.png) [`border-box`](https://mdn.mozillademos.org/files/13649/box-model-alt-small.png))
- Overflow(`auto` `hidden` `visible`)
- Background-clip(`border-box` `padding-box` `content-box`)
- Display(`block` `inline` `inline-block`)
- Position(`static` `relative` `absolute` `fixed`)

### Margin collapse

- Top e Bottom
- First child e Last child
- Sem altura

### Seletores

- Seletores simples(`elementos`, `classes` e `ids`)
- [Seletores de atributo](https://mathmesquita.me/2017/01/24/seletores-avancados-de-css.html)(`[attr[=]]`)
- Pseudo classes([`parte 1`](https://mathmesquita.me/2017/01/25/seletores-avancados-de-css-2.html) [`parte 2`](https://mathmesquita.me/2017/02/22/seletores-avancados-de-css-3.html))
- Pseudo elementos
- [Combinadores](https://mathmesquita.me/2017/01/24/seletores-avancados-de-css.html)(`,` ` ` `>` `+` `~`)

### Unidades

- Valores Numericos(`unitless` `px` `em` `rem` `vw` `vh` `vmin` `vmax`)
- Porcentagens(`parent-related` `font-related`)
- Cores(`keyword` `hex` `hsl` `rgb` `hsla` `rgba`)
- Funções(`rgba()` `translate()` `url()` `...`)

### Ordem de preferencia

- Importancia(`!important`)
- Especificidade(`1000` `100` `10` `1`)
- Ordem no código

### Debug

- Stylesheets
- Computed
- Box-model

### Float

- float(`none` `left` `right` `inherit`)
- clear(`none` `both` `left` `right`)
- Height collapse(`empty div` `::after` `display: flow-root`)

### Flexbox

#### Flex container

- [`flex-direction`](https://css-tricks.com/wp-content/uploads/2013/04/flex-direction2.svg)(`row` `row-reverse` `column` `column-reverse`)
- [`flex-wrap`](https://css-tricks.com/wp-content/uploads/2014/05/flex-wrap.svg)(`nowrap` `wrap` `wrap-reverse`)
- [`flex-flow`](https://cdn.css-tricks.com/wp-content/uploads/2013/04/justify-content-2.svg)(`<flex-direction> <flex-wrap>`)
- [`justify-content`](https://cdn.css-tricks.com/wp-content/uploads/2013/04/justify-content-2.svg)(`flex-start` `flex-end` `center` `space-between` `space-around` `space-evenly`)
- [`align-items`](https://cdn.css-tricks.com/wp-content/uploads/2014/05/align-items.svg)(`stretch` `flex-start` `flex-end` `center` `baseline`)
- [`align-content`](https://css-tricks.com/wp-content/uploads/2013/04/align-content.svg)(`flex-start` `flex-end` `center` `stretch` `space-between` `space-around`)

#### Flex item

- [`order`](https://css-tricks.com/wp-content/uploads/2013/04/order-2.svg)
- [`flex-grow`](https://css-tricks.com/wp-content/uploads/2014/05/flex-grow.svg)
- `flex-shrink`
- [`flex-basis`](https://www.w3.org/TR/css-flexbox-1/images/rel-vs-abs-flex.svg)
- `flex`(`<flex-grow> <flex-shrink> <flex-basis>`)
- [`align-self`](https://css-tricks.com/wp-content/uploads/2014/05/align-self.svg)

### Css Patterns

- [SMACSS](https://smacss.com)(Scalable and Modular Architecture for CSS)
- [BEMCSS](http://getbem.com/introduction/)(Block Element Modifier CSS)
- [RSCSS](http://rscss.io)(Reasonable System for CSS Stylesheet Structure)
- [MaintainableCSS](https://maintainablecss.com)

#### SMACSS

- Base *(input, input\[type=checkbox\], h1, p)*
  - Importancia do reset.css
- Layout *(Wrappers para modules)*
  - *(.l-layout, #sidebar, .l-inline, .l-inline #sidebar)*
- Module *(Partes reutilizaveis)*
  - *(.module, .cart, .form, .form-sidebar)*
  - Modulo subclasse
- State *(Estado do seu componente)*
  - *(.is-state, .cart.is-empty, .form.is-invalid)*
  - Pode ser usado em modulos e layouts
  - Dependente do uso de javascript
- Theme *(Quando necessrio, irá descrever como os layouts e modules deverão aparentar)*
  - Separado em outros arquivos *(mod-name.css, theme.css)*

#### BEMCSS

- Block *(.block)*
- Element *(.block__element)*
- Modifier *(.block__element .block__element--modifier)* *(.block .block--modifier)*

#### RSCSS

##### Componentes

- Nomenclatura *(No minimo 2 palavras)*
  - .cart-item, .header-logo
  
##### Elementos

- Nomenclatura de elementos *(Uma unica palavra)*
  - .cart-item > .title, .header-logo > .acomlogo

##### Variantes

- Nomenclatura de Variantes *(Prefixado com -)*
  - .cart-item.-small, .header-logo > .acomlogo.-blue
  
#### MaintanableCSS

- Semantica *(.col-md.red.pb3.m10)* *(.basket)*
  - Legibilidade
  - Facilidade para responsivo
  - Facilidade para pesquisar *ctrl+f*
  - Reduz risco de mudanças indesejadas
  - Não tem diferença de inline style
  - Hooks para testes automatizados
  - Hooks para o JS
  - Mais facil para debugar
  - Recomendado na doc do HTML
  - Não causa confusão ao estilizar estados como *:hover*
  - Diminui o tamanho do HTML, CSS pode e deve ser cacheado
- Reuso e ID's
- Convenção *(.\<module\>\[-component\]\[-state\]\[--modifier\])*
  - .basket
  - .basket-item
  - .basket-item-isOutOfStock
- Modules vs Components
  - Modules são feito de componentes
  - Modules são distintos na sua aplicação, e combinados formam estruturas complexas
- States
  - Fechado x Aberto, Habilitado x Desabilitado
  - *(.basket .basket-hasInvalidproducts)*
- Modifiers
  - Diferentemente do estado, modifiers so usados quando as diferenças são conhecidas
  - *(.basket .basket--suba, .product .product--phone)*
- Versionamento para teste A/B
  - *(.basket, .basket2)*

### Grid

#### Grid container

- `display` (`grid`, `inline-grid`)
- `grid-template-columns` (`<track-size>` `<line-name>`)
- `grid-template-rows` (`<track-size>` `<line-name>`)
- `grid-template-areas` ("`<grid-area-name>` | `.` | `none` | ...")
- `grid-template`(`<grid-template-rows> / <grid-template-columns>`)
- `grid-column-gap` (`<line-size>`)
- `grid-row-gap` (`<line-size>`)
- `grid-gap`(`<grid-row-gap> ? <grid-column-gap>`)
- `justify-items` (`start` `end` `center` `stretch`)
- `align-items` (`start` `end` `center` `stretch`)
- `place-items` (`<align-items> ? <justify-items>`)
- `justify-content` (_igual flexbox_)
- `align-content` (_igual flexbox_)
- `place-content` (`<align-content> ? <justify-content>`)
- `grid-auto-columns` (`<track-size>`)
- `grid-auto-rows` (`<track-size>`)
- `grid-auto-flow` (`row` `column` `row dense` `column dense`)
- `grid` (`<grid-template>` `<grid-template-rows> / [auto-flow ?&& dense] <grid-auto-columns>` `[auto-flow ?&& dense] <grid-auto-rows> / <grid-template-columns>`)


#### Grid item

- `grid-column-start` (`<line>` `span <number>` `span <name>` `auto`)
- `grid-column-end` (`<line>` `span <number>` `span <name>` `auto`)
- `grid-row-start` (`<line>` `span <number>` `span <name>` `auto`)
- `grid-row-end` (`<line>` `span <number>` `span <name>` `auto`)
- `grid-column` (`<start-line> / <end-line>`)
- `grid-row` (`<start-line> / <end-line>`)
- `grid-area` (`<row-start> / <column-start> / <row-end> / <column-end>`)
- `justify-self` (`start` `end` `center` `stretch`)
- `align-self` (`start` `end` `center` `stretch`)
- `place-self` (`<align-self> ? <justify-self>`)
