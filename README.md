# Frontend Mentor - Stats preview card component solution

This is a solution to the [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:
- View the optimal layout depending on their device's screen size

### Screenshot

![Desktop Screenshot](https://github.com/willetto/Frontend-Mentor-Stat-Card-Component/blob/1e4b11be24059387acfec6b25a850b843c1bdf06/Desktop%20Screenshot.png)
![Mobile Screenshot](https://github.com/willetto/Frontend-Mentor-Stat-Card-Component/blob/31c029919374ef0b503a2b2af209921e4afa4114/Mobile%20Screenshot.png)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Github Pages](https://willetto.github.io/Frontend-Mentor-Stat-Card-Component/)

## My process
I focused on creating html tags and classes that would be the most useful and accesible. Then I focused on the background, color & font styling. Only then did I focus on making the component responsive. I designed the mobile layout first, and then the media quereies were easy to implement. 

### Built with
- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

Below is how I applied the stylesheet color to the B&W image with two overlays to make it as close to the design as possilbe.

```css
.hero-image img {
  position: relative;
  z-index: 1;
  inset: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  opacity: 0.8;
}
.hero-image::before {
  content: "";
  position: absolute;
  inset: 0;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  z-index: 1;
  background: var(--violet-accent);
  mix-blend-mode: screen;
}
.hero-image::after {
  content: "";
  position: absolute;
  inset: 0;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  z-index: 2;
  background: var(--violet-accent);
  mix-blend-mode: multiply;
}
```

### Continued development

The project files came with two pictures of just slightly different sizes, and I couldn't figure out how to swap images at a certian size. I used MDN's resources on it as well. I think one problem was that the Desktop image was actually skinnier, but taller. But it seems the srcset tag makes iimage replacement based on width, so my needs were backwards from waht it was designed to do.

### Useful resources

- [Kevin Powell ::before & ::after tricks Video](https://www.youtube.com/watch?v=QFjqxVMwIl8&t=437s&ab_channel=KevinPowell) - I had seen this recently and used his method for adding multiple overlay layers to the image to get it as clost to possible to the design.

## Author

- Website - [Trey Willetto](https://www.treywilletto.com)
- Frontend Mentor - [@willetto](https://www.frontendmentor.io/profile/willetto)
