### Flexbox

Flexbox is a one-dimensional layout model that allows you to align and distribute items along a single axis.
You can use CSS to style the Flexbox layout elements, just like you would any other HTML element.

The flex container properties are:

- flex-direction
- flex-wrap
- flex-flow
- justify-content
- align-items
- align-content

The flex item properties are:

- order
- flex-grow
- flex-shrink
- flex-basis
- flex
- align-self

```css
.flexbox-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}

.flexbox-item {
  width: 100px;
  height: 100px;
  background-color: red;
}
```

### Grid

Grid is a two-dimensional layout model that allows you to position items in a grid of rows and columns.
You can use CSS to style the Grid layout elements, just like you would any other HTML element.

```css
.grid-container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 1fr 1fr;
}

.grid-item {
  width: 100px;
  height: 100px;
  background-color: red;
}
```
