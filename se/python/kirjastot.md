---
title: Bibliotek och moduler
lang: se
ref: kirjastot
category: python
---

## Paket, funktionsbibliotek och moduler

Någon har redan löst ditt problem. Du behöver bara hitta rätt modul.

I Python kan användaren bruka funktionsbibliotek, även kallade paket, som innehåller olika funktioner och metoder. När du börjar skapa en Notebook lönar det sig att börja med en kodcell där du använder **import**-kommandot för att läsa in paketen du behöver för arbetet. Det kan också löna sig att skapa förkortningar för dem (**import** [paket] **as** [förkortning]) för att göra det smidigare att hänvoisa till dem senare.

````python
# Text som inleds med en "hashtag" räknas inte som en del av koden

import pandas as pd # Det här paketet innehåller verktyg för att läsa in datafiler.
import matplotlib.pyplot as plt # Innehåller olika verktyg för att rita diagram och grafer.
import numpy as np # Innehåller verktyg för numeriska beräkningar, exempelvis värdet på pi.

# Efter att man har laddat in paketen kan man använda deras funktioner på formen "paket.funktion". 
# Exempel:

data = pd.read_csv("Länktilldatafilen.csv") # Läser in en datafil och sparar dess värden som variabeln "data"

h = 4/np.pi # np.pi ger ett noggrannt närmevärde för pi
````

Med hjälp av sökmotorer går det snabbt att hitta de paket man behöver, men det är bra att komma ihåg att inte alla programmeringsmiljöer låter en använda dem direkt. Man kan ladda ned paket för lokal användning med hjälp a v [PIP-kommandot](https://www.w3schools.com/python/python_pip.asp) (preferred installer program, ett verktyg som finns inbyggt i de flesta programmeringsmiljöer). I en webbläsarmiljö som MyBinder eller CoLab kan man lägga till nya paket i *requirements.txt*-filen, som används som grund för att skapa det virtuella arbetsrummet.
