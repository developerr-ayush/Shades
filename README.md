# Shade.scss

The name "Shade" can convey a sense of depth, dimension, and variation in color. It also aligns with the idea of using CSS to add visual shading and depth to web pages. 

## About this project 
 - Shade can refer to the degree of darkness or lightness in a color, which is a key aspect of CSS/SCSS and design.
 - Shade can also refer to a shelter or protection from light, which could be a nod to the idea of the framework providing structure and support for developers.
 - Additionally, "shade" has a cool and trendy vibe that could make it a memorable and catchy name for a framework.

## Key features
- Grid system 
  - grid created using display grid
  - has potential to choose your own grid system you want to follow for a particular section 
  - maximum of 12 grid can be choosed to create it 
  - by just add one class in parent you will able to create grid with equally divided child automatically without adding any class in child
  - gaps between grid are lot easier to use 
  - most of things are controled by parent element 

There are 2 ways to use this setup

### basic way for beginners
- just download css file and use in your project

## responsiveness


Here's all breakpoint that we have in our shades:

xs: The extra-small breakpoint, which applies to devices with a screen width of 0px or greater (i.e., all devices).
sm: The small breakpoint, which applies to devices with a screen width of 576px or greater.
md: The medium breakpoint, which applies to devices with a screen width of 768px or greater.
lg: The large breakpoint, which applies to devices with a screen width of 992px or greater.
xl: The extra-large breakpoint, which applies to devices with a screen width of 1200px or greater.
xxl: The extra-extra-large breakpoint, which applies to devices with a screen width of 1400px or greater.

Developers can use these breakpoint values to write responsive styles for different screen sizes by just adding a class to the element. lets see that in out `grid-system`

### Grid division - create your own grid system
To use this grid system, you can simply add the appropriate class to the parent container of your HTML elements. For example, if you want to create a grid with 3 columns, you can add the class "grid-3" to the parent container. Then, any child elements of that container will be displayed as a grid with 3 columns.

As soon as you add class in parent every child will take 1 column as per your need, you can also customised it too 

Here is an example of how you can use this grid system in your HTML code:
```
<div class="grid-3">
  <div>Element 1</div>
  <div>Element 2</div>
  <div>Element 3</div>
  <div>Element 4</div>
  <div>Element 5</div>
  <div>Element 6</div>
</div>
```
## Here are all classes options you can add in parent element for creating own grid system

```
grid-1
grid-2
grid-3
grid-4
grid-5
grid-6
grid-7
grid-8
grid-9
grid-10
grid-11
grid-12
```

- now if you want to customise it according to layout you can also add classes to customise it as per your need
- lets take example i want to make 80% - 20% of column you will now you will have to use more number of grids to create it as every grid has equal width 
- that means now you will create grid of 10 by `grid-10` and then in first child you will add `col-8` and in second child you will add `col-2` so it will create 80 - 20 grid
- you can also use it like `grid-5` in parent element and in first child you will add class `col-4` and in second child you will add `col-1` it
- totally depends on creativity how you want that to be.
- in total we have 12 grid so as per that we also have 12 `col`

### now lets consider space between these grids too 
if you want to add gaps in between these grid you can use `gap-n` where `n` can range of `1-12` numbers where 1 means 5px of space in between columns

#### here are all classes for gaps in between grid which will be added in parent

```
gap-0 = 0
gap-1 = 5px
gap-2 = 10px
gap-3 = 15px
gap-4 = 20px
gap-5 = 25px
```

### lets get into code for grid system 
- creating grid with 4 equal items in a row with gap of 15px 
```
   <div class="grid-4 gap-3"></div>
```

