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
- [Acknowledgments](#acknowledgments)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshot

![Desktop Screenshot](Destop_Screenshot.jpg)
![Mobile Screenshot](Mobile_Screenshot.jpg)

Add a screenshot of your solution. The easiest way to do this is to use Firefox to view your project, right-click the page and select "Take a Screenshot". You can choose either a full-height screenshot or a cropped one based on how long the page is. If it's very long, it might be best to crop it.

Alternatively, you can use a tool like [FireShot](https://getfireshot.com/) to take the screenshot. FireShot has a free option, so you don't need to purchase it. 

Then crop/optimize/edit your image however you like, add it to your project, and update the file path in the image above.

**Note: Delete this note and the paragraphs above when you add your screenshot. If you prefer not to add a screenshot, feel free to remove this entire section.**

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Github Pages](https://willetto.github.io/Frontend-Mentor-Stat-Card-Component/)

## My process

### Built with
- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

**Note: These are just examples. Delete this note and replace the list above with your own choices**

### What I learned

I focused on creating html tags and classes that would be the most useful and accesible. Then I focused on the background, color & font styling. Only then did I focus on making the component responsive. I designed the mobile layout first, and then the media quereies were easy to implement. 

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
