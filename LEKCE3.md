# LEKCE 3 - FUNKCE

Opakování (20 min)

## Co je to funkce?

(Nejprve se pobavit o tom, kdo zná funkce z matematiky?)

Funkce je nějaký komplikovanější výpočet nebo malý program zabalený do jakési krabičky. Této krabičce dáme nějaké jméno, abychom jej mohli používat na různých místech v našem programu. Funkci si můžeme představit jako topinkovač. Topinkovač pro nás dělá nějakou užitečnou činnost (opéká topinky), která by byla otravná a zdlouhavá, kdybychom ji chtěli dělat sami, například smažit topinky na oleji na pánvičce. Každá funkce má svoje jméno a obvykle má nějaký vstup (čerstvý chleba) a výstup (opečená topinka). Funkci spustíme tak, že ji takzvaně zavoláme.

Programátoři funkce používají, aby si psaní kódu zjednodušili. Často se nám může stát, že v nějakém programu opakujeme nějakou akci vícekrát (např. aktualizujeme skóre, provádíme tah některého z hráčů ve hře, atd.) a bylo by asi celkem otravné kód stále opisovat. Navíc, stejně jako u proměnných, se může třeba část výpočtu změnit (budeme chtít pro skóre nebo tah přidat speciální podmínky) a pokud bychom museli takovou okolnost měnit v celém kódu, bylo by to časově náročnější a rozhodně náchylnější k chybám.

V pythonu existuje spousta již implementovaných (naprogramovaných) funkcí, které si dnes ukážeme, zároveň si můžete psát (definovat) funkce vlastní.

## Moduly

Abychom se v tom všem vyznali, třídíme funkce do takzvaných modulů. Moduly jsou tedy sady funkcí. Např. pro matematické výpočty existuje knihovna `math`. 

### Známe funkce a moduly

Dalším užitečným modulem je modul `random`, který obsahuje funkce pro generování náhodných čísel. Jedna z takových funkcí se jmenuje `randint()`. Umí generovat náhodná celá čísla v zadaném rozmezí. Můžeme tak například simulovat házení kostkou.

Pro práci s řetězci se nám bude velmi hodit funkce `len()`, která vrací délku zadaného řetězce.

Pokud chceme funkce z takovýchto sad (modulů) využívat, musíme vždy na začátek kódu moduly naimportovat. Jednoduše zadáme `import <název modulu>`. Pro random tedy `import random`.

## Dokumentace 

Každý programovací jazyk má svou vlastní dokumentaci, která je vlastně něco jako slovník, když se učíte cizí jazyk. Stejně jako u cizích jazyků, jakmile dobře ovládáte gramatiku, najít si slovíčko, které vám vypadlo z paměti už je jen detail. V dokumentaci tedy hledáme, jak přesně se potřebná fuknce nebo modul jmenuje a jak ji používat (jaké jsou vstupní a výstupní parametry). Samozřejmě nám však příliš nenapoví, v jakých programech je dobré ji využít, to si musí programátor rozmyslet sám.

Dokumentaci pro Python naleznete na https://docs.python.org/.

Stejně dobře samozřejmě můžete využít google, pokud si nemůžete vzpomenout, jakou funkci používat pro absolutní hodnotu, odmocninu nebo generování náhodných čísel. Většina dokumentací a informací je ale v angličtině. Nicméně můžete využít Google překladač. 

## Psaní vlastních funkcí



## Úkoly

Nalezněte v dokumentaci stránku pro moduly math a random.

Převeďte díky zabudované fuknci 60°, 75° a 90° na radiány.

Pomocí funkce randint() simulujte hod šestistěnnou kostkou.

Uložte výsledek funkce randint() do proměnné hod_kostkou.

Vytvořte program, který vypíše "sude cislo", pokud při hodu naší kostkou padne sudé číslo, "liche cislo", pokud padne liché číslo.

Vytvořte program, který načte jméno a vypíše jeho délku.

Vytvořte program, který načte od uživatele heslo a rozhodne, zda je heslo validní (a uživatel ho může použít). Heslo se nesmí skládat pouze z písmen. Bude se vám hodit funkce `isalpha()`.

Vytvořte program, který načte telefonní číslo a rozhodne, zda se opravdu jedná o telefonní číslo (musí obsahovat 9 čísel). Bude se vám hodit funkce `isdecimal()`.
