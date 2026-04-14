# Frontend Mentor - Product preview card component solution

This is my solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa).

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [AI Collaboration](#ai-collaboration)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Links

- Solution URL: [GitHub repository](https://github.com/blessedmbagwu56/product-preview-card-component-main)
- Live Site URL: [View live site](https://blessedmbagwu56.github.io/product-preview-card-component-main/)

## My process

### Built with

- Semantic HTML5 markup
- CSS Flexbox for the two-column layout
- CSS media queries for mobile responsiveness
- The `<picture>` element with `<source>` for responsive images
- Google Fonts (Fraunces & Montserrat)

### What I learned

**The `<picture>` element for responsive images** — I learned you can swap images based on screen size right in HTML:

```html
<picture>
  <source media="(max-width: 600px)" srcset="images/image-product-mobile.jpg" />
  <img src="images/image-product-desktop.jpg" alt="Gabrielle Essence Eau De Parfum" />
</picture>
```

**Media queries for layout changes** — on mobile, the two-column layout flips to a single column:

```css
@media (max-width: 600px) {
  .two-column-layout {
    flex-direction: column;
  }
}
```

**The viewport meta tag is critical** — I lost a lot of time because my mobile view was showing the desktop layout. The fix was adding this single line:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

Without it, phones pretend to be desktop-width and my media queries never kicked in!

### Continued development

- Want to explore CSS Grid as an alternative to Flexbox for two-column layouts
- Learning more about working with different font families and pairings
- Practicing mobile-first design (starting with mobile, then scaling up)

### AI Collaboration

I used **Claude** to help me debug issues like why my mobile view was still showing desktop. The AI walked me through *why* the viewport meta tag matters, which stuck with me better than just being told to add it.

## Author

- GitHub - [@blessedmbagwu56](https://github.com/blessedmbagwu56)
- Frontend Mentor - [@blessedmbagwu56](https://www.frontendmentor.io/profile/blessedmbagwu56)
