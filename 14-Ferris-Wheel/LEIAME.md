# freeCodeCamp - Design responsivo para a web - Aprenda animação em CSS construindo uma roda gigante

## Resultado

![Ferris-Wheel-Image](Ferris-Wheel.jpg)


## Passos

1. Comece com o boilerplate padrão. 
Adicione a declaração DOCTYPE e os elementos html (com o idioma definido para o inglês), head e body.
Adicione seu elemento meta com o charset correto, o elemento title e um elemento link que vincule o arquivo ./styles.css.
Defina o título title para Ferris Wheel.
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8"/>
    <meta http-equiv="X-UA-Compatible" content="IE=edge"/>
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>Ferris Wheel</title>
    <link type="text/css" rel="stylesheet" href="./styles.css"/>
</head>
<body>
</body>
</html>
```

2. Adicione uma div dentro do elemento body e dê a ela uma class com o valor wheel.
Dentro do novo div, adicione seis elementos span com uma class definida como line 
e seis elementos div com uma class definida para cabin.
```
<body>
    <div class="wheel">
        <span class="line"></span>
        <span class="line"></span>
        <span class="line"></span>
        <span class="line"></span>
        <span class="line"></span>
        <span class="line"></span>
        <div class="cabin"></div>
        <div class="cabin"></div>
        <div class="cabin"></div>
        <div class="cabin"></div>
        <div class="cabin"></div>
        <div class="cabin"></div>
    </div>
</body>
```

3. Crie um seletor para o elemento .wheel. 
Comece definindo a border para 2px solid black, o border-radius para 50% e a margin-left para 50px.
```
.wheel {
    border: 2px solid black;
    border-radius: 50%;
    margin-left: 50px;
}
```

4. Defina a propriedade position do seletor .wheel para absolute. 
Defina height e width para 55vw cada.
```
.wheel {
    border: 2px solid black;
    border-radius: 50%;
    margin-left: 50px;
    position: absolute;
    height: 55vw;
    width: 55vw;
}
```

5. Dê ao seletor .wheel as propriedades max-height e max-width com o valor de 500px.
```
.wheel {
    border: 2px solid black;
    border-radius: 50%;
    margin-left: 50px;
    position: absolute;
    height: 55vw;
    width: 55vw;
    max-height: 500px;
    max-width: 500px;
}
```

6. Crie um seletor para os elementos .line. 
Comece definindo a background-color para black, width para 50% e height para 2px.
```
.line {
    background-color: black;
    width: 50%; 
    height: 2px;
}
```

7. Defina a position do seletor .line para absolute, a propiedade left para 50% e a propriedade top para 50%.
```
.line {
    background-color: black;
    width: 50%;
    height: 2px;
    position: absolute;
    left: 50%;
    top: 50%;
}
```

8. A propriedade transform-origin é usada para definir o ponto em torno do qual uma transformação CSS é aplicada. 
Por exemplo, ao executar um rotate (o que você fará mais tarde neste projeto), 
o transform-origin determina em torno de qual ponto o elemento é girado.
Defina o seletor .line para ter uma transform-origin de 0% 0%. 
Isso definirá que o ponto de origem seja deslocado 0% da esquerda e 0% a partir de cima, posicionando-o no meio da borda superior do elemento.
```
.line {
    background-color: black;
    width: 50%;
    height: 2px;
    position: absolute;
    left: 50%;
    top: 50%;
    transform-origin: 0% 0%;
}
```

9. Crie um seletor para o segundo elemento .line. 
Defina a propriedade transform para rotate(60deg).
Lembre-se que a propriedade transform permite que você manipule a forma de um elemento. 
Neste caso, usar o valor de rotate(60deg) girará o elemento em torno de seu ponto transform-origin em 60 graus no sentido horário.
```
.line:nth-of-type(2) {
    transform: rotate(60deg);
}
```

10. Usando o mesmo padrão, crie um seletor separado para a terceira .line, quarta .line, quinta .line e sexta .line.
Defina a propriedade transform para a terceira .line para rotate(120deg), 
para a quarta para rotate(180deg), para a quinta para rotate(240deg) e para a sexta para rotate(300deg).
```
.line:nth-of-type(3) {
    transform: rotate(120deg);
}

.line:nth-of-type(4) {
    transform: rotate(180deg);
}

.line:nth-of-type(5) {
    transform: rotate(240deg);
}

.line:nth-of-type(6) {
    transform: rotate(300deg);
}
```

11. Crie um elemento .cabin.
Comece definindo a background-color para red, width para 20% e height para 20%.
```
.cabin {
    background-color: red;
    width: 20%; 
    height: 20%;
}
```

12. Dê à .cabin uma position absolute e uma border de 2px solid.
```
.cabin {
    background-color: red;
    width: 20%;
    height: 20%;
    position: absolute;
    border: 2px solid;
}
```

13. Defina o .cabin para ter uma propriedade transform-origin de 50% 0%. 
Isso definirá que o ponto de origem seja deslocado 50% da esquerda e 0% a partir de cima, posicionando-o no meio da borda superior do elemento.
```
.cabin {
    background-color: red;
    width: 20%;
    height: 20%;
    position: absolute;
    border: 2px solid;
    transform-origin: 50% 0%;
}
```

14. Hora de posicionar as cabines ao redor do roda. 
Selecione o primeiro elemento .cabin. 
Defina a propriedade right como -8.5% e a propriedade top para 50%.
```
.cabin:nth-of-type(1) {
    right: -8.5%;
    top: 50%;
}
```

15. Continuando o padrão, selecione os elementos .cabin a seguir e aplique as regras específicas a eles:
- O segundo .cabin deve ter a propriedade right definida como 17% e a propriedade top definida como 93.5%.
- O terceiro .cabin deve ter a propriedade right definida como 67% e a propriedade top definida como 93.5%.
- O quarto .cabin deve ter a propriedade left definida como -8.5% e a propriedade top definida como 50%.
- O quinto .cabin deve ter a propriedade left definida como 17% e a propriedade top definida como 7%.
- O sexto .cabin deve ter a propriedade right definida como 17% e a propriedade top definida como 7%.
```
.cabin:nth-of-type(2) {
    right: 17%;
    top: 93.5%;
}

