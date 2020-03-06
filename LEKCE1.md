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

Instalace Visual Studio Code - tutoriál s printscreeny
Čísla a řetězce (vytisknout základní přehled)

Čísla:
celá čísla, desetinná čísla
základní matematické operace
Řetězce:
rozdíl číslo vs. řetězec
skládání řetězců

Příklady:
