# Profile Card

A responsive profile card built with plain HTML and CSS. No frameworks, no JavaScript, no build step.

It shows a name, role, location, bio, quick stats, skill chips, and links to GitHub and email.

## Features

- Responsive layout that works from small phones to desktops
- Automatic dark mode that follows the system setting
- Colors and fonts kept in CSS variables, so retheming is quick
- Hover and focus states on the card and buttons
- Keyboard-friendly focus outlines
- Respects `prefers-reduced-motion`
- Optional availability badge

## Project structure

```
profile-card/
├── index.html    # card markup
├── style.css     # all styling
└── README.md
```

## Getting started

1. Download or clone the project.
2. Put `index.html` and `style.css` in the same folder.
3. Open `index.html` in any browser.

To run it on a local server instead:

```bash
# with Python
python -m http.server 8000

# or with Node
npx serve
```

Then visit `http://localhost:8000`.

## Customizing

### Your details

Edit the text directly in `index.html`: name, role, location, bio, stats, and skills.

Update the two links in the `actions` block:

```html
<a class="btn primary" href="https://github.com/your-username">GitHub</a>
<a class="btn ghost" href="mailto:you@example.com">Email me</a>
```

### Skills

Each skill is a list item. Add the `learning` class for a dashed chip that marks something you are still picking up:

```html
<li>HTML</li>
<li class="learning">Docker (learning)</li>
```

### Profile photo

Replace the avatar `div` with an image. The CSS already supports it:

```html
<img class="avatar" src="your-photo.jpg" alt="Your name">
```

Use a square photo for best results.

### Availability badge

Add this under the bio to show a status with a green dot:

```html
<span class="status">Open to internships</span>
```

### Colors and fonts

All colors live in the `:root` block at the top of `style.css`. Change them there and the whole card updates:

```css
:root {
  --ink: #1f2a5c;      /* headings and primary button */
  --teal: #177a7a;     /* role text and avatar */
  --marigold: #f2b705; /* banner edge and focus ring */
}
```

Dark mode colors are defined in the `@media (prefers-color-scheme: dark)` block just below it.

Fonts are loaded from Google Fonts in the `<head>` of `index.html`: Bricolage Grotesque for headings and DM Sans for body text. If you swap them, update `--font-display` and `--font-body` in the CSS too. The card falls back to system fonts if the fonts fail to load.

## Browser support

Works in current versions of Chrome, Edge, Firefox, and Safari.

## License

Free to use and modify for your own portfolio.
