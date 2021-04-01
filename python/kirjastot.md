---
title: Kirjastot ja moduulit
lang: fi
ref: kirjastot
category: python
---

## Paketit, funktiokirjastot, moduulit

Joku on kuitenkin ratkaissut jo ongelmasi, siihen pitää vain löytää sopiva moduuli.

Pythonissa käyttäjä voi ottaa käyttöönsä funktiokirjastoja, eli paketteja, joiden sisältä sitten otetaan käyttöön kulloinkin tarvittu työkalu (funktio tai metodi). Esimerkiksi yksittäistä Notebookia käyttäessä
alkuun kannattaa kirjoittaa koodisolu, jossa tuodaan **import**-komennolla käyttöön tarvittavat paketit. Tässä yhteydessä yleensä nimetään ne uudelleen lyhenteinä, jotta myöhempi viittaus on helpompaa ja nopeampaa.

Alla on esimerkki, jossa on otettu käyttöön muutama tavallisesti tarvittava paketti ja tehty jotain näiden avulla. Huom. #-merkillä alkavat rivit tai rivin loppuosat ovat kommentteja, jotka eivät vaikuta itse koodiin.

````python
import pandas as pd # tämä paketti sisältää datan lukemiseen sopivia työkaluja
import matplotlib.pyplot as plt # tämä on joukko piirtotyökaluja kuvaajien tekemiseen
import numpy as np # tässä paketissa on numeerisia laskentatyökaluja, kuten piin arvo

# Tämän latauksen jälkeen paketeissa olevia työkaluja voidaan käyttää.

# Datan lukeminen tiedostosta ja tallentaminen muuttujaan
data = pd.read_csv("LinkkiKohteeseen.csv")

# Muuttujan arvon 4/pii määritteleminen
h = 4/np.pi

# Datatiedoston "ydata"-sarakkeen piirtäminen "xdata"-sarakkeen funktiona
plt.plot(data['xdata'], data['ydata'])
plt.show()
````

Internetin hakukoneilla löytää hyvin nopeasti kulloinkin tarvittavia paketteja.
Jos notebookeja käyttää selaimessa MyBinderissa, tulee kaikkien käytettävien pakettien olla listattuna allekkain "requirements.txt"-nimiseen tiedostoon siihen GitHub-repositorioon, jossa kyseinen notebook sijaitsee. Esimerkki tällaisesta tiedostosta on [täällä](https://github.com/cms-opendata-education/cms-jupyter-materials-finnish/blob/master/requirements.txt).
Jos taas notebook on avattu omalla tietokoneella Anacondalla, löytyy suuri määrä paketteja valmiiksi, eikä niiden asentamisesta tarvitse välttämättä välittää.
Jos jokin paketti kuitenkin puuttuu, sen voi asentaa avaamalla "Anaconda Prompt" ja kirjoittamalla sinne "pip install paketin_nimi".
