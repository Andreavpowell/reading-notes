# CSS Transforms

- `transform` gives you alternative ways to size, position, and change elements

## Transform Syntax

- use `transform` followed by it's value
  - `div { -webkit-transform: scale(1.5); -moz-transform: scale(1.5); -o-transform: scale(1.5); transform: scale(1.5); }`
  - vendor prefixes are strongly encouraged for any code in a  production environment

## 2D Transforms

- work on the `x` and `y` axis
- 2D rotate:
  - HTML - `<figure class="box-1">Box 1</figure> <figure class="box-2">Box 2</figure>` CSS - `.box-1 { transform: rotate(20deg); } .box-2 { transform: rotate(-55deg); }`
- 2D scale:
  - HTML - `<figure class="box-1">Box 1</figure> <figure class="box-2">Box 2</figure>` CSS - `.box-1 { transform: scale(.75); } .box-2 { transform: scale(1.25); }`
- 2D translate:
    - `.box-1 { transform: translateX(-10px); }`
  `.box-2 { transform: translateY(25%); }`
  `.box-3 { transform: translate(-10px, 25%); }`
- 2D Skew:
  - `.box-1 { transform: translateX(-10px); } .box-2 { transform: translateY(25%); } .box-3 { transform: translate(-10px, 25%); }`
- combining transforms:
  - `.box-1 { transform: rotate(25deg) scale(.75); } .box-2 { transform: skew(10deg, 20deg) translateX(20px); }`
- transform origin:
  - center of an element
  - `transform-origin: 0 0;`
- perspective:
  - *vanishing point* 
  - use the perspective value within the transform property on individual elements, while the other includes using the perspective property on the parent element residing over child elements being transformed
  - `transform: perspective(200px) rotateX(45deg);`

## 3D Transforms
- `rotateX` value allows you to rotate an element around the `x` axis, as if it were being bent in half horizontally. Using the `rotateY` value allows you to rotate an element around the `y` axis, as if it were being bent in half vertically. Lastly, using the `rotateZ` value allows an element to be rotated around the `z` axis.
- positive values rotate clockwise
- backface visibility:
  - face away from the screen
  - not to see these elements at all, set the `backface-visibility` property to `hidden`

# Transitions & Animations

## Transitional Properties

`background-color`;`background-color`;`background-position`;`border-colorborder-width`;`border-spacing`;`bottom`;`clip`;`color`;`crop`;`font-size`;`font-weight`;`heightleft`;`letter-spacing`;`line-height`;`margin`;`max-height`;`max-width`;`min-height`;`min-width`;`opacity`;`outline-color`;`outline-offset`;`outline-width`;`paddding-right`;`text-indent`;`text-shadow`;`topvertical-align`;`visibilitywidth`;`word-spacing`;`z-index`

## Transition Duration

-  The value of this property can be set using general timing values, including seconds (s) and milliseconds (ms). These timing values may also come in fractional measurements, .2s for example.
- the first property identified within the transition-property property will match up with the first time identified within the transition-duration property, and so forth

## Transition Timing

- `transition-timing-function` property is used to set the speed in which a transition will move. Knowing the duration from the `transition-duration` property a transition can have multiple speeds within a single duration
- `linear` keyword value identifies a transition moving in a constant speed from one state to another
- Each timing function has a cubic-bezier curve behind it, which can be specifically set using the `cubic-bezier(x1, y1, x2, y2)` value

## Transition Delay

- delay sets a time value, seconds or milliseconds, that determines how long a transition should be stalled before executing

## Shorthand Transitions

- transition, capable of supporting all of these different properties and values. Using the transition value alone, you can set every transition value in the order of `transition-property`, `transition-duration`, `transition-timing-function`, and lastly `transition-delay`. 

## Transitional Button

- `button { border: 0; background: #0087cc; border-radius: 4px; box-shadow: 0 5px 0 #006599; color: #fff; cursor: pointer; font: inherit; margin: 0 outline: 0; padding: 12px 20px; transition: all .1s linear; } button:active { box-shadow: 0 2px 0 #006599; transform: translateY(3px); }`

## Animations

- set multiple points at which an element should undergo a transition, use the `@keyframes` rule
  - includes the animation name, any animation breakpoints, and the properties intended to be animated
- `animation-name` property is used with the animation name, identified from the `@keyframes` rule, as the property value. The `animation-name` declaration is applied to the element in which the animation is to be applied to
- Animation Duration, Timing Function, & Delay:
  - behave similarly to transitions
- Animation Iteration:
  - animations run their cycle once from beginning to end and then stop. To have an animation repeat itself numerous times the `animation-iteration-count` property may be used. Values for the `animation-iteration-count` property include either an integer or the infinite keyword

# CSS3 TRANSITIONS THAT WILL WOW YOUR USERS

- https://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-users
- [download the demo files](https://www.webdesignerdepot.com/cdn-origin/uploads7/8-simple-CSS3-transitions-that-will-wow-your-users/demos.zip)

# Buttons Animated

- https://codepen.io/retyui/pen/ByoaXV

# Animaitons: Keyframes

- https://codepen.io/akshaychauhan/pen/oAfae

# 404

- https://codepen.io/kieranfivestars/pen/MYdQxX

# Pure CSS Bounce Animation

- https://codepen.io/dp_lewis/pen/gCfBv

[Home](reading-notes)
