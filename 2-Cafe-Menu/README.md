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

53. Você pode dar ao seu menu um pouco mais de espaço entre o conteúdo e os lados com várias propriedades padding.
    Dê à classe menu um padding-left e um padding-right com o mesmo valor de 20px.
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

54. Assim está bem melhor. Agora, tente adicionar o mesmo preenchimento interno de 20px ao topo e à base do menu.
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

55. Já que todos os 4 lados do menu têm o mesmo espaçamento interno, exclua as quatro propriedades
    e use uma única propriedade padding com o valor 20px.
```
.menu {
    width: 80%;
    background-color: burlywood;
    margin-left: auto;
    margin-right: auto;
    padding: 20px;
}
```

56. A largura atual do menu sempre ocupará 80% da largura do elemento body.
    Em uma tela muito ampla, o café e a sobremesa aparecem muito distantes de seus preços.
    Adicione uma propriedade max-width ao menu com um valor de 500px para evitar esse distanciamento em excesso.
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

57. Você pode alterar o estilo de fonte com font-family, para que o texto fique diferente do estilo de fonte padrão do seu navegador.
    Cada navegador tem algumas fontes comuns já disponíveis.
    Mude todo o texto em body, adicionando a propriedade font-family com o valor sans-serif.
    Esta é um fonte bastante comum que é bem legível.
```
body {
    background-color: burlywood;
    background-image: url(https://cdn.freecodecamp.org/curriculum/css-cafe/beans.jpg);
    font-family: sans-serif;
}
```

58. É um pouco chato ler todo um texto com a mesma font-family.
    Você ainda pode ter a maioria do texto em sans-serif e fazer apenas os elementos h1 e h2 terem um seletor diferente.
    Estilize os elementos h1 e h2 para que apenas o texto desses elementos use a fonte Impact.
```
h1, h2 {
    font-family: Impact;
}
```

59. Você pode adicionar um valor de fallback para a font-family adicionando outro nome de fonte separado por uma vírgula.
    Os fallbacks são usados em instâncias onde a fonte inicial não é encontrada ou não está disponível.
    Adicione a fonte de fallback serif após a fonte Impact.
```
h1, h2 {
    font-family: Impact, serif;
}
```

60. Deixe o texto Est. 2020 em itálico criando um seletor de classe established e, logo depois,
    dê a ele a propriedade font-style com o valor italic.
```
.established {
    font-style: italic;
}
```

61. Agora, aplique a classe established ao texto Est. 2020.
    `<p class="established">Est. 2020</p>`

62. A tipografia dos elementos do cabeçalho (por exemplo, h1, h2) é definida por valores padrão dos navegadores dos usuários.
    Adicione dois novos seletores de tipo (h1 e h2).
    Use a propriedade font-size para ambos, mas use o valor de 40px para h1 e 30px para o h2.
```
h1 {
    font-size: 40px;
}

h2 {
    font-size: 30px;
}
```

63. Adicione um elemento footer abaixo do elemento main, onde você pode colocar uma informação adicional sobre o conteúdo da página.
    `<footer></footer>`

64. Dentro do footer, adicione um elemento p.
    Então, aninhe um elemento de âncora (a) no p que encaminhe para https://www.freecodecamp.org e tenha o texto Visit our website.
    `<p> <a href="https://www.freecodecamp.org">Visit our website</a></p>`

65. Adicione um segundo elemento p abaixo do link e dê a ele o texto 123 Free Code Camp Drive.
    `<p>123 Free Code Camp Drive</p>`

66. Você pode usar um elemento hr para exibir um divisor entre seções de conteúdo diferente.
    Primeiro, adicione um elemento hr entre o elemento p com a classe established e o primeiro elemento section.
    Observe que os elementos hr fecham em si mesmos.
    `<hr/>`

67. As propriedades padrão de um elemento hr farão com que ele apareça como uma linha cinza claro fina.
    Você pode alterar a altura da linha especificando um valor para a propriedade height.
    Altere a altura do elemento hr para que seja 3px.
```
hr {
    height: 3px;
}
```

68. Altere a cor de fundo do elemento hr para brown de modo que combine com a cor dos grãos de café.
```
hr {
    height: 3px;
    background-color: brown;
}
```

69. Observe a cor cinza ao longo das arestas da linha.
    Essas arestas são conhecidas como bordas.
    Cada lado de um elemento pode ter uma cor diferente ou eles podem ser todos iguais.
    Faça com que todas as bordas do elemento hr sejam da mesma cor que o fundo dele usando a propriedade border-color.
```
hr {
    height: 3px;
    background-color: brown;
    border-color: brown;
}
```

70. Percebeu como a espessura da linha parece maior?
    O valor padrão da propriedade border-width é de 1px para todas as arestas dos elementos hr.
    Ao alterar a borda para a mesma cor do fundo, a altura total da linha é de 5px (3px mais a largura superior e inferior da borda, de 1px).
    Altere a propriedade height do elemento hr para que seja de 2px, então a altura total dela se tornará 4px.
```
hr {
    height: 2px;
    background-color: brown;
    border-color: brown;
}
```

71. Adicione outro elemento hr entre o primeiro elemento main e o elemento footer. `<hr/>`

72. Para criar um pouco mais de espaço ao redor do menu, adicione 20px de espaço interno ao elemento body usando a propriedade padding.
```
body {
    background-color: burlywood;
    background-image: url(https://cdn.freecodecamp.org/curriculum/css-cafe/beans.jpg);
    font-family: sans-serif;
    padding: 20px;
}
```

