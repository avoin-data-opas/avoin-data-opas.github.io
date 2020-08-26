## Paketit, funktiokirjastot, moduulit

Joku on kuitenkin ratkaissut jo ongelmasi, siihen pitää vain löytää sopiva moduuli.

Pythonissa käyttäjä kutsuu käyttöönsä funktiokirjastoja, eli paketteja, joiden sisältä sitten otetaan käyttöön kulloinkin tarvittu metodi. Esimerkiksi yksittäistä Notebookia käyttäessä
alkuun kannattaa kirjoittaa koodisolu, jossa tuodaan **import**-komennolla käyttöön tarvittavat paketit. Tässä yhteydessä voidaan kivasti nimetä ne uudelleen, jotta myöhempi viittaus
on nopeampaa.

````python
import pandas as pd # tämä paketti sisältää datan lukemiseen sopivia työkaluja
import matplotlib.pyplot as plt # tämä on joukko piirtotyökaluja kuvaajien tekemiseen
import numpy as np # tässä paketissa on numeerisia laskentatyökaluja, kuten piin arvo

# Tämän latauksen jälkeen paketeista voidaan kiskoa työkaluja ulos.

data = pd.read_csv("LinkkiKohteeseen")

h = 4/np.pi
print(h)
````

Internetin hakukoneilla löytää hyvin nopeasti kulloinkin tarvittavia paketteja, mutta kannattaa huomata ettei näihin pääse suoraan käsiksi kaikista ympäristöistä. Paketteja voi ladata koneelleen PIP-käskyllä (preferred installer program, useimpiin ympäristöihin sisäänrakennettu työkalu pakettien asennukseen komentorivin kautta) tai selainympäristössä (MyBinder, CoLab...) mainitsemalla ne etukäteen requirements.txt -tiedostossa, jonka pohjalta virtuaalinen työtila rakennetaan.
