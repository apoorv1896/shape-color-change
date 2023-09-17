# shape-color-change
## https://apoorv1896.github.io/shape-color-change/

This is a simple HTML, CSS, and JavaScript project that creates a circle that can change color and shape.
## HTML

The HTML code creates a container div with a circle div inside it. The circle div has a shape div inside it. The shape div is initially a circle, but can be changed to a triangle by clicking the "change shape" button

## CSS

The CSS code styles the container div, the circle div, and the shape div. The container div is centered on the page and has a width and height of 500px. The circle div is positioned absolutely inside the container div and has a width and height of 200px. The shape div is positioned absolutely inside the circle div and has a width and height of 100px.

## JavaScript

The JavaScript code adds event listeners to the "change color" and "change shape" buttons. The "change color" button changes the background color of the circle div to a random color from the Color array. The "change shape" button changes the shape of the shape div from a circle to a triangle and vice versa.

```javascript
        var Color = [
  "red",
  "green",
  "cyan",
  "black",
  "voilet",
  "blue",
  "yellow",
  "purple",
  "orange",
  "lightgreen",
  "lemon",
];
var index = 0 ;
const circle = document.getElementById("circle");
        const shape = document.querySelector(".shape");
        const Changecolor = document.querySelector("#color");
        const changeShape = document.querySelector("#changeShape");
        Changecolor.addEventListener("click",()=>{
          
        if (index === Color.length) {
        index = 0;
  }
        circle.style.backgroundColor = Color[index];
        index++;
        })
        var Tringle = false;
        changeShape.addEventListener("click",()=>{
            if(!Tringle){
                var Shape = document.querySelector(".shape");
                Shape.className = "triangle";
                Tringle = true;
            }
            else{
                var shape = document.querySelector(".triangle");
                shape.className = "shape";
                Tringle = false;
            }
        })
      

```
