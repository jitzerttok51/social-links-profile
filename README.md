# Frontend Mentor - Social links profile solution

This is a solution to the [Social links profile challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/social-links-profile-UG32l9m6dQ). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)

### The challenge

Users should be able to:

- See hover and focus states for all interactive elements on the page

### Links

- Live Site URL: [Add live site URL here](https://jitzerttok51.github.io/social-links-profile/)

## My process

### Built with

- Semantic HTML5 markup
- Flexbox
- CSS Animations
- Mobile-first workflow
- Vanilla JS

### What I learned

In this excersize I've learned how to make hover animations. I've went through the CSS `transition` property but then looked into CSS `keyframe animations`. The final solutions uses CSS animations which are applied by responding to the hover event on the button.

```css
li:hover {
  animation: hover-in var(--animation-time) ease-in;
}

.remove-hover {
  animation: hover-out var(--animation-time) ease-out;
}

@keyframes hover-in {
  from {
    background-color: var(--theme-color-gray-777);
  }
  to {
    background-color: var(--theme-color-green);
    color: var(--theme-color-gray-777);
  }
}

@keyframes hover-out {
  from {
    background-color: var(--theme-color-green);
    color: var(--theme-color-gray-777);
  }
  to {
    background-color: var(--theme-color-gray-777);
  }
}
```
```js
document.querySelectorAll("li").forEach(el => {
  el.classList.add("remove-hover");
    const addHover = () => {
      el.removeEventListener("mouseover", addHover);
    };
  el.addEventListener("mouseover", addHover);
});
```
