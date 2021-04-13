---
title: Perusteet
lang: fi
ref: perusteet
category: python
---

## Tervetuloa Pythonin pariin!

Jos haluat päästä käytännönläheisesti alkuun, aloita näistä: 

**Esimerkki data-analyysista Pythonilla**: [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/opendata-education/Python-ja-Jupyter/main?urlpath=tree/materiaali/harjoitukset/jupyter-intro.ipynb) [![Colaboratory](https://github.com/cms-opendata-education/cms-jupyter-materials-finnish/blob/master/Kuvat/colab_icon.png?raw=true)](https://colab.research.google.com/github/opendata-education/Python-ja-Jupyter/blob/gh-pages/_sources/harjoitukset/jupyter-intro.ipynb)

**Opettele Pythonia tekemällä itse data-analyysiharjoitus**: [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/opendata-education/Python-ja-Jupyter/main?urlpath=tree/materiaali/harjoitukset/data-analyysi_esimerkki.ipynb) [![Colaboratory](https://github.com/cms-opendata-education/cms-jupyter-materials-finnish/blob/master/Kuvat/colab_icon.png?raw=true)](https://colab.research.google.com/github/opendata-education/Python-ja-Jupyter/blob/gh-pages/_sources/harjoitukset/data-analyysi_esimerkki.ipynb)

Ylläolevat esimerkit opastavat Python-ohjelmointiin erityisesti data-analyysin näkökulmasta.
Mikäli haluat oppia Pythonia aivan alusta alkaen, netistä löytyy tähän useita tutoriaaleja.
Alkuun pääsee esimerkiksi osoitteessa [learnpython.org](https://www.learnpython.org/).
Ohjelmointitaidot eivät kuitenkaan ole välttämättömiä materiaalipankkimme käyttämiseksi, vaan perusasiat data-analyysin kannalta oppii tutoriaaliemme avulla sekä tutkimalla esimerkkimuistioita.

Yksinkertainen esimerkiksi datan käsittelystä Pythonilla voisi sisältää sopivien työkalujen tuomisen (**import**), halutun datasetin lukemisen ja kuvaajan piirtämisen.

````python
import pandas as pd
import matplotlib.pyplot as plt

datasetti = pd.read_csv("LinkkiKohteeseen")

plt.hist(datasetti['sarake'], bins = 100)
plt.show()
````

Yllä olevassa esimerkissä tuodaan kaksi työkalupakettia `pandas` ja `matplotlib.pyplot`, joista ensimmäinen tarjoaa työkaluja datan lukemiseen ja käsittelyyn ja jälkimmäinen datan visualisointiin (kuvaajien piirtäminen).
Tämän jälkeen luetaan data tiedostosta ("LinkkiKohteeseen" tilalle kirjoitetaan tiedostopolku tai URL datatiedostoon) ja tallennetaan tiedot muuttujaan "datasetti".
Lopuksi piirretään kuvaaja (esimerkissä histogrammi) datasta.

Oleellista on tietää mitä kirjastoja tarvitsee tuoda kulloinkin käytettävään harjoitteeseen ja miten niissä olevia komentoja kutsutaan.
Yleisimmin tarvittavat komennot oppii kuitenkin nopeasti ja apua löytyy helposti sekä esimerkkimuistioistamme että yleisesti googlaamalla.

Pandas ja Matplotlib -kirjastojen dokumentaation löydät täältä:
- [pandas](https://pandas.pydata.org/)
- [matplotlib](https://matplotlib.org/)
