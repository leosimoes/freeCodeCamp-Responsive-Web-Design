# freeCodeCamp - Design responsivo para a web - Aprenda HTML criando um aplicativo de fotos de gatos

## Resultado
![Cat-Photo-App-Image](Cat-Photo-App.jpg)

## Passos
1. Os elementos em HTML têm tags de abertura, como `<h1>`, e tags de fechamento, como `</h1>`.
O texto de um elemento vai entre as tags de abertura e de fechamento.
Encontre o elemento h1 e altere seu texto para: `CatPhotoApp`:
`<h1>CatPhotoApp</h1>`

2. Os elementos de título, que vão de h1 a h6, são usados para dar significado à importância do conteúdo abaixo deles. 
Quanto menor o número, maior a importância. Assim, os elementos h2 têm menos importância que os elementos h1. 
Use apenas um elemento h1 por página e coloque os títulos de importância inferior abaixo dos títulos de maior importância.
Abaixo do elemento h1, adicione um elemento h2 com este texto:`CatPhotoApp`:
`<h2>Cat Photos</h2>`

3. O elemento p é usado para criar um parágrafo de texto nos sites. 
Crie um elemento p abaixo do elemento h2 e dê a ele o seguinte texto:`See more cat photos in our gallery.`
`<p>See more <a target="_blank" href="https://freecatphotoapp.com">cat photos</a> in our gallery.</p>`

4. Colocar comentários permite que você deixe mensagens sem afetar a exibição do navegador. 
Também permite que você deixe o código inativo. 
Um comentário em HTML começa com <!--, contém uma ou várias linhas de texto e termina em -->. 
Por exemplo, o comentário <!-- TODO: Remove h1 --> contém o texto TODO: Remove h1.
Adicione um comentário acima do elemento p com este texto: `TODO: Add link to cat photos`
`<!-- TODO: Add link to cat photos -->`

5. O HTML5 tem alguns elementos que identificam diferentes áreas de conteúdo. 
Essas elementos tornam seu HTML mais fácil de ler e ajudam com a otimização dos mecanismos de busca (SEO) 
e com a acessibilidade.
Identifique a seção principal desta página adicionando uma tag <main> antes do elemento h1 
e uma tag de fechamento </main> depois do elemento p.
```
<main>
    <h1>CatPhotoApp</h1>
    <h2>Cat Photos</h2>
    <!-- TODO: Add link to cat photos -->
    <p>See more cat photos in our gallery.</p>
</main>
```

6. No passo anterior, você colocou os elementos h1 e h2, o comentário e os elementos p dentro do elemento main. 
Isso é chamado de aninhamento. 
Elementos aninhados devem ser colocados dois espaços mais à direita do elemento em qual estão aninhados. 
Este espaçamento é chamado de indentação e é usado para facilitar a leitura do HTML.
Os elementos h1 e h2, assim como o comentário, estão indentados dois espaços adiante do elemento main no código abaixo. 
Use a barra de espaço no seu teclado para adicionar mais dois espaços na frente do elemento p para que 
ele também seja indentado corretamente.
```
<main>
    <h1>CatPhotoApp</h1>
    <h2>Cat Photos</h2>
    <!-- TODO: Add link to cat photos -->
    <p>See more cat photos in our gallery.</p>
</main>
```

7. Você pode adicionar imagens a um site da web usando o elemento img. 
Elementos img têm uma tag de abertura, mas não têm a tag de fechamento. 
A tag de um elemento que não precisa de uma tag de fechamento é conhecida como tag de fechamento automático.
Adicione um elemento img abaixo do elemento p. Neste momento, nenhuma imagem será exibida no navegador.
`<img/>`

8. Atributos em HTML são palavras especiais usadas dentro da tag de abertura de um elemento 
para controlar o comportamento dele. 
O atributo src em um elemento img especifica o URL da imagem (onde a imagem está localizada).
Aqui está um exemplo de um elemento img com um atributo src apontando para o logotipo do freeCodeCamp:
`<img src="https://cdn.freecodecamp.org/platform/universal/fcc_secondary.svg">`
Dentro do elemento existente img, adicione um atributo src com este URL: 
`https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg`
`<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg"/>`