73. Se nos concentrarmos nos itens do menu e nos preços, há um espaço relativamente grande entre cada linha.
    Com o foco em todos os elementos p dentro de elementos com a class definida como item, defina a margem superior e inferior para que seja 5px.
```
.item p {
    display: inline-block;
    margin-top: 5px;
    margin-bottom: 5px;
}
```

74. Usando o mesmo seletor de estilo do passo anterior, torne maior o tamanho da fonte dos itens e preços usando um valor de 18px.
```
.item p {
  display: inline-block;
  margin-top: 5px;
  margin-bottom: 5px;
  font-size: 18px;
}
```

75. Alterar margin-bottom para 5px parece uma ótima ideia.
    No entanto, agora o espaço entre o item de menu Cinnamon Roll e o segundo elemento hr não combina com o espaço
    entre o elemento hr de cima e o título Coffee.
    Adicione mais espaço criando uma classe chamada bottom-line, usando 25px para a propriedade margin-top.
```
.bottom-line{
    margin-top: 25px;
}
```

76. Agora, adicione a classe bottom-line ao segundo elemento hr para que o estilo seja aplicado.
    `<hr class="bottom-line" />`

77. Em seguida, você estilizará o elemento footer.
    Para manter o CSS organizado, adicione um comentário ao final de styles.css com o texto FOOTER.
    `/* FOOTER */ `

78. Descendo para o elemento footer, faça com que todo o texto tenha um valor de 14px para o tamanho da fonte.
```
footer {
    font-size: 14px;
}
```

79. A cor padrão de um link que ainda não foi clicado é tipicamente azul.
    A cor padrão de um link que já foi visitado a partir de uma página é tipicamente roxa.
    Para tornar os links do footer da mesma cor, independentemente de um link ter sido visitado,
    use um seletor de tipo para o elemento de âncora (a) e use o valor black para a propriedade color.
```
a {
    color: black;
}
```

80. Você muda as propriedades de um link quando o link tenha sido visitado de fato usando um pseudosseletor,
    que tem essa aparência: a:visited { propertyName: propertyValue; }.
    Mude a cor do rodapé Visit our website para grey quando um usuário tiver visitado o link.

```
a:visited {
    color: gray;
}
```

81. Você muda as propriedades de um link quando o mouse passa sobre ele usando um pseudosseletor,
    que tem essa aparência: a:hover { propertyName: propertyValue; }.
    Mude a cor do rodapé Visit our website para brown quando um usuário passar o mouse sobre ele.
```
a:hover {
    color: brown;
}
```

82. Você muda as propriedades de um link quando o link tiver sido clicado de fato usando um pseudosseletor,
    que tem essa aparência: a:active { propertyName: propertyValue; }.
    Mude a cor do rodapé Visit our website para white quando um usuário clicar no link
```
a:active {
    color: white;
}
```

83. Para continuar com o mesmo tema da cor que você já está usando (preto e marrom),
    altere a cor para quando o link for visitado para black e use brown para quando o link for clicado de fato.
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

84. O texto do menu CAMPER CAFE tem um espaço diferente do topo do que o espaço do endereço na parte inferior do menu.
    Isso se deve ao navegador ter uma margem superior padrão para o elemento h1.
    Altere a margem superior do elemento h1 para 0 para remover toda a margem superior.
```
h1 {
  font-size: 40px;
  margin-top: 0;
}
```

85. Para remover um pouco do espaço vertical entre o elemento h1 e o texto Est. 2020, altere a margem inferior de h1 para 15px.
```
h1 {
    font-size: 40px;
    margin-top: 0;
    margin-bottom: 15px;
}
```

86. Agora o espaçamento superior parece bom.
    O espaço abaixo do endereço na parte inferior do menu é um pouco maior do que o espaço no topo do menu e no elemento h1.
    Para diminuir o espaço de margem padrão abaixo do elemento p do endereço, crie um seletor de classe chamado address
    e use o valor 5px para a propriedade margin-bottom.

```
.address {
    margin-bottom: 5px;
}
```

87. Agora, aplique a classe address ao elemento p que contém o endereço 123 Free Code Camp Drive.
    `<p class="address">123 Free Code Camp Drive</p>`

88. O menu está com uma boa aparência, mas, excetuando a imagem de fundo dos grãos de café, ele é basicamente feito de texto.
    Sob o título Coffee, adicione uma imagem usando o url https://cdn.freecodecamp.org/curriculum/css-cafe/coffee.jpg.
    Dê à imagem um valor alt de coffee icon.
    `<img src="https://cdn.freecodecamp.org/curriculum/css-cafe/coffee.jpg" alt="coffee icon"/>`

89. A imagem adicionada não está centralizada horizontalmente como o título Coffee acima dela.
    Elementos img são similares aos elementos em linha (inline).
    Para fazer com que a imagem se comporte como elementos de título (que são de nível de bloco),
    crie um seletor de tipo img, use o valor block para a propriedade display e use os valores margin-left e margin-right
    aplicáveis para centralizá-la horizontalmente.
```
img {
    display: block;
    margin-left: auto;
    margin-right: auto;
}
```

90. Adicione uma última imagem sob o título Desserts usando o url https://cdn.freecodecamp.org/curriculum/css-cafe/pie.jpg.
    Dê à imagem um valor alt de pie icon.
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