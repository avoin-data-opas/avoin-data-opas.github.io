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
- [Yritän tallentaa muuttujaan asioita, mutta print(nimi) kertookin None?](#4)
- [Datani ei suostu lataamaan?](#5)
- [Lataamassani datassa on jotain omituisia 'NaN'-arvoja?](#6)
- [Yhdistin palasia datasta, mutta nyt en enää pysty tekemään asioita uudella muuttujallani?](#7) 
- [Koodini ei toimi, vaikka se on ihan varmasti oikein kirjoitettu?](#8)
- [Datan päivämäärät sekoittavat toiminnan, miten korjaan?](#9)
- [Kopioin datan uuteen muuttujaan, jonka käsittelyn jälkeen huomaan alkuperäisen muuttujan arvojen vaihtuneen?](#10)


<h3 id="1">Buhuu, jag kan inte!?</h3>

Ingen panik, ingen är född mästare. Man lär sig genom att försöka och misslyckanden hör till processen.
En fördel med Python är den stora användarskaran: Vad du än kan tänka dig behöva veta är du knappast den första, och oftast hittar du svar på dina frågor genom en snabb googling. Forumet [StackExchange](https://stackexchange.com/) har troligen svaren på dina problem. I den här listan hittar du också svar på några vanliga frågor.



<h3 id="2">Jag försökte köra en cell, men den blir inte klar och ritar inte ut min figur.</h3>

Om cellen inte ska köra några komplicerade operationer så borde det inte ta mer än ett par sekunder att köra den. I såna fall kanske koden innehåller en loop som inte avslutas. Du kan stoppa kerneln och försöka köra koden igen med små ändringar. Om du inte hittar problemet, testa med en enklare syntax tills du är säker på att funktionerna i koden fungerar som du förväntar dig.

<h3 id="3"> Felmeddelandet säger att "variabel is not defined" eller "variabel does not exist"</h3>

Variabeln som koden refererar till har inte blivit definierad. Är du säker på att du har kört den cell som ska definiera variabeln?
Kontrollera också att variabeln är korrekt skriven. Python gör skillnad på stora och små bokstäver.

<h3 id="4">Yritän tallentaa muuttujaan asioita, mutta print(nimi) kertookin None?</h3>

Tallennuksessasi on jokin ongelma. Muista aina tallentaa tekemäsi operaatiot muuttujaan, eli esimerkiksi
```python
muuttuja = ... lataus datasta
muuttuja = muuttuja*2
```
eikä
```python
muuttuja = ... lataus datasta
muuttuja*2
```
Jos muuttujan tarkasteleminen palauttaa None, tällöin muuttujasi on tyhjä.
Tarkasta, että haluamasi operaatio oikeasti on tehtävissä oleva eikä hajoa vaikkapa jonkin sisäfunktion vääriin syötteisiin.

<h3 id="5">Datani ei suostu lataamaan?</h3>
Tavallisia csv- ja vastaavia tekstitiedostoja voi tarkastella tekstinkäsittelyohjelmilla. Tällöin näet, millä merkillä arvot on eroteltu, miltä riviltä
relevantti data alkaa tai onko tiedoston sisältö ylipäätään se mitä kuvittelit.

Jakomerkit, otsikkorivit ja vastaavat voit määrittää lukufunktion parametreina, esimerkiksi
```python
pd.read_csv('linkki tiedostoon', sep = ';')
```
avaisi puolipisteellä erotetun csv:n.

**pd.read_table()** voi auttaa selvittämään datan luonnetta jos ei jaksa avata tekstieditoria.

Joskus ongelma johtuu merkistöjä ohjaavien koodien yhteensopimattomuudesta. Tällöin parametri **encoding** voi auttaa.
Näistä löydät enemmän [täältä](https://docs.python.org/3/library/codecs.html#standard-encodings). Jos oletusasetus ei toimi, usein jokin ISO-variantti kelpaa.

<h3 id="6">Lataamassani datassa on jotain omituisia 'NaN'-arvoja?</h3> 

NaN, 'Not a Number', kertoo että tässä kohtaa dataa ei ole ymmärrettävää arvoa. Joko arvo on omituinen (kuten negatiivisen luvun neliöjuuri) tai sitä ei vain ole.

Monet funktiot eivät välitä NaN-arvoista tai niiden parametreihin voi laittaa asetuksen, jolla ne eivät huomioi niiden olemassaoloa.
Tämä helpottaa etenkin isojen datojen läpikäyntiä, kun kaikkia mahdollisia virheitä ei huomioida eikä kone jumitu törmätessään matemaattiseen mahdottomuuteen.

<h3 id="7">Yhdistin palasia datasta, mutta nyt en enää pysty tekemään asioita uudella muuttujallani?</h3>

Yhdistitkö eri tyyppisiä muuttujia? Kokonaisluvut (integer) ovat tietokoneelle erilaisia kuin desimaaleja ymmärtävät liukuluvut (float),
jotka ovat erilaisia kuin teksti (string) ja niin edelleen.
Joskus numerosarjakin voi olla kirjoitettu johonkin dataan stringinä, mikä on kovasti epämukavaa huomata jälkikäteen.
Pythonissa on erilaisia vertailukomentoja, kuten isstring, joilla voi tarkistaa muuttujien tyypin.

Yhdistithän palaset oikeisiin suuntiin? Jos halusit sarakkeet vierekkäin, niitä ei kannata vahingossa liittää peräkkäin yhdeksi pitkäksi sarakkeeksi.
Tiedoston tarkastelu vaikkapa **len(nimi)** ja **nimi.head()** komennoilla on usein hyödyllistä näissä tilanteissa.


<h3 id="8">Koodini ei toimi, vaikka se on ihan varmasti oikein kirjoitettu?</h3>

Tarkista nyt kuitenkin, ettei ole piste väärässä kohdassa tai väärä kirjainkoko jossakin.
Jos koodi ei ihan oikeasti vaan toimi vaikka pitäisi, syy voi löytyä kerneliin jääneistä aiemmista tiedoista muistissa.
Näissä tapauksissa voi välillä vain kokeilla Kernel-valikosta Restart & Clear Outputtia ja uudelleen ajamista vaikka parikin kertaa.

<h3 id="9">Datan päivämäärät sekoittavat toiminnan, miten korjaan?</h3>

Päivämäärät saattavat tulla ilmoitettuina monessa muodossa. Jos oletusasetukset eivät saa dataa toimimaan nätisti, **pd.read_csv():n** [dokumentaatiosta](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.read_csv.html) näkyy millä sen parametreilla voi vaikuttaa päivämäärien tulkintaan. Esim. **dayfirst** tai **date_parser** saattavat ratkaista ongelman.
Pythonissa on myös paketti [**time**](https://docs.python.org/3/library/time.html), josta löytyy varmasti sopivat palat tilanteeseen.

<h3 id="10">Kopioin datan uuteen muuttujaan, jonka käsittelyn jälkeen huomaan alkuperäisen muuttujan arvojen vaihtuneen?</h3>

Python operoi osoittimilla, joissa muuttujaan tallentuu oikeastaan tiedon itsensä sijaan paikkatieto siitä, mistä päin muistia kyseinen tieto löytyy.
Kopioitaessa kokonaista datamuuttujaa toiseen muuttujaan yksittäisten rivien tai sarakkeiden sijaan saattaa käydä niin, että siinä ei oikeastaan tehdä muuta kuin
viitataan vanhaan tietoon. Jos uudelle muuttujalle tehdään muutoksia, tällöin osoittimet vievät muutokset myös vanhaan dataan ja puf, sekin on muuttunut.
Tätä sattuu joskus ja se on hitusen rasittavaa. Olemme huomanneet hyväksi kopioida alkuperäisen:

```python
uusiNimi = vanhaNimi.copy()
```
jolloin oikeasti tehdään uutta tietoa muistiin niin, ettei viittaus vahingossakaan tapahdu alkuperäiseen muuttujaan.
Kiinnostavaa kyllä tätä ongelmaa ei tunnu esiintyvän muussa kuin koko datan kerralla siirtämisen yhteydessä, eli yksittäisten rivien erottelu uusiin muuttujiin tapahtuu
ilman mitään viittausta alkuperäistietoihin.


