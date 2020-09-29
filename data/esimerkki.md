---
category: data
---

## Esimerkkitapaus datan lataamisesta ja käsittelystä

Tehdään helppo esimerkki!

- Etsitään aineistoa, kuten vaikka aikasarja auringonpilkuista [SIDC:n sivuilta](http://sidc.oma.be/silso/datafiles).
- Tehdään muistio joka pystyy avaamaan sen:

![kuva](../assets/img/aurinko1.png)

- Lukeminen näyttää alkaneen huonosta kohtaa, käsketääs tulokseen mukaan otsikkorivi:

![kuva](../assets/img/aurinko2.png)

- No ei nyt ihan mennyt putkeen tämäkään, mutta huomaamme että syynähän on huonosti muotoiltu taulukko. Oletuserotin pd.read_csv() -komennolle on pilkku, mutta datassa näkyy puolipisteitä. Korjataan parametrilla "sep":

![kuva](../assets/img/aurinko3.png)

- Parempi. Nyt voi tietysti ihmetellä saisiko sarakkeet nimettyä paremmin, jos katsoo mitä kukin tarkoittaa (selitys SIDC:n sivuilla). Käytetään "names"-parametria latauksen yhteydessä. Voisi nämä nimetä muuttujassakin, mutta samalla vaivalla se pienillä tiedostoilla menee tässäkin.

![kuva](../assets/img/aurinko4.png)

- No johan alkaa näyttää ymmärrettävältä informaatiolta! Otetaan nopea kuvaaja pohjoisen ja eteläisen auringonpuoliskon pilkkuluvuista:

![kuva](../assets/img/aurinko5.png)

- Hahaa, voiton puolella. Tehdään vielä joukko muotoilutoimenpiteitä paremman esityksen nimissä:

![kuva](../assets/img/aurinko6.png)

Ja siinä se sitten onkin. Haettiin dataa, katsottiin millaista se on, muotoiltiin se nätimmäksi ja esitettiin se kivana visualisaationa josta voidaan ryhtyä pureutumaan vaikka auringon monivuotisiin sykleihin tai jatkaa tarkemmin itse datan kanssa (selvitetään vaikka keskimääräiset päivittäiset pilkkumäärät ja niiden vuosittaiset vaihtelut).

Kokeile itse samaa luomalla uusi muistio ja etsimällä kiintoisa datasetti (tai kopsaa osoite yltä)!