.cabin:nth-of-type(3) {
    right: 67%;
    top: 93.5%;
}

.cabin:nth-of-type(4) {
    left: -8.5%;
    top: 50%;
}

.cabin:nth-of-type(5) {
    left: 17%;
    top: 7%;
}

.cabin:nth-of-type(6) {
    right: 17%;
    top: 7%;
}
```

16. A regra @keyframes é usada para definir o fluxo de uma animação CSS. 
Dentro da regra @keyframes, você pode criar seletores para pontos específicos na sequência de animação, 
tais como 0% ou 25%, ou usar from e to para definir o início e o fim da sequência.
Regras @keyframes requerem que um nome seja atribuído a elas, que por sua vez você usará em outras regras para referência. 
Por exemplo, a regra @keyframes freeCodeCamp { } seria nomeada freeCodeCamp.
Hora de começar a animar. Crie uma regra de @keyframes chamada wheel.
```
@keyframes wheel {
}
```

17. Agora, você precisa definir como deve começar sua animação. 
Para fazer isso, crie uma regra 0% dentro da sua regra @keyframes wheel. 
As propriedades que você definiu neste seletor aninhado serão aplicadas no início de sua animação.
Para exemplificar, esta seria uma regra de 12%:
```
@keyframes freecodecamp {
  12% {
    color: green;
  }
}
```
```
@keyframes wheel {
    0% {
    }
}
```

18. Dê a regra 0% uma propriedade transform de rotate(0deg). Isso iniciará uma animação sem rotação.
```
@keyframes wheel {
    0% {
        transform: rotate(0deg);
    }
}
```

19. Agora dê à regra @keyframes wheel um seletor de 100%. 
Dentro disso, defina transform para rotate(360deg). 
Ao fazer isso, sua animação completará uma rotação inteira.
```
@keyframes wheel {
    0% {
        transform: rotate(0deg);
    }
    100% {
        transform: rotate(360deg);
    }
}
```

20. A propriedade animation-name é usada para vincular uma regra @keyframes a um seletor CSS. 
O valor dessa propriedade deve corresponder ao nome da regra @keyframes. 
Dê ao seletor .wheel a propriedade animation-name definida para wheel.
A propriedade animation-duration é usada para definir quanto tempo a sequência da animação deve durar até ser concluída. 
O tempo deve ser especificado em segundos (s) ou em milissegundos (ms). 
Dê ao seletor .wheel a propriedade animation-duration definida para 10s.
```
.wheel {
    border: 2px solid black;
    border-radius: 50%;
    margin-left: 50px;
    position: absolute;
    height: 55vw;
    width: 55vw;
    max-height: 500px;
    max-width: 500px;
    animation-name: wheel;
    animation-duration: 10s;
}
```

21. A propriedade animation-iteration-count define quantas vezes sua animação deve repetir. 
Isso pode ser definido como um número, ou como infinite para repetir indefinidamente a animação. 
Sua roda-gigante nunca deve parar, então defina o seletor de .wheel para ter um animation-iteration-count definido como infinite.
A propriedade animation-timing-function define como a animação deve progredir ao longo do tempo. 
Existem alguns valores diferentes para essa propriedade, mas você quer que a animação da roda-gigante funcione com a mesma taxa de início a fim. 
Defina animation-timing-function como linear no seletor.wheel.
```
.wheel {
    border: 2px solid black;
    border-radius: 50%;
    margin-left: 50px;
    position: absolute;
    height: 55vw;
    width: 55vw;
    max-height: 500px;
    max-width: 500px;
    animation-name: wheel;
    animation-duration: 10s;
    animation-iteration-count: infinite;
    animation-timing-function: linear;
}
```

22. Crie uma regra de @keyframes com o nome cabins. 
Use as mesmas propriedades de sua @keyframes wheel, copiando as regras de 0% e 100%, 
mas defina a propriedade transform do seletor 100% para rotate(-360deg).
```
@keyframes cabins {
    0% {
        transform: rotate(0deg);
    }
    100% {
        transform: rotate(-360deg);
    }
}
```

23. Com o seletor de .wheel, você criou quatro propriedades diferentes para controlar a animação. 
Para o seu seletor de .cabin, você pode usar a propriedade animation para definir tudo ao mesmo tempo.
Defina a propriedade animation da regra .cabin para cabins 10s linear infinite. 
Isso definirá as propriedades de animation-name, animation-duration, animation-timing-function 
e animation-iteration-count nessa ordem.
```
.cabin {
    background-color: red;
    width: 20%;
    height: 20%;
    position: absolute;
    border: 2px solid;
    transform-origin: 50% 0%;
    animation: cabins 10s linear infinite;
}
```


## Referências
https://www.freecodecamp.org/portuguese/learn/2022/responsive-web-design/learn-css-animation-by-building-a-ferris-wheel/
, acessado em 26/11/2023.