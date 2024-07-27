# Mouse_move_shadow

This is a 30-days javascript grinding  
js30 [https://github.com/ningh98/js30]  
16. Mouse move shadow [https://github.com/ningh98/Mouse_move_shadow]

## Table of contents

- [Overview](#overview)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)



## Overview

This HTML, CSS, and JavaScript code creates a web page with a dynamic text shadow effect. The shadow of the text moves in response to the user's mouse movements, creating an interactive and visually engaging experience.

### Screenshot

![](./screenshot.png)


### Links

- Live Site URL: [https://ningh98.github.io/Mouse_move_shadow/]

## My process

### Built with

- HTML
- CSS
- Javascript



### What I learned



```js

const hero = document.querySelector('.hero')
const text = hero.querySelector('h1')
const walk = 100; //100px

function shadow(e){
    const { offsetWidth: width, offsetHeight: height } = hero
    let {offsetX: x, offsetY: y} = e
    if (this !== e.target){
        x = x + e.target.offsetLeft;
        y = y + e.target.offsetTop;
    }

    const xWalk = Math.round((x / width * walk) - (walk / 2))
    const yWalk = Math.round((y / height * walk) - (walk / 2))

    text.style.textShadow = `${xWalk}px ${yWalk}px 0 red`


}

hero.addEventListener('mousemove', shadow)
```