# LEKCE 5 - TURTLE, SEZNAMY
Opakování (20 min)

Turtle + seznamy (70 min, půl napůl, začít seznamy)

Dnes se naučíme:
Co je to python knihovna TURTLE
Jak jí používat v Pythonu
Co pomocí Turtle můžeme programovat
Co jsou to seznamy a jaké mají využití
Na závěr si naprogramujeme krátkou hru 

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

### Změna barvy turtle a pera

Na začátku je vždy barva turtle i pera černá. My můžeme měnit dvě věci:
1) barvu turtle -> to změní barvu výplně
2) barvu pera -> to změní barvu linek (čar)

Abychom změnu dobře viděli, nejprve si turtle zvětšíme:

```python
t.shapesize(3,3,3)
```

Nyní změníme barvu turtle (výplně):
```python
t.fillcolor("red")
```

Turtle by nyní měla vypadat takto:

![turtle13](https://files.realpython.com/media/Turtle_Fill_Color_Red_Update.216d34fcf201.png)

Pro změnu pera:

```python
t.pencolor("green")
```

![turtle14](https://files.realpython.com/media/Turtle_Pen_Color_Updated.362202ac18cb.png)

Abychom změnili barvu obojího zároveň, používáme příkaz (funkci) `.color(barva_pera, barva_turtle)`.

```python
t.color("green", "red")
``` 

![turtle15](https://files.realpython.com/media/Turtle_Color_One_Line_Green_and_Red_Updated.060568e73634.png)

### Vyplňování obrazců

Vyplňování určitého obrazce musíme zahájit `.begin_fill()` a ukončit `.end_fill()`.

```python
t.begin_fill()
t.fd(100)
t.lt(120)
t.fd(100)
t.lt(120)
t.fd(100)
t.end_fill()
```

Výsledek:

![turtle16](https://files.realpython.com/media/Turtle_Begin_End_Fill_GIF.849f73374a22.gif)

### Změna tvaru turtle

```python
t.shape("turtle")
t.shape("arrow")
t.shape("circle")
```

Vyzkoušejte si i následující možnosti:
Square
Arrow
Circle
Turtle
Triangle
Classic

Další tvary můžete najít v dokumentaci.

### Rychlost
Obecně se turtle hýbe střední rychlostí. Tu můžeme zvýšit nebo snížit, aby se pohybovala rychleji nebo pomaleji. Nastavujeme pomocí `.speed(rychlost)` rychlost může výt od 1 do 10. Vyzkoušíme si:

```python
t.speed(1)
t.forward(100)
t.speed(10)
t.forward(100)
```


Pokuste se nastavit turtle následovně a vykreslete vyplněný kruh o poloměru 90:

Barva pera: fialová (purple)
Varva výplně: oranžová (orange)
Velikost pera: 10
Rychlost: 9

```python
t.pencolor("purple")
t.fillcolor("orange")
t.pensize(10)
t.speed(9)
t.begin_fill()
t.circle(90)
t.end_fill()
```

Pokud bychom měli více turtle, bylo by celkem zdlouhavé takto vše vypisovat, můžeme použít také jiný způsob:

```python
t.pen(pencolor="purple", fillcolor="orange", pensize=10, speed=9)
t.begin_fill()
t.circle(90)
t.end_fill()
```

![turtle17](https://files.realpython.com/media/TURTLE_EDIT_SINGLE_LINE_CUSTOMISATION_GIF.c30c0839af72.gif)

### Zvednutí pera
Občas chceme přemístit turtle na obrazovce bez toho, aby vykreslovala čáry. Pomyslně tedy potřebujeme pero zvednout `.penup()` a poté zase přiložit `.pendown()`.

```python
t.fd(100)
t.rt(90)
t.penup()
t.fd(100)
t.rt(90)
t.pendown()
t.fd(100)
t.rt(90)
t.penup()
t.fd(100)
t.pendown()
```

Výsledek:

![turtle18](https://files.realpython.com/media/Screenshot_2019-10-01_at_9.22.37_PM.20eeea07c674.png)


### Vyčištění obrazovky

Vyzkoušíme si:

```python
t.clear()
t.reset()
```

### Klonování

Občas chceme mít na obrazovce více turtle. To využijeme například v naší hře na konci dnešní lekce. Nyní si ukážeme, jak toho docílit pomocí klonování:

```python
c = t.clone()
t.color("magenta")
c.color("red")
t.circle(100)
c.circle(60)
```

Výsledek: 

![turtle21](https://files.realpython.com/media/TURTLE_EDIT_CLONE_GIF.1736204d0292.gif)

Paráda! Vše potřebné již máme za sebou!





### for
Do you remember the program that you used to create a square? You had to repeat the same line of code four times, like this:

>>> t.fd(100)
>>> t.rt(90)
>>> t.fd(100)
>>> t.rt(90)
>>> t.fd(100)
>>> t.rt(90)
>>> t.fd(100)
>>> t.rt(90)
A much shorter way to do this is with the help of a for loop. Try running this code:

>>> for i in range(4):
...     t.fd(100)
...     t.rt(90)
Here, the i is like a counter that starts from zero and keeps increasing by 1. When you say in range(4), you’re telling the program that the value of this i should be less than 4. It will terminate the program before i reaches 4.

Here’s a breakdown of how the program works:

At i = 0, the turtle moves forward by 100 units and then turns 90 degrees to the right.
At i = 0 + 1 = 1, the turtle moves forward by 100 units and then turns 90 degrees to the right.
At i = 1 + 1 = 2, the turtle moves forward by 100 units and then turns 90 degrees to the right.
At i = 2 + 1 = 3, the turtle moves forward by 100 units and then turns 90 degrees to the right.
The turtle will then exit the loop. To check the value of i, type i and then press the Enter key. You’ll get the value of i equal to 3:

### while
The while loop is used to perform a certain task while a condition is still satisfied. If the condition is no longer satisfied, then your code will terminate the process. You can use a while loop to create a series of circles by typing in this code:

>>> n=10
>>> while n <= 40:
...     t.circle(n)
...     n = n+10
When you run this code, you’ll see the circles appearing one after the other, and each new circle will be larger than the previous one.

Conditional Statements
You use conditional statements to check if a given condition is true. If it is, then the corresponding command is executed. Try typing in this program:

>>> u = input("Would you like me to draw a shape? Type yes or no: ")
>>> if u == "yes":
...     t.circle(50)
input() is used to obtain input from the user. Here, it will store the user’s response under the variable u. Next, it will compare the value of u with the condition provided and check whether the value of u is "yes". If it’s "yes", then your program draws a circle. If the user types in anything else, then the program won’t do anything.

When you add an else clause to an if statement, you can specify two results based on whether the condition is true or false. Let’s see this in a program:

>>> u = input("Would you like me to draw a shape? Type yes or no: ")
>>> if u == "yes":
...     t.circle(50)
>>> else:
...     print("Okay")
Here, you tell the program to display a particular output even when the user does not say "yes". You use print() to display some pre-defined characters on the screen.

Note that the user doesn’t need to type "no". They can type anything else, in which case, the result will always be "Okay", because you’re not explicitly telling the program that the user needs to type "no". Not to worry, however, as that can be fixed. You can add an elif clause to provide the program with several conditions and their respective outputs, as you can observe here:

> u = input("Would you like me to draw a shape? Type yes or no: ")
>>> if u == "yes":
...     t.circle(50)
>>> elif u == "no":
...     print("Okay")
>>> else:
...     print("Invalid Reply")
As you can see, this program now has more than one outcome, depending on the input it receives. Here’s how this code works:

If you type in "yes", then the code processes the input and draws a circle, as per your instructions.
If you type in "no", then the code prints out "Okay" and your program is terminated.
If you type in anything else, like "Hello" or "Sandwich", then the code prints "Invalid Reply" and your program is terminated.
Note that this program is case-sensitive, so when you’re trying it out, be sure to put the strings in upper-case or lower-case accordingly.


## Turtle závod

Cíl hry: Hráč, jehož turtle je dříve v domečku vyhrává.

Jak hrát: Každý hráč "háže kostkou". Poté se o hozené číslo turtle posune. Hráči se střídají, dokud jeden z nich nezvítězí.

Pravidla:
Každý hráč má jednu turtle s konkrétní barvou. Můžete mít i více hráčů, ale dnes si vyzkoušíme verzi pro dva.
Každá turtle má domeček, do kterého musí dorazit.
Každý hráč používá hod kostkou k určení náhodné hodnoty pro dané kolo. V naší hře to bude seznam s čísly od 1 do 6.




### Krok 1 - Importování knihoven

Musíme si naimportovat knihovny `turtle` a `random`
```python
import turtle
import random
```

### Krok 2 - Nastavení turtle a domečků

Nyní si vytvoříme dvě turtle pro dva hráče. Každá bude mít jinou barvu. 

```python
player_one = turtle.Turtle()
player_one.color("green")
player_one.shape("turtle")
player_one.penup()
player_one.goto(-200,100)
player_two = player_one.clone()
player_two.color("blue")
player_two.penup()
player_two.goto(-200,-100)
```

Nyní vytvoříme cílové domečky - kružnice.

```python
player_one.goto(300,60)
player_one.pendown()
player_one.circle(40)
player_one.penup()
player_one.goto(-200,100)
player_two.goto(300,-140)
player_two.pendown()
player_two.circle(40)
player_two.penup()
player_two.goto(-200,-100)
```

![turtle22](https://files.realpython.com/media/UPDATE_Turtle_Race_Setup_Blue_and_Green.16e6da3cc20d.png)

Dobrá práce! Nyní si vytvoříme kostku.

### Kostka

Kostka bude fungovat jako seznam s čísly od 1 do 6, z kterého budeme náhodně vybírat jedno konkrétní číslo.
`die = [1,2,3,4,5,6]`

### Zbytek hry
Budeme využívat smyčky a podmínky, takže musíme dávat pozor na odsazení kódu! Kroky jsou následující:

Krok 1: Začneme tím, že náš program zkontroluje, zda nějaká z turtle není v domečku.
Krok 2: Pokud není, hráči mohou pokračovat ve hře.
Krok 3: V každé smyčce musíme házet kostkou - program vybere ze seznamu náhodně číslo.
Krok 4: Poté se musí turtle o daný počet kroků pohnout dopředu.

Program toto opakuje a zastaví se, pokud jeden z hráčů vyhraje.

```python
for i in range(20):
    if player_one.pos() >= (300,100):
            print("Player One Wins!")
            break
    elif player_two.pos() >= (300,-100):
            print("Player Two Wins!")
            break
    else:
            player_one_turn = input("Press 'Enter' to roll the die ")
            die_outcome = random.choice(die)
            print("The result of the die roll is: ")
            print(die_outcome)
            print("The number of steps will be: ")
            print(20*die_outcome)
            player_one.fd(20*die_outcome)
            player_two_turn = input("Press 'Enter' to roll the die ")
            d = random.choice(die)
            print("The result of the die roll is: ")
            print(die_outcome)
            print("The number of steps will be: ")
            print(20*die_outcome)
            player_two.fd(20*die_outcome)
```

Nakonec by naše hra měla vypadat nějak takto:

![turtle_final](https://files.realpython.com/media/Update_-_Turtle_Race_Green_and_Blue.b1ee6be37a9f.gif)







