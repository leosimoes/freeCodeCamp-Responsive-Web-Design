# freeCodeCamp - Responsive Web Design - Learn the CSS Box Model by Building a Rothko Painting

## Result

![Rothko-Painting-Image](Rothko-Painting.jpg)


## Steps

1. Now, you should be familiar with the basic elements that an HTML page must have.
   Define your code with a DOCTYPE declaration and the html (with the language set to English), head and body elements.
```
<!DOCTYPE html>
<html lang="en"></html>
```

2. Inside the head element, add a meta tag that defines the charset as UTF-8 and a title element with the value Rothko Painting.
   Inside the body element, add an img element with a src of `https://cdn.freecodecamp.org/curriculum/css-box-model/diagram-1.png`.
```
<head>
     <meta charset="UTF-8"/>
     <title>Rothko Painting</title>
</head>
<body>
     <img src="https://cdn.freecodecamp.org/curriculum/css-box-model/diagram-1.png" />
</body>
```

3. In the CSS box model, all HTML elements are treated as a box with four areas.
   Imagine you received a box from your favorite online store -- the contents are the item in the box, or in our case,
   a header, paragraph, or image element.
   Change the src attribute in the `<img>` of `https://cdn.freecodecamp.org/curriculum/css-box-model/diagram-1.png`
   to `https://cdn.freecodecamp.org/curriculum/css-box-model/diagram-2.png`.
```
<img src="https://cdn.freecodecamp.org/curriculum/css-box-model/diagram-2.png" />
```

4. The content is surrounded by a space called padding, in the same way as plastic wrap.
   bubble separates an item from the box around it.
   Think of the border as the box the item was shipped in.
   Change the src attribute to `https://cdn.freecodecamp.org/curriculum/css-box-model/diagram-3.png`
```
<img src="https://cdn.freecodecamp.org/curriculum/css-box-model/diagram-3.png" />
```

5. The margin is the area outside the box and can be used to control the space between other boxes or elements.
   Here, the bottom element has a larger top margin, pushing it further down the page.
   Now that you understand the CSS box model, let's start working on the Rothko painting.
   Remove the `<img>` element.

6. Add a div element to the body.
   Set the class attribute to canvas.
   This element will act as the canvas for your painting.
```
<div class="canvas"></div>
```

7. Before you start styling the div you added, you need to link the CSS to the HTML.
   Add a link element to link the styles.css file. Set the href to styles.css
   and remember to set the rel attribute as stylesheet.
```
  <link type="text/css" rel="stylesheet" href="styles.css"/>
```

8. Even though the <div> has no text, it is still treated as a box with content.
   Write a new CSS rule that uses the .canvas selector and sets the width to 500 pixels.
   Here is a CSS rule that sets the width of the card class to 300 pixels:
```
.card {
   width: 300px;
}
```
```
.canvas {
     width: 500px;
}
```

9. Add the height property with a value of 600px to the .canvas rule.
```
.canvas {
     width: 500px;
     height: 600px;
}
```

10. Change the screen background-color to #4d0f00.
```
.canvas {
     width: 500px;
     height: 600px;
     background-color: #4d0f00;
}
```

11. Every painting needs a frame.
    Wrap the .canvas element in another div.
    Give the div the frame class.
```
<div class="frame">
     <div class="canvas"></div>
</div>
```

12. Write a new rule using the .frame class selector.
    Use the border shorthand declaration to give the .frame element a solid black border with a width of 50px.
```
.frame {
     border: solid black 50px;
}
```

13. The frame is too wide.
    In the .frame selector, set the width to 500 pixels.
```
.frame {
     border: solid black 50px;
     width: 500px;
}
```

14. Use padding to adjust the spacing within an element.
    In .frame, use the padding shorthand property to increase the space between the .frame and .canvas elements by 50px.
    The shorthand property will increase the space above, below, left and right of the element and canvas border
    inside him.
```
.frame {
     border: solid black 50px;
     width: 500px;
     padding: 50px;
}
```

