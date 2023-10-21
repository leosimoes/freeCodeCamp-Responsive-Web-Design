# freeCodeCamp - Responsive Web Design - Learn Basic CSS by Building a Cafe Menu

## Result
![Cafe-Menu-Image](Cafe-Menu.jpg)


## Steps
The steps to build the project were:
1. Add the <!DOCTYPE html> tag and an html element with a lang attribute of en.
```
<!DOCTYPE html>
<html lang="en"></html>
```

2. Add a head element inside the html element so you can add a title element.
   The text of the title element must be Cafe Menu.
```
<head>
     <title>Cafe Menu</title>
</head>
```

3. Inside the head element, add a meta element with an attribute called charset set to the utf-8 value for
   tell the browser how to encode characters for the page. Note that meta elements close in on themselves.
   `<meta charset="UTF-8"/>`

4. To prepare your code to create content, add a body element below the head element.
   `<body></body>`

5. Add a main element inside the existing body element.
   Later on, it will contain information about the prices of coffees and desserts offered by the café.
   `<main></main>`

6. The name of the café is CAMPER CAFE.
   You must create an h1 element inside the main element.
   Capitalize the name of the coffee shop so it stands out.
   `<h1>CAMPER CAFE</h1>`

7. To let visitors know that the cafe was founded in 2020,
   add a p element below the h1 element with the text Est. 2020.
   `<p>Est. 2020</p>`

8. Add a section element inside the main element so that you have a place to put all the available coffees.
   `<section></section>`

9. Create an h2 element in the section element and give it the text Coffee.
   `<h2>Coffee</h2>`

10. Until now, you have been limited in the presentation and appearance of the content you create.
    To start taking control, add a style element inside the head element.
    `<style></style>`

11. You can add style to an element by specifying it in the style element and setting a property for it.
    Center your h1 element by setting its text-align property to the center value.
```
<style>
   h1{
     text-align: center;
   }
</style>
```

12. In the previous step, you used a type selector to style the h1 element.
    Center the h2 and p elements by adding a new type selector for each to the existing style element.
```
<style>
   h1 {
     text-align: center;
   }
   h2 {
     text-align: center;
   }
   P {
     text-align: center;
   }
</style>
```

13. You can add the same style group to many elements by creating a selector list.
    Each selector is separated by commas.
    Delete the three existing type selectors and replace them with a selector list that centers
    the text for the h1, h2 and p elements.
```
<style>
   h1, h2, p {
     text-align: center;
   }
</style>
```

14. You styled three elements by writing CSS inside the style tags.
    This works, but since there will be several other styles, it's best to put all the styles in a separate file and link to that.
    We create a separate styles.css file for you and switch the editor view to that file.
    You can switch file views in the tabs at the top of the editor.
    Start by rewriting the styles you created in the styles.css file.
    Make sure to delete the opening and closing style tags.

15. Now that you have the CSS in the styles.css file, go ahead and remove the style element and all of its content.
    Once removed, the centered text will return to the left.

16. Now you need to link the styles.css file so that the styles are applied again.
    Add a self-closing link element to the head element.
    Give it the value of the rel attribute from stylesheet and the value of the href attribute from styles.css.
    `<link rel="stylesheet" href="styles.css"/>`

17. To make the page styling look similar on mobile, desktop or laptop,
    you need to add a meta element with a special content attribute.
    Add the following inside the head element: `<meta name="viewport" content="width=device-width, initial-scale=1.0"/>`

18. The text is centered again, so the link to the CSS file is working.
    Add another style to the file that changes the background-color property to brown for the body element.
```
body {
   background-color: brown;
}
```

19. This brown background makes the text difficult to read.
    Change the background color of the body element to burlywood so that it has color but you can still read the text.
```
body {
   background-color: burlywood ;
}
```

20. Unlike the other content elements you've used so far,
    The div element is mainly used for design layout purposes.
    Add a div element inside the body element and then move all other elements inside the new div.
    Inside the div's opening tag, add the id attribute with the menu value.
    `<div id="menu"></div>`

21. Now the objective is to make the div not occupy the entire width of the page.
    The CSS width property is perfect for this.
    You must use the id selector to mark a specific div element.
    An id selector is defined by a name with a hashtag symbol directly in front of it.
    Use the #menu selector to give the element a width of 300px.
```
#menu {
   width: 300px;
}
```

22. Comments in CSS look like this: `/* comment here */`
    In your stylesheet, comment out the line that contains the background-color property and value,
    so you can see the effect of styling just the #menu element. This will make the background white again.
    `/*background-color: burlywood;*/`