9. Todos os elementos img devem ter um atributo alt. 
O texto de um atributo alt é usado por leitores de tela para melhorar a acessibilidade. 
Ele é exibido se a imagem não puder ser carregada. 
Por exemplo, `<img src="cat.jpg" alt="A cat">` tem um atributo alt com o texto A cat.
Dentro do elemento img, adicione um atributo alt com este texto: `A cute orange cat lying on its back`
`<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" alt="A cute orange cat lying on its back."/>`

10. Você pode fazer uma ligação com outra página usando o elemento de âncora (a). 
Por exemplo, `<a href='https://freecodecamp.org'></a>` faria um link para freecodecamp.org.
Adicione um elemento de âncora após o parágrafo que faça um link para `https://freecatphotoapp.com`. 
Neste momento, o link não será exibido na pré-visualização.
`<a href="https://freecatphotoapp.com"></a>`

11. O texto de um link deve ser colocado entre as tags de abertura e fechamento de um elemento de âncora (a). 
Por exemplo, `<a href="https://www.freecodecamp.org">click here to go to freeCodeCamp.org</a>`
é um link com o texto click here to go to freeCodeCamp.org.
Adicione o texto link to cat pictures ao elemento de âncora. Ele se tornará o texto do link.
`<a href="https://freecatphotoapp.com">link to cat pictures</a>`

12. Você pode transformar qualquer texto em um link, como o texto dentro de um elemento p.
`<p>I think <a href="https://www.freecodecamp.org">freeCodeCamp</a> is great.</p>`
No texto do elemento p, transforme as palavras cat photos em um link adicionando as tags de abertura e fechamento 
de um elemento de âncora (a) ao redor dessas palavras. 
Em seguida, defina o valor do atributo href como `https://freecatphotoapp.com`
`<p>See more <a href="https://freecatphotoapp.com">cat photos</a> in our gallery.</p>`

13. Agora que você transformou o texto de cat photos dentro do elemento p em um link, 
você não precisa do segundo link abaixo do elemento p. 
Exclua todo o elemento de âncora abaixo do elemento p.
`<p>See more <a href="https://freecatphotoapp.com">cat photos</a> in our gallery.</p>`

14. Adicione um atributo target com o valor _blank à tag de abertura do elemento de âncora (a) 
para que o link seja aberto em uma nova guia.
`<p>See more <a href="https://freecatphotoapp.com" target="_blank">cat photos</a> in our gallery.</p>`

15. Nos passos anteriores, você usou um elemento de âncora para transformar texto em um link. 
Outros tipos de conteúdo também podem ser transformados em link, colocando-os dentro de tags de elementos de âncora.
Transforme a imagem em um link, envolvendo-a com as tags dos elementos necessários. 
Use `https://freecatphotoapp.com` como valor do atributo href do elemento de âncora.
```
<a href="https://freecatphotoapp.com">
    <img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" 
         alt="A cute orange cat lying on its back."/>
</a>
```

16. Antes de adicionar conteúdo novo, você deve usar um elemento section para separar o conteúdo de fotos 
de gatos do resto do conteúdo.
Faça com que os elementos h2, de comentário, p e âncora (a) fiquem aninhados em um elemento section.
`<section></section>`

17. É hora de adicionar uma nova seção. Adicione um segundo elemento section abaixo do elemento section existente.
`<section></section>`

18. Dentro do segundo elemento section, adicione um novo elemento h2 com o texto `Cat Lists`.
```
<section>
    <h2>Cat Lists</h2>
</section>
```

19. Quando você adiciona um elemento de título menor à página, é implícito que você está iniciando uma nova subseção.
Depois do último elemento h2 do segundo elemento section, adicione um elemento h3 com este texto: `Things cats love:`
`<h3>Things cats love:</h3>`

20. Após o elemento h3 com o texto Things cats love:, adicione um elemento de lista não ordenada (ul). 
Observe que nada será exibido neste momento.
`<ul></ul>`

