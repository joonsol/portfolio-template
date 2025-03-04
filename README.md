# portfolio-template
# Animated Circles using Anime.js

## Description
This project creates animated circles using JavaScript and Anime.js. The script dynamically generates `div` elements inside two parent containers (`.c1` and `.c2`) and applies a scaling animation to them.

## Features
- Dynamically generates 250 elements in `.c1` and 300 elements in `.c2`.
- Animates the elements using Anime.js.
- Uses staggered animation for a grid-like effect.
- Looping animation with smooth easing transitions.

## Code Explanation

```javascript
const c1 = document.querySelector('.c1')
const c2 = document.querySelector('.c2')

let childElement = null
let num1 = 250
let num2 = 300

appendChild(c1, num1)
appeChild(c2, num2)

function appendChild(child, idx) {
    for (let i = 0; i < idx; i++) {
        childElement = document.createElement('div')
        child.append(childElement)
    }
}

anime({
    targets: '.circle>div',
    scale: [
        { value: .1, easing: 'easeOutSine', duration: 2000 },
        { value: 1, easing: 'easeInOutQuad', duration: 1200 }
    ],
    delay: anime.stagger(200, { grid: [20, 15], from: 'center' }),
    loop: true
});
```

## How to Use
1. Include Anime.js in your HTML file:
   ```html
   <script src="https://cdnjs.cloudflare.com/ajax/libs/animejs/3.2.1/anime.min.js"></script>
   ```
2. Add containers `.c1` and `.c2` to your HTML file:
   ```html
   <div class="c1"></div>
   <div class="c2"></div>
   ```
3. Run the script to see the animations in action.

## Dependencies
- [Anime.js](https://animejs.com/)

## License
This project is open-source and free to use.

