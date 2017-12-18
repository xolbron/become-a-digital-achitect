# Animations
*Written by: Jordan Budisantoso*

## Introduction


This example uses some basic shapes, but puts them in motion. Notice how the animation tag goes between the opening and closing tags for the object.

There are many different animations that we can do. This example demostrates some common types, such as rotation, position, and opacity. Feel free to explore the Resource docuument to see others, and the aframe.io website for a complete list.

Please read the comments in the code for some examples of different animations to try.

### Example 1

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Animations</title>
    <!--The A-frame Link Below may change over time. Therefore check the A-frame Website for the most updated link-->
    <script src="https://aframe.io/releases/0.7.0/aframe.min.js"></script>
  </head>
  <body>
    <a-scene>
      <a-box position="-1 1 -4" rotation="0 0 0" width="1" height="1" depth="1"  color="blue">
            <a-animation 
                attribute="rotation" 
                from="0 0 0" 
                to="0 180 0"
                dur="2000" 
                repeat="1"
                direction="alternate">
            </a-animation>
            
      </a-box>
      
      <a-sphere position="-1 2.5 -4" radius="0.5" color="yellow">
          <a-animation
                attribute="position"
                from="-1 2.5 -4"
                to= "3 1 4"
                dur= "2000"
                repeat="indefinite"
                direction="forwards">
          </a-animation>
      </a-sphere>
      
      <a-cylinder position="3 1 -4" height="2" 
            radius="1" color="blue">
          <a-animation
                attribute="color"
                from="blue"
                to="red"
                dur="1000"
                begin="100"
                repeat="3"
                direction="alternate">
          </a-animation>
      </a-cylinder>
      
      <a-sky color="lightblue"></a-sky>
      </a-scene>
  </body>
</html>
```

Experiment with the different types of animations. Try changing things like the repeat from indefinate to a number, change the from and too values, change the direction from alternate to normal, etc. Also, play with the duration (dur). This is in milliseconds, so 1000 = 1 secod duration. What happens if you take some of the attributes out?

#### Example 2

```html
<!DOCTYPE html>
<html>
  <head>
    <title>A-Frame Animation</title>
    <script src="https://aframe.io/releases/0.3.2/aframe.min.js"></script>
  </head>
  <body>
    <a-scene>
      <a-sphere position="0 0 -3" radius="1" color="green">
            <a-animation
                attribute="color"
                from="green"
                to= "blue"
                dur= "2000"
                repeat="indefinite"
                direction="alternate">
          </a-animation>
      </a-sphere>
      <a-sphere position="0 0 -3" radius="0.95" color="yellow">
          <a-animation
                attribute="position"
                from="0 0 -3"
                to= "0 3 -3"
                dur= "2000"
                repeat="indefinite"
                direction="alternate">
          </a-animation>
      </a-sphere>
      <a-sky color="lightblue"></a-sky>
      </a-scene>
  </body>
</html>
```