# Transforms
 property to revisited with alternative ways to size, position, and change elements. and it comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values.

 ## Transform Syntax:
  transform property is including the transform property followed by the value. The value specifies the transform type followed by a specific amount inside parentheses.
  transform property includes multiple vendor prefixes to gain the best support across all browsers.



  ``` html
  div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);
}
```

[shayhowe](https://learn.shayhowe.com/advanced-html-css/css-transforms/)


## 2D Transform:
Two-dimensional transforms work on the x and y axes.

some 2D properties:
- 2D Rotate: rotate value provides the ability to rotate an element from 0 to 360 degrees
``` html
<figure class="box-1">Box 1</figure>

.box-1 {
  transform: rotate(20deg);
```

- 2D Scale: change the appeared size of an element. The default scale value is 1, therefore any value between .99 and .01 makes an element appear smaller while any value greater than or equal to 1.01 makes an element appear larger.

```html
<figure class="box-1">Box 1</figure>
.box-1 {
  transform: scale(.75);
}
```

- 2D Translate: translateX value will change the position of an element on the horizontal axis while using the translateY value will change the position of an element on the vertical axis.

```html
<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>
<figure class="box-3">Box 3</figure>

.box-1 {
  transform: translateX(-10px);
}
.box-2 {
  transform: translateY(25%);
}
.box-3 {
  transform: translate(-10px, 25%);
}

```

## 3D Transform
Three-dimensional transforms work on both the x and y axes, as well as the z axis. three-dimensional transforms define the length, width and depth of the element.

- 3D Rotate: With three-dimensional transforms we can rotate an element around any axes. To do so, we use three new transform values, including rotateX, rotateY, and rotateZ.

```html
<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>
<figure class="box-3">Box 3</figure>

.box-1 {
  transform: perspective(200px) rotateX(45deg);
}
.box-2 {
  transform: perspective(200px) rotateY(45deg);
}
.box-3 {
  transform: perspective(200px) rotateZ(45deg);
}
```


# Transitions:
provide a change from one state to another

## ways for determining styles for different states:
:hover, :focus, :active, and :target pseudo-classes.

## transition related properties include:
- transition-property
- transition-duration
- transition-timing-function: set the speed in which a transition will move, linear:same speed, ease-in:start slow then become faster, ease-out :start fast then become slower,  ease-in-out:start slow then spead up the bck to be slow again at the end.
- transition-delay: sets a time value(s,ms), that determines how long a transition should be stalled before executing.

``` html
.box {
  background: #2db34a;
  transition-property: background;
  transition-duration: 1s;
  transition-timing-function: linear;
}
.box:hover {
  background: #ff7b29;
}
```

### Note: The code above are not vendor prefixed, For the best support across all browsers, use vendor prefixes.

## Transitional Properties:
not all properties can be transitioned, these are the properties that may be transitioned:
- background 
- colorbackground
- positionborder
- colorborder
- widthborder
- spacingbottomclipcolorcropfont
- sizefont-weightheightleftletter
- spacingline
- heightmarginmax
- heightmax
- widthmin
- heightmin
- widthopacityoutline
- coloroutline
- offsetoutline
- widthpaddingrighttext
- indenttext
- shadowtopvertical
- alignvisibilitywidthword
- spacingz
- index

# Animations
when multiple change in the state is required, we use Animations insted of Transition

### Animations Keyframes:

To set multiple points at which an element should undergo a transition, use the @keyframes rule. The @keyframes rule includes the animation name, any animation breakpoints, and the properties intended to be animated.

``` html
@keyframes slide {
  0% {
    left: 0;
    top: 0;
  }
  50% {
    left: 244px;
    top: 100px;
  }
  100% {
    left: 488px;
    top: 0;
  }
}
```

[shayhowe](https://learn.shayhowe.com/advanced-html-css/transitions-animations/)


## some CSS transition effects:
 - Fade in:


```html
.fade
{
        opacity:0.5;
}
.fade:hover
{
        opacity:1;
}
```

- Change color:

```html

.color:hover
{
        background:#53a7ea;
}
```


- Grow & Shrink:


```html
.grow:hover
{
        -webkit-transform: scale(1.3);
        -ms-transform: scale(1.3);
        transform: scale(1.3);
}
.shrink:hover
{
        -webkit-transform: scale(0.8);
        -ms-transform: scale(0.8);
        transform: scale(0.8);
}

```


- Rotate elements:


```html
.rotate:hover
{
        -webkit-transform: rotateZ(-30deg);
        -ms-transform: rotateZ(-30deg);
        transform: rotateZ(-30deg);
}
```

-  Square to circle:


```html
.circle:hover
{
        border-radius:50%;
}
```


- 3D shadow:

```html
.threed:hover
{
        box-shadow:
                1px 1px #53a7ea,
                2px 2px #53a7ea,
                3px 3px #53a7ea;
        -webkit-transform: translateX(-3px);
        transform: translateX(-3px);
}
```

- Inset border:


```html
.border:hover
{
        box-shadow: inset 0 0 0 25px #53a7ea;
}
```

[webdesignerdepot](https://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-users)