21. Use elementos de item de lista (li) para criar itens em uma lista. 
Aqui está um exemplo de itens de lista em uma lista não ordenada:
```
<ul>
  <li>milk</li>
  <li>cheese</li>
</ul>
```
Dentro do elemento ul, aninhe três itens de lista para exibir três coisas que os gatos amam: `cat nip`, `laser pointers`, `lasagna`.
```
<ul>
  <li>cat nip</li>
  <li>laser pointers</li>
  <li>lasagna</li>
</ul>
```

22. Após a lista não ordenada, adicione uma nova imagem com o valor do atributo src definido como: `https://cdn.freecodecamp.org/curriculum/cat-photo-app/lasagna.jpg`
Além disso, defina o valor do atributo alt como: `A slice of lasagna on a plate.`
`<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/lasagna.jpg" alt="A slice of lasagna on a plate."/>`

23. O elemento figure representa um conteúdo auto-contido e permitirá que você associe uma imagem com uma legenda.
Aninhe a imagem que você acabou de adicionar dentro de um elemento figure.
```
<figure>
    <img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/lasagna.jpg" alt="A slice of lasagna on a plate."/>
</figure>
```

24. Um elemento de legenda da figura (figcaption) é usado para adicionar uma legenda para descrever a imagem 
contida dentro do elemento figure. Por exemplo, `<figcaption>A cute cat</figcaption>` adiciona a legenda A cute cat.
Após a imagem dentro do elemento figure, adicione um elemento figcaption com o texto definido como: `Cats love lasagna.`
```
<figure>
    <img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/lasagna.jpg" alt="A slice of lasagna on a plate."/>
    <figcaption>Cats love lasagna.</figcaption>
</figure>
```

25. Enfatize a palavra love no elemento figcaption encapsulando-o em um elemento em.
`<em>love</em>`

26. Após o elemento figure, adicione outro elemento h3 com o texto: `Top 3 things cats hate:`
`<h3>Top 3 things cats hate:</h3>`

27. O código de uma lista ordenada (ol) é semelhante ao de uma lista não ordenada, mas a lista de itens 
em uma lista ordenada é numerada quando eles são exibidos.
Após o último elemento h3 do segundo elemento section, adicione uma lista ordenada com esses três itens de lista:
`flea treatment thunder other cats`
```
<ol>
    <li>flea treatment</li>
    <li>thunder</li>
    <li>other cats</li>
</ol>
```

28. Depois da lista ordenada, adicione outro elemento `figure`.
`<figure></figure>`

29. Dentro do elemento figure que você acabou de adicionar, coloque um elemento img com um atributo 
src definido como `https://cdn.freecodecamp.org/curriculum/cat-photo-app/cats.jpg`.
```
<figure>
    <img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/cats.jpg" />
</figure>
```

30. Para melhorar a acessibilidade da imagem que você adicionou, 
insira um atributo alt com o texto: `Five cats looking around a field.`
```
<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/cats.jpg" 
     alt="Five cats looking around a field."/>
```

31. Depois do último elemento img, adicione um elemento figcaption com o texto `Cats hate other cats`.
`<figcaption>Cats hate other cats.</figcaption>`

32. O elemento strong é usado para indicar que algum texto é de grande importância ou urgência.
Na figcaption que você acabou de adicionar, indique que hate é de grande importância 
envolvendo a palavra em um elemento strong.
`<figcaption>Cats <strong>hate</strong> other cats.</figcaption>`

33. É hora de adicionar uma nova seção. 
Adicione um terceiro elemento section abaixo do segundo elemento section existente.
`<section></section>`

34. Dentro do terceiro elemento section, adicione um elemento h2 com o texto: `Cat Form`
`<h2>Cat Form</h2>`

35. Agora, adicione um formulário para a web para coletar informações de usuários.
Depois do cabeçalho `Cat Form`, adicione um elemento form.
`<form></form>`

36. O atributo action indica para onde os dados do formulário devem ser enviados. 
Por exemplo, `<form action="/submit-url"></form>` informa ao navegador que os dados do formulário devem 
ser enviados para o caminho `/submit-url`.
Adicione um atributo action com o valor `https://freecatphotoapp.com/submit-cat-photo` ao elemento form.
`<form action="https://freecatphotoapp.com/submit-cat-photo"></form>`

