# LEKCE 1 (2. 4.) L + K
## Příkazová řádka
V této lekci se seznámíme s příkazovou řádkou – černým okýnkem, které programátoři používají na zadávání příkazů. 

Příkazová řádka (respektive program, kterému se říká i konzole či terminál; anglicky command line, console, terminal) se na různých systémech otevírá různě:

Windows (české): Start → napsat na klávesnici „cmd“ → Příkazový řádek
Windows (anglické): Start → napsat na klávesnici „cmd“ → Command Prompt

Po otevření konzole tě uvítá řádek, kterým počítač vybízí k zadání příkazu. Bude končit znakem >, před nímž můžou být ještě další informace:
### WINDOWS
``` > ```
Podle systému se potom liší i samotné příkazy, které budeš zadávat.

## První příkaz
Začneme jednoduchým příkazem. Napiš `whoami` (z angl. who am I? – kdo jsem?) a stiskni Enter. Objeví se přihlašovací jméno. 

Znak `$` nebo `>` je v ukázce jen proto, aby bylo jasné, že zadáváme příkaz do příkazové řádky. Vypíše ho počítač, většinou ještě s něčím před ním, takže ho nepiš! Zadej jen `whoami` a stiskni Enter.

## Aktuální adresář
Příkazová řádka pracuje vždy v nějakém adresáři (neboli složce, angl. directory, folder). Ve kterém adresáři zrovna je, to nám poví příkaz `cd` (z angl. current directory – aktuální adresář).

## Co v tom adresáři je?
Příkaz `dir` (z angl. directory – adresář) nám vypíše, co aktuální adresář obsahuje: všechny soubory, včetně podadresářů, které se v aktuálním adresáři nacházejí.

## Změna aktuálního adresáře
Aktuální adresář se dá změnit pomocí příkazu `cd` (z angl. change directory – změnit adresář). Za `cd` se píše jméno adresáře, kam chceme přejít. Pokud máš adresář Desktop nebo Plocha, přejdi tam. Pak nezapomeň ověřit, že jsi na správném místě.

## Vytvoření adresáře
Co takhle si vytvořit adresář na Python? To se dělá příkazem `mkdir` (z angl. make directory – vytvořit adresář). Za tento příkaz napiš jméno adresáře, který chceš vytvořit – v našem případě naucse-python:

```
mkdir naucse-python
```

Teď se můžeš podívat na Plochu nebo do nějakého grafickém programu na prohlížení adresářů: zjistíš, že adresář se opravdu vytvořil!

## Úkol
Zkus v nově vytvořeném adresáři naucse-python vytvořit adresář test a zkontrolovat, že se opravdu vytvořil.
Budou se hodit příkazy `cd`, `mkdir` a `ls` či `dir`.

## Úklid
Teď vytvořené adresáře zase smažeme.
Nemůžeš ale smazat adresář, ve kterém jsi. Proto se vrátíme na Desktop. Ale nemůžeme použít cd Desktop – v aktuálním adresáři žádný Desktop není. Potřebuješ se dostat do nadřazeného adresáře: toho, který obsahuje adresář ve kterém právě jsi. Nadřazený adresář se značí dvěma tečkami: 

```
cd ..
```
Teď můžeš smazat vytvořený adresář naucse-python. K tomu použij příkaz rm nebo rmdir (z remove – odstraň, resp. remove directory – odstraň adresář).

## Pozor!
Příkazová řádka nepoužívá odpadkový koš! Všechno se nadobro smaže. Takže si dobře překontroluj, že mažeš správný adresář.

Na Windows je potřeba zadat přepínač, který říká, že má smazat adresář a veškerý jeho obsah. Tentokrát je to /S (lomítko, S). Příkaz rmdir se automaticky ujistí, jestli to co mažeš opravdu chceš smazat.

```
> rmdir /S naucse-python 

```

## Shrnutí
Tady je tabulka základních příkazů, se kterými si zatím vystačíme:

| Příkaz       | Popis           | Příklad  |
| ------------- |:-------------:| -----:|
| cd      | změna adresáře | cd test |
| cd      | výpis aktuálního adresáře      |   cd |
| dir | výpis adresáře      |    dir |
| copy | zkopírování souboru     |    copy puvodni.txt kopie.txt |
| move | přesun/přejmenování souboru      |    move puvodni.txt novy.txt |
| mkdir | vytvoření adresáře     |    mkdir test |
| del | smazání souboru      |    rm ahoj.txt |
| exit | ukončení      |    exit |

