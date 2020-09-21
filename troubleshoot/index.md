## Ongelmia?

Kooste:

- Yhyy, en osaa?  
- Solu jäi jumiin eikä piirrä kuvaajaani tai aja koodiani?  
- Virheilmoitus herjaa 'nimi is not defined' tai 'nimi does not exist'?  
- Yritän tallentaa muuttujaan asioita, mutta print(nimi) kertookin None?  
- Datani ei suostu lataamaan?  
- Lataamassani datassa on jotain omituisia 'NaN'-arvoja?  
- Yhdistin palasia datasta, mutta nyt en enää pysty tekemään asioita uudella muuttujallani?  
- Koodini ei toimi, vaikka se on ihan varmasti oikein kirjoitettu?  
- Datan päivämäärät sekoittavat toiminnan, miten korjaan?  
- Kopioin datan uuteen muuttujaan, jonka käsittelyn jälkeen huomaan alkuperäisen muuttujan arvojen vaihtuneen?  


### Yhyy, en osaa?

Nou hätä, kukaan ei aloita mestarina. Tekemällä oppii ja virheet kuuluvat asiaan.
Pythonissa on kivana puolena sen laaja käyttäjäkunta: mitä ikinä keksitkään kysyä, et ole ensimmäinen ja vastaus luultavasti löytyy ensimmäisten googlaustulosten joukosta (esim. StackExchange on hyvä paikka vastausten löytämiseen).
Tässä on ohjeita muutamiin yleisimpiin ongelmatilanteisiin.

### Solu jäi jumiin eikä piirrä kuvaajaani tai aja koodiani?

Jos solun ajamisessa kuluu joitain sekunteja pidempään ilman, että sen pitäisi tehdä mitään erityisen raskasta, on mahdollista että koodissa on virheellisesti kirjoitettu
jokin silmukka johon koneen lukija jää jumiin. Pysäytä kernelin toiminta ja tarkista koodisi mahdollisten kitkakohtien varalta.
Jos et löydä ongelmaa, yksinkertaista syntaksia kunnes olet varma, että palaset etenevät loogisesti haluttuun suuntaan.

Yksi yleinen ongelma on, että syntaksivirhe ajaa koneen tekemään jotain väärää. Esimerkkitapaus: piirrät histogrammia yhdestä isomman datan sarakkeesta,
mutta unohdat sarakkeen nimen koodista. Tällöin kone yrittää toteuttaa käskyäsi ja hämmentyy saamastaan koko datan sisältävästä taulukosta.
Pysäytä kernelin toiminta ja korjaa muuttujien nimet oikein.

### Virheilmoitus herjaa 'nimi is not defined' tai 'nimi does not exist'? 

Muuttujaa, johon viittaat, ei ole olemassa. Olethan muistanut varmasti ajaa tässä istunnossa sen solun, jossa kyseinen muuttuja määritellään?
Muista myös kirjainkoon tarkka merkitys.

### Yritän tallentaa muuttujaan asioita, mutta print(nimi) kertookin None?

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

### Datani ei suostu lataamaan? 
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

### Lataamassani datassa on jotain omituisia 'NaN'-arvoja?  

NaN, 'Not a Number', kertoo että tässä kohtaa dataa ei ole ymmärrettävää arvoa. Joko arvo on omituinen (kuten negatiivisen luvun neliöjuuri) tai sitä ei vain ole.

Monet funktiot eivät välitä NaN-arvoista tai niiden parametreihin voi laittaa asetuksen, jolla ne eivät huomioi niiden olemassaoloa.
Tämä helpottaa etenkin isojen datojen läpikäyntiä, kun kaikkia mahdollisia virheitä ei huomioida eikä kone jumitu törmätessään matemaattiseen mahdottomuuteen.

### Yhdistin palasia datasta, mutta nyt en enää pysty tekemään asioita uudella muuttujallani?

Yhdistitkö eri tyyppisiä muuttujia? Kokonaisluvut (integer) ovat tietokoneelle erilaisia kuin desimaaleja ymmärtävät liukuluvut (float),
jotka ovat erilaisia kuin teksti (string) ja niin edelleen.
Joskus numerosarjakin voi olla kirjoitettu johonkin dataan stringinä, mikä on kovasti epämukavaa huomata jälkikäteen.
Pythonissa on erilaisia vertailukomentoja, kuten isstring, joilla voi tarkistaa muuttujien tyypin.

Yhdistithän palaset oikeisiin suuntiin? Jos halusit sarakkeet vierekkäin, niitä ei kannata vahingossa liittää peräkkäin yhdeksi pitkäksi sarakkeeksi.
Tiedoston tarkastelu vaikkapa **len(nimi)** ja **nimi.head()** komennoilla on usein hyödyllistä näissä tilanteissa.


### Koodini ei toimi, vaikka se on ihan varmasti oikein kirjoitettu? 

Tarkista nyt kuitenkin, ettei ole piste väärässä kohdassa tai väärä kirjainkoko jossakin.
Jos koodi ei ihan oikeasti vaan toimi vaikka pitäisi, syy voi löytyä kerneliin jääneistä aiemmista tiedoista muistissa.
Näissä tapauksissa voi välillä vain kokeilla Kernel-valikosta Restart & Clear Outputtia ja uudelleen ajamista vaikka parikin kertaa.

### Datan päivämäärät sekoittavat toiminnan, miten korjaan?  

Päivämäärät saattavat tulla ilmoitettuina monessa muodossa. Jos oletusasetukset eivät saa dataa toimimaan nätisti, **pd.read_csv():n** [dokumentaatiosta](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.read_csv.html) näkyy millä sen parametreilla voi vaikuttaa päivämäärien tulkintaan. Esim. **dayfirst** tai **date_parser** saattavat ratkaista ongelman.
Pythonissa on myös paketti [**time**](https://docs.python.org/3/library/time.html), josta löytyy varmasti sopivat palat tilanteeseen.

### Kopioin datan uuteen muuttujaan, jonka käsittelyn jälkeen huomaan alkuperäisen muuttujan arvojen vaihtuneen?  

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