37. O elemento input permite a você várias maneiras de coletar dados a partir de um formulário da web. 
Assim como os elementos img, os elementos input são de fechamento automático e não precisam de tags de fechamento.
Adicione um elemento input dentro do elemento form.
`<input/>`

38. Existem muitos tipos de entradas (inputs) que você pode criar usando o atributo type. 
Você pode criar facilmente um campo de senha, um botão de redefinição ou um controle para permitir que 
os usuários selecionem um arquivo armazenado no computador.
Crie um campo de texto para obter a entrada de texto de um usuário adicionando o atributo type com o valor text 
para o elemento input.
`<input type="text"/>`

39. Para que os dados de um formulário sejam acessados pelo local especificado no atributo action, 
você deve dar ao campo de texto um atributo name e atribuir a ele um valor que represente os 
dados que estão sendo enviados. Por exemplo, você pode usar a sintaxe a seguir para um campo de texto 
de endereço de e-mail: `<input type="text" name="email">`.
Adicione o atributo name com o valor catphotourl para o campo de texto.
`<input type="text" name="catphotourl"/>`

40. O texto de placeholder é usado para dar às pessoas uma dica sobre o tipo de informação que deve ser 
inserido em uma entrada (input). 
Por exemplo, `<input type="text" placeholder="Email address">`.
Adicione o placeholder cat photo URL ao elemento input.
`<input type="text" name="catphotourl" placeholder="cat photo URL"/>`

41. Para evitar que um usuário envie o formulário quando as informações necessárias estiverem faltando, 
você precisa adicionar o atributo required a um elemento input. Não há a necessidade de definir um 
valor para o atributo required. Em vez disso, apenas adicione a palavra required (obrigatório) ao elemento input, 
certificando-se de que haja um espaço entre esse atributo e os outros.
`<input type="text" name="catphotourl" placeholder="cat photo URL" required/>`

42. Use o elemento button para criar um botão clicável. 
Por exemplo, `<button>Click Here</button>` cria um botão com o texto Click Here.
Adicione um elemento button com o texto Submit abaixo do elemento input. 
O comportamento padrão de clicar em um botão de formulário sem qualquer atributo envia o formulário 
para o local especificado no atributo action.
`<button>Submit</button>`

43. Mesmo que você tenha adicionado o botão abaixo do campo (input) de texto, eles aparecem um ao lado de outro na página.
Isso ocorre porque os elementos input e button são elementos em linha (inline), que não aparecem em novas linhas.
O botão que você adicionou enviará o formulário por padrão. 
No entanto, confiar no comportamento padrão pode causar confusão.
Adicione o atributo type com o valor submit ao button para deixar claro que ele é um botão de envio.
`<button type="submit">Submit</button>`

44. Você pode usar botões de opção para perguntas onde você queira que o usuário dê apenas uma resposta entre várias opções.
Aqui está um exemplo de um botão de opção com a opção cat: `<input type="radio">` cat. 
Lembre-se de que os elementos input são de fechamento automático.
Antes da entrada de texto, adicione um botão de opção com a opção definida como: `Indoor`
`<input type="radio"/> Indoor`

45. Os elementos label são usados para ajudar a associar o texto de um elemento input com o próprio elemento input 
(especialmente para tecnologias assistivas como leitores de tela). 
Por exemplo, `<label><input type="radio"> cat</label>` torna possível que clicar na palavra cat também selecione
o botão de opção correspondente.
Coloque o botão radio dentro de um elemento label.
`<label><input type="radio"/> Indoor</label>`

46. O atributo id é usado para identificar elementos HTML específicos. 
O valor de cada atributo id deve ser único em comparação aos outros valores de id para a página inteira.
Adicione o atributo id com o valor indoor para o botão de opção. Quando os elementos têm vários atributos, 
a ordem desses atributos não importa.
`<label><input id="indoor" type="radio"/> Indoor</label>`

47. Crie outro botão de opção abaixo do primeiro. 
Coloque-o dentro de um elemento label com Outdoor sendo o texto do label. 
Dê ao botão de opção um atributo id com o valor outdoor.
`<label><input id="outdoor" type="radio" name="indoor-outdoor" value="outdoor"/> Outdoor</label>`

