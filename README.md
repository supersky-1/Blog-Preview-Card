# Blog Preview Card

A simple blog preview card built with HTML and CSS. The project displays a centered article card with a thumbnail image, category label, publication date, title, short description, and author footer.

## Overview

This project is a static front-end component. It does not use JavaScript, a build tool, or any framework. The card is styled with plain CSS and can be opened directly in a browser.

## Project Structure

### `blog-card.html`

Contains the page markup:

- Loads the Google Sans font from Google Fonts.
- Links to `blog-preview.css`.
- Creates the main card layout.
- Uses `assets/thumbnail.png` for the card thumbnail.
- Uses `assets/avatar.jpg` for the author avatar.
- Adds `tabindex="0"` to the category label so it can receive keyboard focus.

### `blog-preview.css`

Contains all visual styling:

- Centers the card on the page with flexbox.
- Gives the page a gold background.
- Styles the card with a white background, rounded corners, padding, and shadow.
- Uses a `cardLoad` animation so the card fades in and moves upward on page load.
- Adds hover effects for the thumbnail, label, title, and footer.
- Adds a focus style to the category label.
- Makes the avatar image circular and fit inside the footer button.

### `assets/`

Stores the local images used by the page:

- `thumbnail.png`: Main card thumbnail image.
- `avatar.jpg`: Author avatar image.

## Features

- Responsive viewport centering.
- Card load animation.
- Thumbnail hover scale effect.
- Focusable category label.
- Title hover state.
- Circular avatar button.
- Local image assets.
- No JavaScript required.

## How To View

Open `blog-card.html` in your browser.

Because this project is plain HTML and CSS, no installation step is required.

## Important CSS Concepts Used

### Flexbox Centering

The page uses flexbox to center the card horizontally and vertically:

```css
section {
    display: flex;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
}
```

### Card Layout

The card uses column flexbox so the footer can sit at the bottom:

```css
.card {
    display: flex;
    flex-direction: column;
}

footer {
    margin-top: auto;
}
```

### Focus State

The label is focusable because the HTML includes `tabindex="0"`:

```html
<label for="text" tabindex="0">Learning</label>
```

The focus style is handled in CSS:

```css
label:focus {
    background-color: black;
    color: gold;
    outline-offset: 3px;
}
```

### Avatar Image Fit

The footer button hides overflow, and the image fills the circular space:

```css
button {
    width: 50px;
    height: 50px;
    border-radius: 50%;
    padding: 0;
    border: none;
    overflow: hidden;
}

.avatar img {
    width: 50px;
    height: 50px;
    border-radius: 50%;
    object-fit: cover;
    display: block;
}
```

