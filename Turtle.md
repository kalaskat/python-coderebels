## Co je to knihovna turtle

`turtle` je předinstalovaná knihovna, díky které může uživatel vytvářet různé obrázky a tvary na virtuálním plátně. Peru, kterým kreslíme, se říká turtle (anglicky želva) a podle toho je celá knihovna pojmenovaná. Ve zkratce, knihovna turtle ukazuje programování v interaktivní podobě.

S touto knihovnou můžete vykreslovat a vytvářet různé variace tvarů a obrazců. Zde je malá ukázka:

![ukazka](turtle1.gif)

## Začínáme programovat s turtle

Jak jsme si již řekli, turtle je předinstalovaná knihovna, proto se nemusíme trápit s její instalací. Vše, co musíme udělat, je knihovnu naimportovat. V pythonu pomocí příkazu `import`. 

```python
import turtle
```

Nyní, když máme knihovnu importovanou, můžeme se vrhnout na programování. Turtle je grafická knihovna, což znamená, že si musíme vytvořit oddělené okno (obrazovku), do kterého budeme kreslit. To můžeme vytvořit tak, že pro něj inicializujeme proměnnou.
To uděláme následovně:

(s = screen)

```python
s = turtle.getscreen()
```

Nyní bychom měli vidět nové okno (obrazovku):
![turtle2](turtle2.png)

Na této obrazovce můžete sledovat výstup vašeho programu (kódu). Ta malá černá šipka uprostřed obrazovky se nazívá turtle.

Dále si nastavíme proměnnou t (jako turtle), kterou budeme v programu používat jako odkaz na naši turtle.

```python
t = turtle.Turtle()
```
Nyní máme obrazovku a turtle. Obrazovka funguje jako plátno a turtle jako pero, které můžeme naprogramovat tak, aby se hýbalo a kreslilo na obrazovce. Turtle má nějaké měnitelné vlastnosti jako je velikost, barva a rychlost. Vždy míří konkrétním směrem a dokud jí jiný směr nenaprogramujeme, tak bude kreslit tím daným směrem.

Když míří nahoru, znamená to, že při pohybu nebude vykreslovat žádné čáry.
Když míří dolů, bude při pohybu vykreslovat čáry.

## Programování turtle

První věc, kterou se naučíme, je jak s turtle hýbat směrem, kterým chceme. Dále si ukážeme, jak turtle měnit a jak programovat její okolí. Nakonec se naučíme i nějaké extra příkazy, které vykonávají speciální úkoly.

### Pohyb

Turtle se může pohybovat 4 směry: dopředu `forward(pocet_kroku)`, dozadu `backward(pocet_kroku)`, doleva `left(pocet_stupnu)` a doprava `right(pocet_stupnu)`. Pomocí prvních dvou příkazů se turtle hýbe, proto je parametrem funkce počet kroků, pomocí dalších dvou příkazů můžeme turtle otáčet.

Vyzkoušejte si následující příkazy:

```python
t.right(90)
t.forward(100)
t.left(90)
t.backward(100)
```

Co se stane?

![turtle3](https://files.realpython.com/media/Update_-_Moving_Turtle_VIDEO_GIF.61623cf40fed.gif)

Pro tyto příkazy existují i zkrácené verze:

t.rt() = t.right()
t.fd() = t.forward()
t.lt() = t.left()
t.bk() = t.backward()

Čáru můžeme vykreslit také mezi 2 zadanými body, naší výchozí pozicí a druhým místem na obrazovce. To samozřejmě děláme pomocí souřadnic.

![turtle4](https://files.realpython.com/media/Turtle_EDIT_Graph.790c213ce0ba.jpg)

Obrazovka je rozdělena na 4 kvadranty. Na začátku programu je turtle vždy na pozici (0,0), které říkáme Home (domov). Abychom vykreslili čáru z tohoto místa, použijeme příkaz `.goto(pozice_x, pozice_y)`:

```python
t.goto(100,100)
```
Výsledek by měl vypadat takto:

![turtle5](https://files.realpython.com/media/TURTLE_EDIT_GOTO_GIF.ac9b7de34b40.gif)

Pokud chceme turtle vrátit zpátky na domovskou pozici, použijeme:
```python
t.home()
```

Je to stejné jako kdybychom použili `t.goto(0,0)`.

### Tvary
Nyní, když už známe pohyby, začneme vykreslovat tvary. Začneme polygony. Vyzkoušejte si tyto příkazy.

```python
t.fd(100)
t.rt(90)
t.fd(100)
t.rt(90)
t.fd(100)
t.rt(90)
t.fd(100)
```

Výsledek:

![turtle6](https://files.realpython.com/media/TURTLE_SQUARE_EDIT.626bc3fccd67.gif)

Vyzkoušejte si nakreslit obdélník.

#### Předvolené tvary

Jak vykreslit kružnici?
Pomocí bodů bychom jej vykreslovali velmi složitě.

```python
t.circle(60)
```

Výsledek:

![turtle7](https://files.realpython.com/media/Update_-_Turtle_Circle_GIF.14906fdf5060.gif)

Číslo v závorkách značí poloměr.

Jak nakreslit kruh?

```python
t.dot(20)
```

![turtle8](https://files.realpython.com/media/Turtle_Dot_Pic.8f171e2c7d98.png)

Pozor, zde však zadáváme PRŮMĚR.

### Změna barvy obrazovky

Standartně je obrazovka bílá, její barvu můžeme změnit pomocí:

```python
turtle.bgcolor("blue")
```

Vyzkoušejte si barvu změnit ("green", "red",...).

![turtle9](https://files.realpython.com/media/1-BG_COLOR-GIF.8619d9e1783f.gif)

Také můžete využít HEX kód (Color Picker na googlu).

### Změna názvu obrazovky

```python
turtle.title("My Turtle Program")
```

![turtle10](https://files.realpython.com/media/Change_in_Screen_Title_UPDATE.bf645f90e3d0.jpg)

### Změna velikosti turtle

Turtle můžeme zvětšovat i zmenšovat. To děláme pomocí příkazu `shapesize(delka, sirka, sirka_okraje)`. Vyzkoušejte si následující příkazy:

```python
t.shapesize(1,5,10)
t.shapesize(10,5,1)
t.shapesize(1,10,5)
t.shapesize(10,1,5)
```

Výsledek:

![turtle11](https://files.realpython.com/media/Turtle_Shape_Size_Updated_GIF.3f31c5f85340.gif)

### Změna velikosti pera
Předchozí příkazy měnily pouze tvar turtle. Pro změnu tloušťky pera, kterým turtle kreslí používáme `.pensize(velikost)`:

```python
t.pensize(5)
t.forward(100)
```

Výsledek:

![turtle12](https://files.realpython.com/media/Pen_Size_GIF.4d1fb1beefd6.gif)