48. Observe que os dois botões de opção podem ser selecionados ao mesmo tempo. 
Para fazer com que selecionar um botão de opção automaticamente desmarque a seleção do outro, 
os dois botões devem ter um atributo de name com o mesmo valor.
Adicione o atributo name com o valor indoor-outdoor para os dois botões de opção.
```
<label><input id="indoor" type="radio" name="indoor-outdoor"/> Indoor</label>
<label><input id="outdoor" type="radio" name="indoor-outdoor"/> Outdoor</label>
```

49. Se você selecionar o botão de opção Indoor e enviar o formulário, os dados de formulário para o 
botão são baseados em seus atributos name e value. Como seus botões de opção não têm um atributo value, 
os dados do formulário incluirão indoor-outdoor=on, o que não é útil quando você tem vários botões.
Adicione um atributo value para os dois botões de opção. 
Por conveniência, defina o atributo value do botão com o mesmo valor do atributo id.
```
<label><input id="indoor" type="radio" name="indoor-outdoor" value="indoor" /> Indoor</label>
<label><input id="outdoor" type="radio" name="indoor-outdoor" value="outdoor"/> Outdoor</label>
```

50. O elemento fieldset é usado para agrupar entradas (inputs) e rótulos (labels) relacionados em um formulário da web. 
Os elementos fieldset são elementos de nível de bloco, o que significa que eles aparecem em uma nova linha.
Coloque os botões de opção Indoor e Outdoor dentro de um elemento fieldset e não se esqueça de indentar os botões de opção.
```
<fieldset>
    <label><input id="indoor" type="radio" name="indoor-outdoor" value="indoor"/> Indoor</label>
    <label><input id="outdoor" type="radio" name="indoor-outdoor" value="outdoor"/> Outdoor</label>
</fieldset>
```

51. O elemento legend atua como uma legenda para o conteúdo do elemento fieldset. 
Ele dá aos usuários um contexto sobre o que devem inserir nessa parte do formulário.
Adicione um elemento legend com o texto `Is your cat an indoor or outdoor cat?` acima dos dois botões de opção.
`<legend>Is your cat an indoor or outdoor cat?</legend>`

52. Em seguida, você vai adicionar alguns novos elementos input ao formulário. 
Adicione outro elemento fieldset diretamente abaixo do elemento fieldset existente.
`<fieldset></fieldset>`

53. Adicione um elemento legend com o texto ` What's your cat's personality?` dentro do segundo elemento fieldset.
`<legend>What's your cat's personality?</legend>`

54. Os formulários normalmente usam caixas de seleção para perguntas que tenham mais de uma resposta.
Por exemplo, aqui temos uma caixa de seleção com a opção tacos: `<input type="checkbox">` tacos.
Abaixo do elemento legend que você acaba de adicionar, adicione um elemento input 
com o atributo type definido como checkbox e dê a ele a opção: `Loving`
`<input type="checkbox"/> Loving`

55. Adicione o atributo id com o valor loving para a caixa de seleção.
`<input type="checkbox" id="loving"/> Loving`

56. Existe outra maneira de associar o texto de um elemento input com o elemento em si. 
Você pode colocar o texto dentro de um elemento label e adicionar um atributo for com o mesmo valor que 
o atributo id do elemento input.
Associe o texto Loving com a caixa de seleção inserindo apenas o texto Loving em um elemento label 
e dando a ele um atributo for apropriado.
`<input id="loving" type="checkbox"/> <label for="loving">Loving</label>`

57. Adicione o atributo name com o valor personality no elemento input da caixa de seleção.
Embora você não veja isso no navegador, fazer isso facilita para o servidor o processamento 
do formulário da web, especialmente quando há várias caixas de seleção.
`<input id="loving" type="checkbox" name="personality"> <label for="loving">Loving</label>`

58. Adicione outra caixa de seleção depois daquela que você acaba de adicionar. 
O valor do atributo id deve ser lazy e o valor do atributo name deve ser o mesmo que o da última caixa de seleção.
Adicione também um elemento label à direita da nova caixa de seleção com o texto Lazy. 
Certifique-se de associar o elemento label com a nova caixa de seleção usando o atributo for.
`<input id="lazy" type="checkbox" name="personality""> <label for="lazy">Lazy</label>`

