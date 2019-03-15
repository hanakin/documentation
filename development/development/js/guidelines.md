## Formating

- Tab indentation
- Semicolons are required at the end of a line
- Single-quotes
- No unused variables
- Space after keyword `if (condition) {}`
- Always === instead of ==

things to add to xo
- `array-bracket-spacing: ["error", "always"]`
- `block-spacing: "error"`
- `comma-dangle: ["error", "always"]`
- `multiline-comment-style: ["error", "starred-block"]`
- `computed-property-spacing: "off"`
- `space-in-parens: "off"`

reference this https://eslint.org/docs/user-guide/configuring#configuring-rules

## Doc Blocks

We require the use of jsdoc Documentation blocks for any and all functions and classes. This helps to not only better understand what the code is trying to do and defines all of its paramaters. It also allows code editors/IDEs to provide better code completion and hints for the project codebase.

## Seperation of Concerns


To ensure the cleanest and most manageable codebase possible we enforcea strict seperation of concerns philosophy. This means all code for a specific programming language is done in files with that ext. Any and all interactions or outputs to a file of a different coding language should be handled through a hooh or an abstraction layer such as a template system.

#### Action Binding/Toggling

Given Javascripts interactive nature this means carful adherence an established way of handling these interactions. All HTML components the require JS will make use of data-attributes to pass information back and forth to the JS code. We will also utlizes these to establish a two way directional hook.

Lets say you have something that toggles an action and a component that executes said action. each of these would get a data-attribute specifying what they are for set to a common value to specify the relationship.

For Example:

```html
    <element data-toggle="modal">
```

This used to specify an element as a toggle to open a modal.

```html
    <component data-action="modal">
```

This used to specify that a component has an action called by a toggle
