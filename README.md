Created for a Uni assignment, as _A light, lean alternative to [slides.com](https://slides.com)_.

- Made with React using:
  - Typescript
  - Shadcn/UI components
  - Tailwind CSS
  - Tanstack Router

## Features

I would recommend just trying it out [here](https://slides.kaistuff.dev) and then coming back to view the full feature list.

### Basic Auth

- Login
- Register

### Presentations

- View all presentations on the dashboard
- Create a new presentation
- Create slides within the presentation, move between them

### Slides

- Can put Text, Video, Images, Code elements onto the slides.
  - Certain size and position can be chosen for the elements upon creation.
  - Text elements can have their font-size and colour adjusted.
  - Videos have an autoplay option
  - Code elements autodetect the language (C, Javascript and Python) supported at the moment.
  - These properties can be edited by right clicking after creation
- These elements can be moved by dragging and also resized.
- Text elements font can be selected from a provided set of fonts.
- The theme and background colours of the slides can be chosen. It can be a solid colour or a gradient.
- The presentation can be previewed (opens up a new tab with just the presentation viewable)
- Slide transition animations in the presentation mode
- Slides can be rearranged by dragging
- Slide version history, so that it can be reverted back to a previous state.

## Accessibility Considerations

-Semantic html elements were used so not everything is just a div.
-Alt-text included where required.

- Shadcn/UI components were used which are just styled radixUI components.

RadixUI handles many accessibility features, heres a description from their website:

> We take care of many of the difficult implementation details related to accessibility, including aria and role attributes, focus management, and keyboard navigation. That means that users should be able to use our components as-is in most contexts and rely on functionality to follow the expected accessibility design patterns.

Additionally, neutral colours were used with clear contrast. We used off-white colours alongside darker-grey colours, this makes it accessible to those with colour blindness without the excessive contrast of direct black on white.

## Testing

Cypress was used for both component and ui testing.

For the ui testing, a happy path alongside a 'depressing' path was tested, with the latter being one that encounters many errors when trying to do invalid actions such as inputting invalid values into forms.

Components tested:

- text slide element
- code slide element
- video slide element
- delete slide button
- revision history menu
- edit code modal

Components that have important and distinct functionalities that can be tested were chosen. E.g. Correct code-highlighting for the code element.

## UI/UX considerations

Using a component library like shadcn/ui makes things look quite good from the get-go as they are pre-styled.

- Using a responsive-grid & flexbox which allows the current layout to automatically adjust for the current screen size.
- Keeping key actions and menu items where you would expect them to be. E.g:
  - Account actions in the top-right
  - Presentation actions in a menubar above the slide
- Any buttons used change the cursor on hover to a pointer to make sure the user understands it is clickable.
- Also disabling certain elements when they are not meant to be interacted with, this also changes the previously mentioned pointer-behaviour to not occur.
- Overall, just keeping the layout intuitive and straightforward.
