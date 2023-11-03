# Positioning: Relative and Absolute

In web design and CSS, positioning refers to how elements are placed and displayed within the layout of a webpage. Two common positioning properties are "relative" and "absolute," each with distinct behaviors and use cases.

## Relative Positioning

- **Relative positioning** refers to positioning an element relative to its normal position in the document flow. It allows elements to be shifted without affecting the layout of other elements.
- When an element is relatively positioned, it can be moved using properties like `top`, `right`, `bottom`, and `left`.
- Relative positioning is often used for fine-tuning the position of elements within a container without disrupting the surrounding content.
- Elements with relative positioning still occupy space in their original position, which may lead to overlapping with other elements.
- Relative positioning does not take the element out of the normal document flow.

```css
.element {
  position: relative;
  top: 10px;
  left: 20px;
}
```

# Absolute Positioning

Absolute positioning is a CSS property that allows you to precisely position an element within its closest positioned ancestor or the viewport. This positioning method is particularly useful for creating overlays, pop-up menus, and elements that need to be placed precisely on a web page.

## How Absolute Positioning Works

When an element is given absolute positioning, it is removed from the normal document flow. This means it does not take up space in its original position, which can lead to other content overlapping if not managed correctly.

To position an element absolutely, you can use CSS properties like `top`, `right`, `bottom`, and `left`. These properties define the distance between the element and the edges of its nearest positioned ancestor (an ancestor element with a `position` value other than `static`) or the viewport.

## Example:

Let's consider an example where you want to create a tooltip that appears when a user hovers over a specific element. Here's how you can achieve this with absolute positioning:

```html

  <style>
    .tooltip {
      position: absolute;
      top: 20px;
      left: 50px;
      background-color: #333;
      color: #fff;
      padding: 5px;
      display: none;
    }

    .hover-element {
      position: relative;
    }

    .hover-element:hover .tooltip {
      display: block;
    }
```
