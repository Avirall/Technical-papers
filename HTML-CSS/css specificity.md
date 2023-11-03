# CSS Specificity

CSS specificity is a set of rules used to determine which styles are applied to an HTML element when multiple conflicting styles exist. It helps define which style rules take precedence in the rendering of a web page.

## How Specificity Works

Specificity is calculated based on the combination of selectors in a CSS rule. It is determined using the following factors, in order of importance:

1. **Inline Styles**: Styles applied directly to an HTML element using the `style` attribute have the highest specificity. These styles override any other styles.

2. **ID Selectors**: Styles applied using the `#id` selector have a high specificity. An ID selector is more specific than a class selector or a type selector.

3. **Class Selectors and Attribute Selectors**: Styles applied using class selectors (e.g., `.class`) and attribute selectors (e.g., `[data-attribute]`) have medium specificity.

4. **Type Selectors**: Styles applied using element type selectors (e.g., `div`, `p`) have the lowest specificity.

5. **Combining Selectors**: When multiple selectors are combined, the specificity is cumulative. For example, `div p` has a lower specificity than `#unique-id`.

## Calculating Specificity

Specificity is usually represented in the format of four numbers: `a, b, c, d`. These numbers indicate the specificity of a CSS rule. Here's how they are calculated:

- `a` is the number of inline styles.
- `b` is the number of ID selectors.
- `c` is the number of class selectors, attribute selectors, and pseudo-classes.
- `d` is the number of type selectors and pseudo-elements..

## Resolving Conflicts

When conflicting styles exist, the style with the highest specificity is applied. If two styles have the same specificity, the one that appears later in the CSS file takes precedence (the "cascading" part of Cascading Style Sheets).

Understanding specificity is essential for managing and troubleshooting CSS styles in complex web projects. It helps ensure that the desired styles are applied to elements and avoid unexpected overrides.
