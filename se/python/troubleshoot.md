---
title: Problem?
lang: se
ref: troubleshoot
category: python
---

## Problem?

Innehåll:

- [Buhuu, jag kan inte!](#1)
- [Jag försökte köra en cell, men den blir inte klar och ritar inte ut min figur.](#2)
- [Felmeddelandet säger att "variabel is not defined" eller "variabel does not exist"](#3)  
- [Jag försöker ändra en variabel, men print(variabel) ger resultatet "None"](#4)
- [Min Datafil vill inte ladda in](#5)
- [I datan jag laddat in finns NaN-värden.](#6)
- [Jag slog ihop flera delar av min data till samma variabel, men nu fungerar inte min nya variabel.](#7) 
- [Min kod fungerar inte, fastän den alldeles säkert är rätt skriven.](#8)
- [Datan innehåller datum, som krånglar till formatet. Hur fixa?](#9)
- [Jag kopierade data till en ny variabel, men efter det har originalvariabeln ändrats.](#10)


<h3 id="1">Buhuu, jag kan inte!?</h3>

Ingen panik, ingen är född mästare. Man lär sig genom att försöka och misslyckanden hör till processen.
En fördel med Python är den stora användarskaran: Vad du än kan tänka dig behöva veta är du knappast den första, och oftast hittar du svar på dina frågor genom en snabb googling. Forumet [StackExchange](https://stackexchange.com/) har troligen svaren på dina problem. I den här listan hittar du också svar på några vanliga frågor.



<h3 id="2">Jag försökte köra en cell, men den blir inte klar och ritar inte ut min figur.</h3>

Om cellen inte ska köra några komplicerade operationer så borde det inte ta mer än ett par sekunder att köra den. I såna fall kanske koden innehåller en loop som inte avslutas. Du kan stoppa kerneln och försöka köra koden igen med små ändringar. Om du inte hittar problemet, testa med en enklare syntax tills du är säker på att funktionerna i koden fungerar som du förväntar dig.

<h3 id="3"> Felmeddelandet säger att "variabel is not defined" eller "variabel does not exist"</h3>

Variabeln som koden refererar till har inte blivit definierad. Är du säker på att du har kört den cell som ska definiera variabeln?
Kontrollera också att variabeln är korrekt skriven. Python gör skillnad på stora och små bokstäver.

<h3 id="4">Jag försöker ändra en variabel, men print(variabel) ger resultatet "None" eller ett annat oväntat resultat</h3>

Det är troligen något fel med hur du sparar informationen. Kom ihåg att alltid definiera variabeln när du ändrar den. Exempel:

```python
variabel = 3
variabel = variabel*2
print(variabel)
```
Denna kod skriver ut värdet på *variabel*, som är 6.

Felexempel:
```python
variabel = 3
variabel*2
print(variabel)
```
Denna kod skriver ut värdet 3, eftersom man inte har definierat om *variabel*.


<h3 id="5">Min Datafil vill inte ladda in</h3>
Vanliga csv- eller motsvarande textfiler kan öppnas och undersökas med hjälp av ett vanligt textbehandlingsprogram. Du kan kontrollera vilka tecken som separerar värdena, på vilka rader den relevanta datan hittas eller om filen över huvud taget innehåller det du väntat dig. 

Separationstecken, titelrader och annat kan bestämmas med hjälp av inläsningsfunktionens parametrar.


```python
pd.read_csv('länk till filen', sep = ';')
```
Den här koden läser in en csv-fil där värdena separeras med semikolon.


**pd.read_table()** kan hjälpa dig undersöka Datans format om du inte vill öppna den i ett annat program.

Ibland beror problemet på att fien innehåller tecken som inte kan tolkas med grundinställningarna. Då kan parametern **encoding** vara till hjälp. Du hittar mer info om parametern och olika teckenpaket [här](https://docs.python.org/3/library/codecs.html#standard-encodings). Om inte grundinställningen duger, fungerar oftast någon ISO-variant.


<h3 id="6">I datan jag laddat in finns NaN-värden.</h3> 

NaN, 'Not a Number', innebär att den här datan har ett värde som inte kan tolkas. Det kan innebära att värdet är odefinierat (t.ex. kvadratroten av ett negativt tal) eller att värdet bara saknas. 

Många funktioner ignorerar NaN-värden (eller så kan parametrarna ändras så att de ignorerar dem). Det här är praktiskt när man går igenom stora datafiler. Annars kan alla möjliga småfel göra att koden hakar upp sig.



<h3 id="7">Jag slog ihop flera delar av min data till samma variabel, men nu fungerar inte min nya variabel.</h3>

Kombinerade du olika typer av variabler? Programmet gör skillnad på heltalsvariabler, *integer*, decimaltal, *float*, och text, *string*.
Ibland kan en sifferserie bland datan vara definierad som en *string*, och det kan ställa till med problem när man ska göra beräkningar. Python har en del kontrollkommandon med hjälp av vilka man kan kontrollera variabelns format:

```python
# Vi kontrollerar om variabeln test_string är string med hjälp av type() 
  
# Vi skapar variabeln    
test_string = "404"

# Vi kontrollerar om variabeln är av typen string. Variabeln "kontroll" får värdet true eller false
kontroll=type(test_string) == str
  
# Vi skriver ut resultatet 
print("Variabeln är ", test_string, ". Är variabeln en string?")
print(kontroll)
```
Koden skriver ut:

Variabeln är  404 . Är variabeln en string?
True

Eller har du satt ihop flera sifferserier och vill ha dem som kolumner, men fick istället alla serier i en lång rad? Du kan kontrollera om så är fallet med hjälp av kommandona **len(variabel)** och **nimi.head()**

```python
# Vi skapar två listor
test1 = (1, 2, 3, 4)
test2 = (5, 6, 7, 8)

# Vi slår ihop båda listorna till en och räknar elementen
combo = test1 + test2
print(combo)
print("Variabeln är", len(combo),"celler lång")

# Vi slår ihop listorna som två kolumner och räknar elementen
combo = [test1, test2]
print(combo)
print("Variabeln är", len(combo),"celler lång")
```
(1, 2, 3, 4, 5, 6, 7, 8)
Variabeln är 8 celler lång
(1, 2, 3, 4), (5, 6, 7, 8)
Variabeln är 2 celler lång


<h3 id="8">Min kod fungerar inte, fastän den alldeles säkert är rätt skriven.</h3>

Kontollera en extra gång att du inte saknar något kommatecken eller har fel case på bokstäverna.
Om koden faktiskt är felfri och ändå inte fungerar så kan felet bero på att *kernel*n har sparat någon information som stör. I Kernel-menyn kan du då välja **Restart & Clear Output** och köra alla kodceller igen.


<h3 id="9">Datan innehåller datum, som krånglar till formatet. Hur fixa?</h3>

Datum kommer i många former, och kan ställa till det. Om originalinställningarna inte kan tolka det prydligt, så kan du hitta tips i [dokumentationen](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.read_csv.html) för **pd.read_csv()**. Exempelvis **dayfirst** eller **date_parser** kan vara till hjälp. I Python finns också paketet [**time**](https://docs.python.org/3/library/time.html), där man kan hitta rätt verktyg.


<h3 id="10">Jag kopierade data till en ny variabel, men efter det har originalvariabeln ändrats.</h3>

Variabler i python använder hänvisningar. Det innebär att variabeln egentligen bara sparar information om var dess värde hittas, inte själva värdet. Om du har kopierat en variabel till en annan (ex. *kopiaavinfo = info*) kan det ibland hända att den bara hänvisar till den andra variabeln. När du sedan ändrar den nya variabeln kan båda ändras. Ett bra sätt att komma undan detta när man kopierar en variabel är:

```python
kopiaavinfo = info.copy()
```
Då kommer inte den nya variabeln att i misstag hänvisa till den gamla.
Det här problemet brukar märkligt nog bara uppkomma när man kopierar hela datasets. Om man bara kopierar enskilda kolumner fungerar det som det ska.


