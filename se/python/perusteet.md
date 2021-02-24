---
title: Grunder
lang: se
ref: perusteet
category: python
---

## Välkommen att använda Python!

Om du vill sätta igång med att lära dig Python direkt kan du lösa och testa dig fram i vår guide för datahantering:


**Guide för Python**[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/cms-opendata-education/cms-jupyter-materials-finnish/master?filepath=TyokalutTutuiksi%2FOhjeita%20Pythonin%20k%C3%A4ytt%C3%B6%C3%B6n.ipynb) [![Colaboratory](https://github.com/cms-opendata-education/cms-jupyter-materials-finnish/blob/master/Kuvat/colab_icon.png?raw=true)](https://colab.research.google.com/github/cms-opendata-education/cms-jupyter-materials-finnish/blob/master/TyokalutTutuiksi/Ohjeita%20Pythonin%20k%C3%A4ytt%C3%B6%C3%B6n.ipynb)

Om du inte alls är bekant med programmering från tidigare, och vill lära dig Python ordentligt från grunden kan du hitta massvis med instruktioner med hjälp av google eller direkt på adressen [learnpython.org](https://www.learnpython.org/). För vår användning av Python här krävs inte så mycket kunskap om programmering, men om du som lärare vill skapa eget material är det bra att ha en bredare kunskap än det vi erbjuder här. 

Python som programmeringsspråk strävar efter minimalism. Hr är ett utdrag ur Pythons grundfilosofi, ["Zen of Python"](https://en.wikipedia.org/wiki/Zen_of_Python):

- Beautiful is better than ugly.
- Explicit is better than implicit.
- Simple is better than complex.
- Complex is better than complicated.
- Flat is better than nested.
- Sparse is better than dense.
- Readability counts.

Det här märks direkt från början i att användaren inte behöver krångla med att specificera dokumentklass eller navigera i mappar.

Ta python-scripten nedan som exempel. Det här är en fullständig kod som importerar en datafil och sätter in dess värden i ett histogram. Vi tar en titt på vad varje del av koden gör:
  **import**-kommandot läser in funktionspaket. Paketen vi använder är **pandas**, som innehåller funktioner för att läsa in datafiler och **matplotlib.pyplot**, som låter oss rita upp diagram och grafer.
  Vi skapar en variabel, "dataset", och läser in en datafil med hjälp av funktionen **read_csv** i *pandas*. **csv** står för "comma separated values", vilket i sig beskriver vad en sådan fil innehåller. Alla värden i datafilen är nu sparade i variabeln *dataset*.
  Kommandot **plt.hist** skapar ett histogram över alla värden i variabeln *dataset*. Parametern **bins=100** anger att histogrammet består av 100 staplar, jämnt fördelade från det minsta till det största värdet i *dataset*.
  Vi kan lägga till fler **plt.**-kommandon om vi vill, för att t.ex ändra på histogrammets skala och färg eller namnge axlarna i diagrammet. Vi behöver avsluta med kommandot **plt.show** för att histogrammet ska visas.



````python
import pandas as pd
import matplotlib.pyplot as plt

dataset = pd.read_csv("Hit sätter vi en länk till någon datafil")

plt.hist(dataset, bins = 100)
plt.show()
````
