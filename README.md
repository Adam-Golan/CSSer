# Welcome to CSSer!
### Starting up
1. Run `npm i`
1. Run `npm run watch:scss`

### Configuration
You can edit [config.scss](./config.scss) in order to determine variables for your app and configure it.<br>
***Sections***:
1. Colour Schemes - Here you'll determine your app's colour and background-color.<br>
Note that both properties will replace each other in dark mode.<br>
Output examples: var(--bg), var(--bgShadow), var(--trans-bg-(high | medium | low)).
1. Custom Colours - Here you can use a map to output any colour you like for your app.<br>
("green": #6db966) will output: var(--green), var(--green-(l | d)-(1-5));
1. Font - Here you'll set your app's font.
2. Responsive sizes - Here you can configure any variable for any screen size.
3. Class generators switches - Here you can switch on and off compiling options.
