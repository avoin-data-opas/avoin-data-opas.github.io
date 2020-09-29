---
category: python
---

## Tervetuloa Pythonin pariin!

Python kielenä pyrkii minimalismiin. Suunnittelufilosofiaa avaava [Zen of Python](https://en.wikipedia.org/wiki/Zen_of_Python) kertoo muun muassa seuraavaa:

- Beautiful is better than ugly.
- Explicit is better than implicit.
- Simple is better than complex.
- Complex is better than complicated.
- Flat is better than nested.
- Sparse is better than dense.
- Readability counts.

Tämä näkyy heti alusta lähtien siinä, ettei käyttäjän tarvitse erityisemmin määritellä luokkia tai sählätä kansiorakenteiden kanssa.

Yksinkertainen Python-skripti voisi esimerkiksi sisältää sopivien työkalujen tuomisen (**import**), halutun datasetin lukemisen ja siitä kuvaajan piirtämisen.

````python
import pandas as pd
import matplotlib.pyplot as plt

datasetti = pd.read_csv("LinkkiKohteeseen")

plt.hist(datasetti, bins = 100)
plt.show()
````

Oleellista on tietää mitä kirjastoja tarvitsee tuoda kulloinkin käytettävään harjoitteeseen ja miten niissä olevia komentoja kutsutaan.
