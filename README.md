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
- [Flexbox](#flexbox)
  - [Flex container](#flex-container)
  - [Flex item](#flex-item)

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