15. Use margins to adjust the spacing outside an element.
    Using the margin property, give the .frame element a vertical margin of 20px and a horizontal margin of auto.
    This will move the frame down 20 pixels and center it on the page horizontally.
```
.frame {
     border: solid black 50px;
     width: 500px;
     padding: 50px;
     margin: 20px auto;
}
```

16. Add a new div element below the .canvas element.
    Give the new div element the class attribute with the value of one. This will be your first rectangle.
```
<div class="one"></div>
```

17. Write a new rule that targets .one and sets its width to 425 pixels.
```
.one {
     width: 425px;
}
```

18. Now set the height for .one to 150 pixels.
```
.one {
     width: 425px;
     height: 150px;
}
```

19. Set the background-color of the .one element to #efb762.
```
.one {
     width: 425px;
     height: 150px;
     background-color: #efb762;
}
```

20. Use margins to position the .one element on the screen.
    Add the margin shorthand property with a vertical margin of 20px and a horizontal margin of auto.
```
.one {
     width: 425px;
     height: 150px;
     background-color: #efb762;
     margin: 20px auto;
}
```

21. Now .one is centered horizontally, but its top margin is beyond the screen limits
    and entering the edge of the frame, shifting the entire screen 20 pixels down.
    Add a 1px padding to the .canvas element to give the .one element something solid as a barrier.
```
.canvas {
     width: 500px;
     height: 600px;
     background-color: #4d0f00;
     padding: 1px;
}
```

22. Adding 1 padding pixel to the top, bottom, left and right parts of the screen changed its dimensions
    to 502 pixels x 602 pixels.
    Replace the padding property with overflow set to hidden - which returns the screen to its original dimensions.
```
.canvas {
     width: 500px;
     height: 600px;
     background-color: #4d0f00;
     overflow: hidden;
}
```

23. Add another div with class having the value two just below its one element. This will be your second rectangle.
```
<div class="two"></div>
```

24. Create a CSS rule that uses the .two selector and sets the width to 475 pixels.
```
.two {
     width: 475px;
}
```

25. Set the height of the .two element to 200 pixels.
```
.two {
     width: 475px;
     height: 200px;
}
```

26. Set the background-color of the .two element to #8f0401.
```
.two {
     width: 475px;
     height: 200px;
     background-color: #8f0401;
}
```

27. Center the .two element by setting the margin to auto.
```
.two {
     width: 475px;
     height: 200px;
     background-color: #8f0401;
     margin: auto;
}
```

28. Create a div with the class having the value of three just below the .two element. This will be your third rectangle.
```
<div class="three"></div>
```

29. You don't always need to use pixels when sizing an element.
    Create a new rule, .three, and set its width to 91%.
```
.three {
     width: 91%;
}
```

30. Set the height of .three to 28%.
```
.three {
     width: 91%;
     height: 28%;
}
```

31. Change the background-color of the .three element to #b20403.
```
.three {
     width: 91%;
     height: 28%;
     background-color: #b20403;
}
```

32. Center the .three element on the screen by setting the margin to auto.
```
.three {
     width: 91%;
     height: 28%;
     background-color: #b20403;
     margin: auto;
}
```

33. It's helpful to have your margins push in a certain direction.
    In this case, the bottom margin of the .one element pushes .two 20 pixels down.
    In the .two selector, use the margin shorthand property to set the top margin to 0,
    the horizontal margin as auto and the bottom margin as 20px.
    This will remove the top margin, center the element horizontally, and set the bottom margin to 20 pixels.
```
.two {
     width: 475px;
     height: 200px;
     background-color: #8f0401;
     margin: 0 auto 20px;
}
```

34. The colors and shapes of the painting are too accurate to pretend that it is a Rothko painting.
    Use the filter property to blur the painting by 2px on the .canvas element.
    Here's an example of a rule that adds a 3px blur:
```
P {
     filter: blur(3px);
}
```
```
.canvas {
     width: 500px;
     height: 600px;
     background-color: #4d0f00;
     overflow: hidden;
     filter: blur(2px);
}
```

35. Create a rule that targets .one and .two and increases the blur effect to 1 pixel.
```
.one, .two {
     filter: blur(1px);
}
```

36. Increase the blur value of .three by 2 pixels.
```
.three {
     width: 91%;
     height: 28%;
     background-color: #b20403;
     margin: auto;
     filter: blur(2px);
}
```

37. The rectangles are too small and their edges do not have a smooth painterly quality.
    Increase the area and soften the edges of .one by setting its box-shadow to 0 0 3px 3px #efb762.
```
.one {
     width: 425px;
     height: 150px;
     background-color: #efb762;
     margin: 20px auto;
     box-shadow: 0 0 3px 3px #efb762;
}
```

38. Use the same box-shadow declaration for .two, but change the color from #efb762 to #8f0401.
```
.two {
     width: 475px;
     height: 200px;
     background-color: #8f0401;
     margin: 0 auto 20px;
     box-shadow: 0 0 3px 3px #8f0401;
}
```

39. Add a box-shadow to .three with the values 0 0 5px 5px #b20403.
```
.three {
     width: 91%;
     height: 28%;
     background-color: #b20403;
     margin: auto;
     filter: blur(2px);
     box-shadow: 0 0 5px 5px #b20403;
}
```

40. The corners of each rectangle are still very sharp.
    Round each corner of the .one element by 9 pixels using the border-radius property.
```
.one {
     width: 425px;
     height: 150px;
     background-color: #efb762;
     margin: 20px auto;
     box-shadow: 0 0 3px 3px #efb762;
     border-radius: 9px;
}
```

41. Use the border-radius property in the .two selector to set the top left and bottom right radii to 8px
    and the top right and bottom left corner radii as 10px.
```
.two {
     width: 475px;
     height: 200px;
     background-color: #8f0401;
     margin: 0 auto 20px;
     box-shadow: 0 0 3px 3px #8f0401;
     border-radius: 8px 10px;
}
```

42. The border-radius property accepts up to four values to round the top left corners,
    top right, bottom right and bottom left.
    Round the top left corner of .three by 30 pixels, the top right corner by 25 pixels,
    the bottom right corner at 60 pixels and the bottom left corner at 12 pixels.
```
.three {
     width: 91%;
     height: 28%;
     background-color: #b20403;
     margin: auto;
     filter: blur(2px);
     box-shadow: 0 0 5px 5px #b20403;
     border-radius: 30px 25px 60px 12px;
}
```

43. Rotate all the rectangles to give them more of an imperfect, hand-painted look.
    Use the transform property on the .one selector with the value rotate to rotate the element counterclockwise by 0.6 degrees.
```
.one {
     width: 425px;
     height: 150px;
     background-color: #efb762;
     margin: 20px auto;
     box-shadow: 0 0 3px 3px #efb762;
     border-radius: 9px;
     transform: rotate(-0.6deg);
}
```

44. Rotate the .two element clockwise by 0.4 degrees.
```
.two {
     width: 475px;
     height: 200px;
     background-color: #8f0401;
     margin: 0 auto 20px;
     box-shadow: 0 0 3px 3px #8f0401;
     border-radius: 8px 10px;
     transform: rotate(0.4deg);
}
```

45. Rotate .three counterclockwise by 0.2 degrees.
    With this last step, the Rothko painting is complete.
```
.three {
     width: 91%;
     height: 28%;
     background-color: #b20403;
     margin: auto;
     filter: blur(2px);
     box-shadow: 0 0 5px 5px #b20403;
     border-radius: 30px 25px 60px 12px;
     transform: rotate(-0.2deg);
}
```


## References
https://www.freecodecamp.org/learn/2022/responsive-web-design/learn-the-css-box-model-by-building-a-rothko-painting/
, accessed on 11/05/2023.