- creating grid with 2 unequal item with gap of 5px in 70% width for 1st - 30% width for 2nd element
```
  <div class="grid-10 gap-1">
        <div class="col-7"></div>
        <div class="col-3"></div>
   </div>
``` 
- creating grid with 3 unequal item with gap of 10px , 60% width for 1st element - 20% width for 2nd and 3rd element
```
    <div class="grid-10 gap-2">
        <div class="col-6"></div>
        <div class="col-2"></div>
        <div class="col-2"></div>
   </div>
``` 
- creating grid with 5 items which will be in 2 rows  
- first element will have 80% of width
- second element will have 20% of width
- third, fourth and fifth element will have equal of width in second row
- ofcourse for this there can be many ways we can use here are 2 ways of it
- first way for approx
```
   <div class="grid-12 gap-2">
        <div class="col-9"></div>
        <div class="col-3"></div>
        <div class="col-4"></div>
        <div class="col-4"></div>
        <div class="col-4"></div>
   </div>
```
- second way for exact
```
    <div class="grid-5 gap-1">
        <div class="col-4"></div>
        <div class="col-1"></div>
    </div>
    <div class="grid-3 gap-1">
        <div></div>
        <div></div>
        <div></div>
    </div>
```
- For making it responsive just add breakpoint after `col-x-y` where x stands for breakpoint and y stands for value
- for example if you want to show 2 column in a row in mobile device and 4 column in a row in desktop then you will use below code
```
    <div class="grid-2 grid-lg-4">
        <div></div>
        <div></div>
        <div></div>
        <div></div>
    </div>
```




### advanced way
- make sure that you have installed node and npm in your system 
- clone this repo `https://github.com/shahayush480/default-setup.git`
- use `npm install` and then `npm start` to run this repo
- here you go with our project setup and now you can customisie most of things in this code and get the code you want in your project 



## ignore below this it is still in progress

This is a SASS code snippet that defines two maps, $colors and $breakpoints.

The $colors map contains various color values, grouped into two categories: theme colors and system colors. Theme colors are named according to their intended usage, such as 'primary', 'secondary', and 'accent', and have three variants each: light, regular, and dark. System colors, on the other hand, are named based on their actual color, such as 'pure-white', 'pure-black', and 'grey', and also include a few named colors for specific purposes, such as 'info', 'error', 'success', and 'warning'.

The $breakpoints map contains the breakpoints for the responsive design of the website, with each key being a name for the breakpoint, such as 'xs', 'sm', 'md', 'lg', 'xl', and 'xxl', and each value being the corresponding width in pixels. These breakpoints can be used in conjunction with SASS's built-in mixins, such as @media screen and (min-width: map-get($breakpoints, sm)) to apply styles only to screens with a width greater than the value defined for the 'sm' breakpoint.


Documentation for the CSS Code
This is a set of CSS styles that defines a color palette and some default styles for HTML elements.

Color Palette
The color palette is defined using custom properties. Each color has a light, regular, and dark shade, plus some other colors used for backgrounds or text.

Primary Colors
--primary-light: #9ce5e9
--primary: #2ec9d1
--primary-dark: #1d7d82
Secondary Colors
--secondary-light: #7e1c79
--secondary: #d12ec9
--secondary-dark: #e898e4
Accent Colors
--accent-light: #84891e
--accent: #c9d12e
--accent-dark: #e3e794
Other Colors
--pure-white: #fff
--pure-black: #000
--white: #f7f7fa
--black: #212529
--grey: #ccc
--grey-light: #efefef
--grey-dark: #6c757d
--neutral: #28293d
--info: #0163f7
--error: #ff3c3a
--success: #09c270
--warning: #fe8800
To use one of these colors, you can reference it using the custom property. For example, to set the text color to the primary light color, you would use color: var(--primary-light);.

Default Styles
The CSS also includes some default styles for HTML elements, which you can use as a starting point for your own styles.

Reset Styles
The first part of the CSS applies a set of reset styles to all elements, removing margins, padding, and setting the box-sizing property to border-box.

Font Styles
The font-family property is set to a fallback list of system fonts, with the primary font being Arial. The font-size is set to 1.4rem for most elements, with some exceptions for headings and other elements.

Heading Styles
The headings (h1 to h6) have font-sizes ranging from 1.4rem to 2.8rem, with larger sizes on larger screens. They also have a margin of half the default spacing above and below.

Body Styles
The body element has a background-color of the --grey-color custom property (not defined in the code shared) and all links have no underline by default.

Color Styles
Finally, the CSS defines a set of text and background color classes for each color in the palette. These can be used to set the color of text or background by applying the relevant class to the element.