Příkazů existuje samozřejmě daleko víc. Dokonce každý program, který máš na počítači nainstalovaný, jde spustit z příkazové řádky – a to většinou jen zadáním jeho jména. Zkus, jestli na tvém počítači bude fungovat `firefox`, `notepad`, `safari` nebo `gedit`.

Při učení Pythonu použiješ programy/příkazy jako `python`, které zanedlouho nainstalujeme.

## Instalace Visual Studio Code 
Na stránce https://code.visualstudio.com/download si stáhneme instalační soubor a nainstalujeme si Visual Studio Code. Jedná se o program, ve kterém budem psát kód pro programy a následně jej budeme spouštět.

## Instalace Pythonu
Běž na stahovací stránku Pythonu (https://www.python.org/downloads/) a stáhni si instalátor nejnovější stabilní verze Pythonu. Ověř si že je to verze 3.6.0 nebo novější – verze 3.6.0 má jistá vylepšení, která budeme v tomto kurzu používat.

Kde zjistíš, zda máš 32bitové nebo 64bitové Windows? Otevři nabídku Start, vyhledat „Systém“ a otevřít Systémové informace. Pokud máš novější počítač, téměř jistě budeš mít Windows 64bitové.

![instalace](https://naucse.python.cz/course/pyladies/beginners/install/static/windows_add_python_to_path.png)

Stažený instalátor spusť. Na začátku instalace zaškrtni Install launcher for all users a také Add Python to PATH. 

Pak zmáčkni Install now a dále se drž instrukcí.

Máš-li otevřenou příkazovou řádku, po instalaci Pythonu ji zavři a otevři novou. Instalace mění systémové nastavení, které se musí načíst znovu.

## Čísla a řetězce 

### Čísla
V Pythonu rozlišujeme a používáme dva typy čísel - celá čísla (2, -5, 9, 0,...) a čísla desetinná (0.59, 1.2, atd.). Pozor! U desetinných čísel se místo desetinné čárky píše tečka.
### Základní matematické operace
Protože při programování dost často narazíme na matematiku (ale není třeba se toho bát!), např. když budeme potřebovat spočítat, o kolik políček se nám mají hýbat postavy ve hře, nebo jaké má hráč skóre. Určitě tedy budeme potřebovat základní matematické operace, jako je sčítání, odečítání, násobení a dělení. Pro obtížnější výpočty (např. výpočet odmocnin) je pro python vytvořené speciální sada funkci math, o které si budeme povídat později.

Základní operace se píší, tak jak jste zvyklí:

sčítání: +
`>>> 5 + 5`

odčítání: -
`>>> 1 - 7`

násobení: *
`>>> 3 * 8`

dělení: /
`>>> 30/7`


Další operace jsou:

mocnění: **
`>>> 5**2`

celočíselné dělení: //
`>>> 30//7`

zbytek po dělení: %
`>>> 30%7`

### Řetězce
Zjednodušeně řečeno - řetězce používáme, když chceme naopak v programu používat něco s písmeny. Např. pokud si chceme uložit přezdívku hráčů nebo vypsat Game over. V pythonz poznáme řetězce podle toho, že jsou ohraničené úvozovkami. Nezáleží na tom, jestli používáte jednoduché nebo dvojité, každý programátor má radši jiné. 
`>>> "Code rebels"`

### Operace s řetězci
I pro řetězce máme v pythonu některé operace. Můžeme řetězce skládat dohromady, pomocí operátoru +. Řetězce můžeme také násobit, čímž způsobíme, že se jeden řetězec bude několikrát opakovat za sebou. Také můžeme zjištovat, jaké písmeno je první nebo poslední (což se nám může třeba hodit při ověřování hesel), avšak to se naučíme později v kurzu.

`>>> 'Code' + ' ' + 'Rebels'`

### Číslo vs. řetězec

Také číslo můžeme chtít někdy použít jako řetězec, v případě, že se třeba bude jednat o šifru a nechceme, aby nám s číslem někdo manipuloval. V tom případě dáme do závorek i číslo "789567". Můžete si vyzkoušet, že poté 
skládání řetězců.

### Příkaz print()

V dnešní lekci budeme používat pro výpis programu příkaz print(). Do kulatých závorek vždy vložíme, co chceme vytisknout. 

### Příklady

Vyzkoušejte si, jaký je rozdíl mezi dělením a celočíselným dělením.

Vypočítejte, kolik mi zbyde bonbónů, pokud jich mám 87 a spravedlivě je rozdělím mezi svých 9 kamarádů.

Vyzkoušejte si příkaz "87998" - 8. Jaký bude výsledek?

Vypište slovo "la" 180x za sebou.

Vypište slovo "la" 180x za sebou včetně mezer.







