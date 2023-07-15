# Frontend Mentor - Four card feature section solution

This is a solution to the [Four card feature section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/four-card-feature-section-weK1eFYK). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [Reference](#reference)
  - [Color](#color)
  - [Typography](#typography)
  - [Font](#font)
- [Run Locally](#run-locally)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size

### Screenshot

| ![Four card feature section desktop screenshot](https://devshaunb.github.io/fem-four-card-feature-section/screenshots/desktop.png) |
| - |
||
| ![Four card feature section mobile screenshot](https://devshaunb.github.io/fem-four-card-feature-section/screenshots/mobile.png)   |

### Links

- Solution URL: [https://www.frontendmentor.io/solutions/four-card-feature-section-using-css-grid-nX1TDYXVwu](https://www.frontendmentor.io/solutions/four-card-feature-section-using-css-grid-nX1TDYXVwu)
- Live Site URL: [https://devshaunb.github.io/fem-four-card-feature-section/](https://devshaunb.github.io/fem-four-card-feature-section/)

## Reference

### Color

#### Primary

- ![hsl(0, 78%, 62%)](https://via.placeholder.com/10/ea5353?text=+) `Red: hsl(0, 78%, 62%)`
- ![hsl(180, 62%, 55%)](https://via.placeholder.com/10/45d3d3?text=+) `Cyan: hsl(180, 62%, 55%)`
- ![hsl(34, 97%, 64%)](https://via.placeholder.com/10/fcaf4a?text=+) `Orange: hsl(34, 97%, 64%)`
- ![hsl(212, 86%, 64%)](https://via.placeholder.com/10/549ef2?text=+) `Blue: hsl(212, 86%, 64%)`

#### Neutral

- ![hsl(234, 12%, 34%)](https://via.placeholder.com/10/4c4e61?text=+) `Very Dark Blue: hsl(234, 12%, 34%)`
- ![hsl(229, 6%, 66%)](https://via.placeholder.com/10/a3a5ae?text=+) `Grayish Blue: hsl(229, 6%, 66%)`
- ![hsl(0, 0%, 98%)](https://via.placeholder.com/10/fafafa?text=+) `Very Light Gray: hsl(0, 0%, 98%)`

### Typography

#### Body Copy

- Font size: 15px

### Font

- Family: [Poppins](https://fonts.google.com/specimen/Poppins)
- Weights: 200, 400, 600

## Run Locally

Clone the project

```bash
  git clone https://github.com/DevShaunB/fem-four-card-feature-section.git
```

Go to the project directory

```bash
  cd fem-four-card-feature-section
```

Run `index.html`

```bash
  <browsername> index.html
```

E.g.

```bash
  firefox index.html
```

```bash
  google-chrome index.html
```

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

- used CSS custom properties and pseudo elements for accent border at top of card

```html
<li class="feature-section__feature-item accent-blue">
  <!-- card markup -->
</li>
```

```css
.accent-blue {
  --clr-accent: hsl(var(--clr-blue-300));
}

.feature-section__feature-item {
  position: relative;
  overflow: hidden;
  /* other styles */
}

.feature-section__feature-item::before {
  content: '';
  position: absolute;
  width: 100%;
  height: 0.25em;
  top: 0;
  left: 0;
  background-color: var(--clr-accent);
}
```

- used CSS grid

```css
.feature-section__feature-list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(19.4375em, 21.875em));
  place-content: center;
  gap: 1.5em;
}

.feature-section__feature-item {
  grid-row: 2 / span 2;
}

.feature-section__feature-item:nth-of-type(2) {
  grid-row: 1 / span 2;
}

.feature-section__feature-item:nth-of-type(3) {
  grid-row: 3 / span 2;
}
```

## Author

- Frontend Mentor - [@DevShaunB](https://www.frontendmentor.io/profile/DevShaunB)
- Twitter - [@DevShaunB](https://www.twitter.com/DevShaunB)

## Acknowledgments

- [Four card feature section challenge](https://www.frontendmentor.io/challenges/four-card-feature-section-weK1eFYK) by [Frontend Mentor](https://www.frontendmentor.io/)