23. Now, use the existing #menu selector to set the background color of the div element to be burlywood.
    `background-color: burlywood;`

24. Now it's easy to see that the text is centered inside the #menu element.
    Currently, the width of the #menu element is specified in pixels (px).
    Change the value of the width property to be 80%, which will make it 80% of the width of its parent element (body).
```
#menu {
     width: 80%;
     background-color: burlywood;
}
```

25. Then center the #menu horizontally. You can do this by setting the margin-left and margin-right properties to auto.
    Think of margin as an invisible space around an element.
    Using these two margin properties, center the #menu element inside the body element.
```
#menu {
     width: 80%;
     background-color: burlywood;
     margin-left: auto;
     margin-right: auto;
}
```

26. So far, you have been using type and id selectors to style elements.
    However, it is more common to use a different selector to style the elements.
    A class selector is defined by a name with a dot directly in front of it
    Change the existing #menu selector to a class selector by replacing #menu with a class called .menu.
```
.menu {
     width: 80%;
     background-color: burlywood;
     margin-left: auto;
     margin-right: auto;
}
```

27. To apply the class style to the div element,
    remove the id attribute and add the class attribute to the opening tag of the div element.
    Make sure you set the value of class to menu.
    `<div class="menu">`

28. Since the main product for sale in the coffee shop is coffee, you can use an image of coffee beans for the page background.
    Delete the comment and content within the body type selector.
    Then add a background-image property
    and set its value as url(https://cdn.freecodecamp.org/curriculum/css-cafe/beans.jpg)
```
body {
     background-color: burlywood;
     background-image: url(https://cdn.freecodecamp.org/curriculum/css-cafe/beans.jpg);
}
```

29. Appearance is good. It's time to start adding some menu items.
    Add an empty article element below the Coffee title.
    It will contain the flavor and price of each coffee you offer.
    `<article></article>`

30. Article elements commonly contain several elements that have related information.
    In this case, it will contain a coffee flavor and a price for that flavor.
    Nest two p elements inside the article element.
    The first text must be French Vanilla and the second text must be 3.00.
```
<article>
     <p>French Vanilla</p>
     <p>3.00</p>
</article>
```

31. Starting below the existing coffee/price pair, add the coffees and prices below using article elements
    with two elements nested within each p.
    As before, the first text p must contain the coffee flavor and the second text p must contain the price.
```
Caramel Macchiato 3.75
Pumpkin Spice 3.50
Hazelnut 4.00
Mocha 4.50
```
```
<article>
     <p>French Vanilla</p>
     <p>3.00</p>
</article>
<article>
     <p>Caramel Macchiato</p>
     <p>3.75</p>
</article>
<article>
     <p>Pumpkin Spice</p>
     <p>3.50</p>
</article>
<article>
     <p>Hazelnut</p>
     <p>4.00</p>
</article>
<article>
     <p>Mocha</p>
     <p>4.50</p>
</article>
```

32. The flavors and prices are currently stacked on top of each other and centered with their respective p-elements.
    It would be nice if the flavor was on the left and the price was on the right.
    Add the flavor class name to the p element that says French Vanilla.
    `<p class="flavor">French Vanilla</p>`

33. Using your new flavor class as a selector, set the value of the text-align property to left.
```
.flavor{
     text-align: left;
}
```

34. Next, you must align the price to the right. Add a class called price to your p element that has the text 3.00.
    `<p class="price">3.00</p>`

35. Now align the text with right for the elements with the price class.
```
.price{
     text-align: right;
}
```

36. Now it's closer to what you want, but it would be nice if the taste and price were on the same line.
    p elements are block-level elements, so they occupy the entire width of their parent element.
    To make them stay on the same line, you need to apply some kind of style to the p elements,
    so that they start to behave more like inline elements.
    To do this, start by adding a class attribute with the value item to the first article element under the title Coffee.
    `<article class="item">`

37. The p elements are nested in an article element with the item class attribute.
    You can style all p elements nested anywhere in the elements with a class called item like this:
    `.item p { }`
    Using the selector above, add a display property with inline-block value so that the p elements are
    behave more like in-line elements.
```
.item p {
     display: inline-block;
}
```

38. That's closer, but the price hasn't gone further to the right. This is due to the fact that inline-block elements only
    occupy the width of your content.
    To distribute them, add a width property to the flavor and price class selectors with a value of 50% each.
```
.flavor {
   text-align: left;
   width: 50%;
}

.price {
   text-align: right;
   width: 50%;
}
```

39. Well, that didn't work. Style p elements as inline-block and place them on separate lines in the code
    creates an extra space to the right of the first p element, causing the second to move to the next line.
    One way to fix this is to make the width of each p element less than 50%.
    Change the width of each class to 49% and see what happens.
```
.flavor {
   text-align: left;
   width: 49%;
}

.price {
   text-align: right;
   width: 49%;
}
```

40. Cool, it worked. But there's still a bit of room to the right of the price.
    You could keep trying various percentages for the widths.
    Instead, use the Backspace key on your keyboard to move the p element with the price class to the side
    of the p element with the flavor class so that they are on the same line in the editor.
    Make sure there is no space between them.
    `<p class="flavor">French Vanilla</p><p class="price">3.00</p>`

41. Now go ahead and change the width of the flavor and price classes to 50% again.
```
.flavor {
   text-align: left;
   width: 50%;
}

.price {
   text-align: right;
   width: 50%;
}
```

42. Now that you know it works, you can change the remaining article and p elements to
    correspond to the first set.
    Start by adding the item class to the other article elements.
```
<article class="item">
     <p>Caramel Macchiato</p><p>3.75</p>
</article>
<article class="item">
     <p>Pumpkin Spice</p><p>3.50</p>
</article>
<article class="item">
     <p>Hazelnut</p><p>4.00</p>
</article>
<article class="item">
     <p>Mocha</p><p>4.50</p>
</article>
```

43. Then position the other p elements on the same line, with no space between them.

44. To complete the styling, add the applicable class names flavor and price to all remaining p elements.
```
<article class="item">
     <p class="flavor">Caramel Macchiato</p><p class="price">3.75</p>
</article>
<article class="item">
     <p class="flavor">Pumpkin Spice</p><p class="price">3.50</p>
</article>
<article class="item">
     <p class="flavor">Hazelnut</p><p class="price">4.00</p>
</article>
<article class="item">
     <p class="flavor">Mocha</p><p class="price">4.50</p>
</article>
```

45. If you make the page view width smaller, you will notice, at some point,
    that part of the text on the left starts to wrap to the next line.
    This is because the width of the p elements on the left side can only take up 50% of the space.
    Since you know that the trailing values have significantly fewer characters,
    change the width value of the flavor class to 75% and the width of the price class to 25%.
```
.flavor {
     text-align: left;
     width: 75%;
}

.price {
     text-align: right;
     width: 25%;
}
```

46. You'll still come back to menu styling, but for now,
    add a second section element below the first to show the desserts offered by the café.
    `<section></section>`

47. Add an h2 element in the new section and give it the text Desserts.
    `<h2>Desserts</h2>`

48. Add an empty article element below the Desserts title. Give it a class attribute with the value item.
    `<article class="item"></article>`

49. Place two p elements inside the article element. The text of the first element must be Donut
    and the text of the second must be 1.50.
    Place the two on the same line, ensuring there is no space between them.
    `<p>Donut</p><p>1.50</p>`

50. For the two p elements you just added, add dessert as the value of the class attribute of the
    first element p and price as the value of the class attribute of the second element p.
    `<p class="dessert">Donut</p><p class="price">1.50</p>`

51. Something doesn't seem right. You added the correct value of the class attribute for the p element that
    has the text Donut, but you haven't defined a selector for it.
    The CSS rule for the flavor class already defines the properties you want.
    Add the dessert class as an additional selector for this CSS rule.
```
.flavor, .dessert {
     text-align: left;
     width: 75%;
}
```

52. Below the dessert you just added, add the rest of the desserts and prices using three more elements
    of article, each with two p elements within them. Each element must have the correct dessert and price text.
    Everyone must have the correct classes.
```
Cherry Pie 2.75
Cheesecake 3.00
Cinnamon Roll 2.50
```
```
<article class="item">
     <p class="dessert">Cherry Pie</p><p class="price">2.75</p>
</article>
<article class="item">
     <p class="dessert">Cheesecake</p><p class="price">3.00</p>
</article>
<article class="item">
     <p class="dessert">Cinnamon Roll</p><p class="price">2.50</p>
</article>
```

53. You can give your menu a little more space between the content and sides with various padding properties.
    Give the menu class a padding-left and a padding-right with the same value of 20px.
```
.menu {
     width: 80%;
     background-color: burlywood;
     margin-left: auto;
     margin-right: auto;
     padding-left: 20px;
     padding-right: 20px;
}
```

54. This is much better. Now try adding the same 20px inner padding to the top and bottom of the menu.
```
.menu {
     width: 80%;
     background-color: burlywood;
     margin-left: auto;
     margin-right: auto;
     padding-left: 20px;
     padding-right: 20px;
     padding-top: 20px;
     padding-bottom: 20px;
}
```

55. Since all 4 sides of the menu have the same internal spacing, delete the four properties
    and use a single padding property with the value 20px.
```
.menu {
     width: 80%;
     background-color: burlywood;
     margin-left: auto;
     margin-right: auto;
     padding: 20px;
}
```

56. The current width of the menu will always occupy 80% of the width of the body element.
    On a very wide screen, coffee and dessert appear far removed from their prices.
    Add a max-width property to the menu with a value of 500px to avoid this excessive distance.
```
.menu {
     width: 80%;
     background-color: burlywood;
     margin-left: auto;
     margin-right: auto;
     padding: 20px;
     max-width: 500px;
}
```

57. You can change the font style with font-family, so the text will look different from your browser's default font style.
    Every browser has some common fonts already available.
    Change all text in the body by adding the font-family property with the sans-serif value.
    This is a fairly common font that is very readable.
```
body {
     background-color: burlywood;
     background-image: url(https://cdn.freecodecamp.org/curriculum/css-cafe/beans.jpg);
     font-family: sans-serif;
}
```

58. It's a bit annoying to read an entire text with the same font-family.
    You can still have most of the text in sans-serif and just have the h1 and h2 elements have a different selector.
    Style the h1 and h2 elements so that only the text in these elements uses the Impact font.
```
h1, h2 {
     font-family: Impact;
}
```

59. You can add a fallback value to the font-family by adding another font name separated by a comma.
    Fallbacks are used in instances where the initial source is not found or unavailable.
    Add the serif fallback font after the Impact font.
```
h1, h2 {
     font-family: Impact, serif;
}
```

60. Leave the text Est. 2020 in italics by creating an established class selector and, soon after,
    give it the font-style property with the value italic.
```
.established {
     font-style: italic;
}
```

61. Now, apply the established class to the Est. 2020 text.
    `<p class="established">Est. 2020</p>`

62. The typography of header elements (e.g. h1, h2) is set by default values of users' browsers.
    Add two new type selectors (h1 and h2).
    Use the font-size property for both, but use the value 40px for h1 and 30px for h2.
```
h1 {
     font-size: 40px;
}

h2 {
     font-size: 30px;
}
```

63. Add a footer element below the main element, where you can place additional information about the page content.
    `<footer></footer>`

64. Inside the footer, add a p element.
    Then, nest an anchor element (a) in p that links to https://www.freecodecamp.org and has the text Visit our website.
    `<p> <a href="https://www.freecodecamp.org">Visit our website</a></p>`

65. Add a second p element below the link and give it the text 123 Free Code Camp Drive.
    `<p>123 Free Code Camp Drive</p>`

66. You can use an hr element to display a divider between sections of different content.
    First, add an hr element between the p element with the established class and the first section element.
    Note that the hr elements close on themselves.
    `<hr/>`

67. The default properties of an hr element will make it appear as a thin light gray line.
    You can change the row height by specifying a value for the height property.
    Change the height of the hr element so that it is 3px.
```
hr {
     height: 3px;
}
```

68. Change the background color of the hr element to brown so that it matches the color of the coffee beans.
```
hr {
     height: 3px;
     background-color: brown;
}
```

69. Notice the gray color along the edges of the line.
    These edges are known as edges.
    Each side of an element can have a different color or they can all be the same.
    Make all the borders of the hr element the same color as its background using the border-color property.
```
hr {
     height: 3px;
     background-color: brown;
     border-color: brown;
}
```

70. Notice how the thickness of the line seems thicker?
    The default value of the border-width property is 1px for all edges of hr elements.
    When changing the border to the same color as the background, the total line height is 5px (3px plus the top and bottom border width of 1px).
    Change the height property of the hr element to be 2px, so its total height will become 4px.
```
hr {
     height: 2px;
     background-color: brown;
     border-color: brown;
}
```

71. Add another hr element between the first main element and the footer element. `<hr/>`

72. To create a little more space around the menu, add 20px of space inside the body element using the padding property.
```
body {
     background-color: burlywood;
     background-image: url(https://cdn.freecodecamp.org/curriculum/css-cafe/beans.jpg);
     font-family: sans-serif;
     padding: 20px;
}
```

73. If we focus on menu items and prices, there is a relatively large space between each line.
    With the focus on all p elements within elements with the class set to item, set the top and bottom margin to be 5px.
```
.item p {
     display: inline-block;
     margin-top: 5px;
     margin-bottom: 5px;
}
```

74. Using the same style selector as in the previous step, make the font size of the items and prices larger using a value of 18px.
```
.item p {
   display: inline-block;
   margin-top: 5px;
   margin-bottom: 5px;
   font-size: 18px;
}
```

75. Changing margin-bottom to 5px seems like a great idea.
    However, now the space between the Cinnamon Roll menu item and the second hr element does not match the space
    between the top hr element and the title Coffee.
    Add more space by creating a class called bottom-line, using 25px for the margin-top property.
```
.bottom line{
     margin-top: 25px;
}
```

76. Now add the bottom-line class to the second hr element so that the style is applied.
    `<hr class="bottom-line" />`

77. Next, you will style the footer element.
    To keep your CSS organized, add a comment to the end of styles.css with the text FOOTER.
    `/* FOOTER */ `

78. Moving down to the footer element, make all text a value of 14px for the font size.
```
footer {
     font-size: 14px;
}
```

79. The default color of a link that has not yet been clicked is typically blue.
    The default color of a previously visited link from a page is typically purple.
    To make footer links the same color regardless of whether a link has been visited,
    use a type selector for the anchor element (a) and use the black value for the color property.
```
The {
     color: black;
}
```

80. You change the properties of a link when the link has actually been visited using a pseudo selector,
    which looks like this: a:visited { propertyName: propertyValue; }.
    Change the Visit our website footer color to gray when a user has visited the link.

```
a:visited {
     color: gray;
}
```

81. You change the properties of a link when the mouse hovers over it using a pseudo selector,
    which looks like this: a:hover { propertyName: propertyValue; }.
    Change the Visit our website footer color to brown when a user hovers over it.
```
a:hover {
     color: brown;
}
```

82. You change the properties of a link when the link has actually been clicked using a pseudo selector,
    which looks like this: a:active { propertyName: propertyValue; }.
    Change the Visit our website footer color to white when a user clicks the link
```
a:active {
     color: white;
}
```

83. To continue with the same color theme you are already using (black and brown),
    change the color for when the link is visited to black and use brown for when the link is actually clicked.
```
a:visited {
   color: black;
}

a:hover {
   color: brown;
}

a:active {
   color: brown;
}
```

84. The CAMPER CAFE menu text has a different space at the top than the address space at the bottom of the menu.
    This is due to the browser having a default top margin for the h1 element.
    Change the top margin of the h1 element to 0 to remove the entire top margin.
```
h1 {
   font-size: 40px;
   margin-top: 0;
}
```

85. To remove some of the vertical space between the h1 element and the 2020 Est text, change the bottom margin of h1 to 15px.
```
h1 {
     font-size: 40px;
     margin-top: 0;
     margin-bottom: 15px;
}
```

86. Now the top spacing looks good.
    The space below the address at the bottom of the menu is slightly larger than the space at the top of the menu and in the h1 element.
    To decrease the default margin space below the p element of the address, create a class selector called address
    and use the value 5px for the margin-bottom property.

```
.address {
     margin-bottom: 5px;
}
```

87. Now apply the address class to the p element that contains the address 123 Free Code Camp Drive.
    `<p class="address">123 Free Code Camp Drive</p>`

88. The menu looks good, but other than the background image of coffee beans, it's mostly text.
    Under the heading Coffee, add an image using the url https://cdn.freecodecamp.org/curriculum/css-cafe/coffee.jpg.
    Give the image an alt value of coffee icon.
    `<img src="https://cdn.freecodecamp.org/curriculum/css-cafe/coffee.jpg" alt="coffee icon"/>`

89. The added image is not horizontally centered like the Coffee title above it.
    img elements are similar to inline elements.
    To make the image behave like title elements (which are block level),
    create an img type selector, use the block value for the display property and use the margin-left and margin-right values
    applicable to center it horizontally.
```
img {
     display: block;
     margin-left: auto;
     margin-right: auto;
}
```

90. Add one last image under the Desserts heading using the url https://cdn.freecodecamp.org/curriculum/css-cafe/pie.jpg.
    Give the image an alt value of pie icon.
    `<img src="https://cdn.freecodecamp.org/curriculum/css-cafe/pie.jpg" alt="pie icon" />`

91. It would be nice if the vertical space between h2 elements and their associated icons was smaller.
    H2 elements have the default top and bottom margin space, so you can change the bottom margin of h2 elements to 0 or another number.
    There is an easier way, which is to simply add a negative top margin to the img elements to pull them in
    up from their current positions. Negative values are created by using - in front of the value.
    To complete this project, use a negative top margin of 25px in the img type selector.
```
img {
     display: block;
     margin-left: auto;
     margin-right: auto;
     margin-top: -25px;
}
```


## References
https://www.freecodecamp.org/learn/2022/responsive-web-design/learn-basic-css-by-building-a-cafe-menu/
, accessed on 10/15/2023.