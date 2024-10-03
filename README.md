# Flex Gallery Panels

This project is a simple, responsive flexbox gallery that uses JavaScript to manipulate flex elements for an interactive experience. The images in the gallery expand and reveal hidden text when clicked. The text smoothly transitions in and out as the user interacts with the panels.

## Features

- **Responsive Design**: Uses CSS Flexbox to ensure the layout is responsive and adjusts to various screen sizes.
- **Interactive Panels**: Clicking on a panel causes it to expand, revealing additional text, while shrinking the others.
- **Smooth Transitions**: Transitions for expanding panels and moving text are animated for a visually appealing user experience.
- **Dynamic Content Loading**: JavaScript is used to dynamically control the opening and closing of the panels and apply CSS classes for active states.

![Photo of CSS Variable Practice application](photo-sample.png)

## How It Works

### HTML

- The `div.panels` container holds five `div.panel` elements, each representing a flexbox panel.
- Each panel contains three `<p>` elements with various texts that transition into view when the panel is clicked.

### CSS

- **Flexbox Layout**: The `.panels` class uses `display: flex` to arrange all the `.panel` elements in a row.
- **Transitions**: Panels transition in size (`flex: 1` by default, expanding to `flex: 5` when clicked).
- **Text Transitions**: The text in the panels moves up or down from outside the visible area to the center when the panel becomes "active."
- **Background Images**: Each panel has its own background image, which covers the entire panel using `background-size: cover`.

### JavaScript

- **Event Listeners**: JavaScript selects all `.panel` elements and adds click event listeners to toggle their expanded state.
  - `toggleOpen()`: Adds or removes the "open" class to a panel when clicked, causing it to expand.
  - `toggleActive()`: Ensures the text slides into view only after the flex transition ends by listening for the transition event and toggling the `open-active` class.

## How to Use

1. Clone or download the repository.
2. Open the `index.html` file in any modern browser to view the gallery.
3. Click on any panel to expand it and reveal the text. Clicking it again will close the panel.

## File Structure

- `index.html`: The main HTML file with embedded CSS and JavaScript.
- Images used for the panels are loaded via external URLs from Unsplash.

## Additional Notes

- The fonts used are imported from Google Fonts (`Amatic SC`).
- The JavaScript is kept simple, focusing on toggling CSS classes based on user interaction.

## License

This project is open-source and free to use.
