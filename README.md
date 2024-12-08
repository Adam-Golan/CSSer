# Welcome to CSSer!

### Starting up

1. Run `npm i`
1. Run `npm run watch:scss`

### Configuration

You can edit [config.scss](./config.scss) in order to determine variables for your app and configure it.

**_Sections_**:

1. Colour Schemes - Here you'll determine your app's colour and background-color. Note that both properties will replace each other in dark mode. Output examples: var(--bg), var(--bgShadow), var(--trans-bg-(high | medium | low)).
2. Custom Colours - Here you can use a map to output any colour you like for your app. ("green": #6db966) will output: var(--green), var(--green-(l | d)-(1-5));
3. Font - Here you'll set your app's font.
4. Responsive sizes - Here you can configure any variable for any screen size.
5. Class generators switches - Here you can switch on and off compiling options.

### Tips and Tricks

Here are some powerful CSS properties you can leverage for advanced layouts and responsiveness:

#### 1. **Columns**
Use `columns` to create a responsive, multi-column layout effortlessly.
```css
.multi-column {
  columns: 3 200px; /* 3 columns with at least 200px width each */
  column-gap: 1em; /* Space between columns */
}
```
- Great for text-heavy content or card grids.
- Can be combined with `column-rule` for styled dividers.

#### 2. **Block-Size**
The `block-size` property ensures responsive height, independent of writing mode.
```css
.responsive-height {
  block-size: 50vh; /* Half of the viewport height */
}
```
- Use with `inline-size` for a flexible, writing-mode-agnostic layout.
- Works seamlessly with `min-block-size` and `max-block-size`.

#### 3. **Aspect-Ratio**
Maintain consistent proportions across different screen sizes.
```css
.fixed-ratio {
  aspect-ratio: 16 / 9; /* Widescreen aspect ratio */
}
```
- Perfect for media elements like videos and images.
- Ensures consistent sizing without manual width/height adjustments.

#### 4. **Scroll Snap**
Create smooth scrolling experiences for carousels or lists.
```css
.snap-container {
  scroll-snap-type: x mandatory;
}
.snap-item {
  scroll-snap-align: center;
}
```
- Combine with `overflow-x: scroll` for horizontal scrolling.
- Ideal for creating a snap-to-item effect in carousels or galleries.

#### 5. **Clamp**
Use `clamp()` for dynamic, range-bound sizing.
```css
.dynamic-font {
  font-size: clamp(1rem, 2.5vw, 3rem); /* Responsive font size */
}
```
- Ideal for fluid typography and spacing.
- Ensures that the value stays within a defined range, regardless of screen size.

#### 6. **Object-Fit**
The `object-fit` property allows you to control how an element's content is resized to fit its container.
```css
.image-container {
  width: 100%;
  height: 300px;
  object-fit: cover; /* Ensures the image covers the container */
}
```
- Ideal for images and videos to maintain their aspect ratio while filling the container.
- Other values include `contain`, `fill`, and `none`.

#### 7. **Accent-Color**
The `accent-color` property sets the color of form controls (such as checkboxes, radio buttons, etc.) and input fields.
```css
input, button {
    accent-color: #3498db; /* Apply a blue accent color */
}
```
- Adds consistency and theming to form elements.
- Can be used for customizing checkboxes, radio buttons, and other form components.

#### 8. **Box-Reflect**
The `box-reflect` property adds a reflection effect to an element.
```css
.reflect {
    -webkit-box-reflect: below 0px linear-gradient(transparent, transparent 40%, rgba(0, 0, 0, 0.15));
}
```
- Great for creating a mirrored reflection effect for images and elements.
- Can be combined with `box-shadow` for more complex effects.

#### 9. **@supports**
The `@supports` rule lets you apply styles only if a certain CSS feature is supported by the browser.
```css
@supports (display: grid) {
    .grid-container {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
    }
}
```
- Use this to implement fallbacks for older browsers that do not support newer CSS features.
- Ensures compatibility across different environments (known as incompatible in firefox).

#### 10. **filter**
The `filter` property allows you to apply visual effects such as blur, brightness, and grayscale to an element.
```css
.image {
    filter: grayscale(50%) blur(5px); /* Apply grayscale and blur */
}
```
- Useful for creating effects like image manipulation or hover effects.
- Combine multiple filter functions to create complex visual effects.

#### 11. **mask**
The `mask` property allows you to define an image, gradient, or other shape to hide portions of an element.
```css
.masked {
    mask-image: url('mask.png');
    mask-size: cover;
}
```
- Can be used for creating complex shapes and effects like circular masks or textured overlays.
- Combine with `mask-repeat`, `mask-position`, and `mask-type` for more control.

#### 12. **backdrop-filter**
The `backdrop-filter` property applies graphical effects to the area behind an element, such as blur or brightness.
```css
.backdrop {
    backdrop-filter: blur(10px); /* Apply a blur effect to the background */
}
```
- Ideal for frosted glass effects or background manipulation behind semi-transparent elements.
- Combine with `background-color` for additional visual effects.