59. Adicione uma caixa de seleção final após a anterior com um atributo id com o valor energetic. 
O atributo name deve ser o mesmo que o da caixa de seleção anterior.
Adicione também um elemento label à direita da nova caixa de seleção com o texto Energetic. 
Certifique-se de associar o elemento label à nova caixa de seleção.
`<input id="energetic" type="checkbox" name="personality"> <label for="energetic">Energetic</label>`

60. Assim como os botões de opção, os dados de formulário para caixas de seleção marcadas são o par de atributos name/value. 
Embora o atributo value seja opcional, é melhor incluí-lo com todas as caixas de seleção ou botões de opção da página.
Adicione um atributo value a cada caixa de seleção. 
Por conveniência, defina o atributo value de cada caixa de seleção com o mesmo valor do atributo id.
```
<input id="loving" type="checkbox" name="personality" value="loving"> <label for="loving">Loving</label>
<input id="lazy" type="checkbox" name="personality" value="lazy"> <label for="lazy">Lazy</label>
<input id="energetic" type="checkbox" name="personality" value="energetic"> <label for="energetic">Energetic</label>
```

61. Para que uma caixa de seleção ou botão de opção esteja selecionado por padrão, você precisa adicionar 
o atributo checked ao elemento. 
Não há a necessidade de definir um valor para o atributo checked. 
Em vez disso, apenas adicione a palavra checked (selecionado) ao elemento input,
certificando-se de que haja um espaço entre esse atributo e os outros.
Faça com que o primeiro botão de opção e a primeira caixa de seleção estejam selecionados por padrão.
`<label><input id="indoor" type="radio" name="indoor-outdoor" value="indoor" checked/> Indoor</label>`
`<input id="loving" type="checkbox" name="personality" value="loving" checked/> <label for="loving">Loving</label>`

62. Agora você vai adicionar uma seção de rodapé à página.
Depois do elemento main, adicione um elemento footer.
`<footer></footer>`

63. Coloque um elemento p com o texto `No Copyright - freeCodeCamp.org` dentro do elemento footer.
`<p>No Copyright - freeCodeCamp.org</p>`

64. Torne o texto freeCodeCamp.org existente em um link, incluindo-o em um elemento de âncora (a). 
O atributo href deve estar definido como `https://www.freecodecamp.org.`
`<p>No Copyright - <a href="https://www.freecodecamp.org">freeCodeCamp.org</a></p>`

65. Observe que tudo o que você adicionou à página até agora está dentro do elemento body. 
Todos os elementos de conteúdo da página que devem ser renderizados na página ficam dentro do elemento body. 
No entanto, outras informações importantes vão dentro do elemento head.
Adicione um elemento head acima do elemento body.
`<head></head>` 

66. O elemento title determina o que os navegadores mostrarão na barra de título ou na aba da página.
Adicione um elemento title dentro do elemento head usando o texto abaixo: `CatPhotoApp`
`<title>CatPhotoApp</title>`

67. Observe que todo o conteúdo da página está aninhado em um elemento html. 
Todos os outros elementos devem ser descendentes (estar dentro) deste elemento html.
Adicione o atributo lang com o valor en à tag de abertura de html para especificar que o idioma da página é o inglês.
`<html lang="en">`

68. Todas as páginas devem começar com <!DOCTYPE html>. 
Essa string especial é conhecida como uma declaração e garante que o navegador tentará atender às especificações gerais do setor.
Adicione essa declaração como a primeira linha do código.
`<!DOCTYPE html>`

69. Você pode definir o comportamento do navegador adicionando elementos meta de autofechamento em head.
Aqui está um exemplo: `<meta attribute="value">`
Diga ao navegador para colocar a marcação (markup) em diversos idiomas criando um elemento meta como filho do elemento head. 
Defina o atributo charset como UTF-8.
`<meta charset="UTF-8"/>`

## Referências
https://www.freecodecamp.org/portuguese/learn/2022/responsive-web-design/learn-html-by-building-a-cat-photo-app/
, acessado em 25/10/2023.