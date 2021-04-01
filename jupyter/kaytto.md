---
title: Käyttöönotto
lang: fi
ref: kaytto
category: jupyter
---

## Jupyter Notebookien käyttöönotto

Jupyter Notebookeja voi käsitellä joko lokaalisti omalta tietokoneeltaan tai verkon yli selaimella virtuaalisella työtasolla.

Selaimessa ajettaessa ei tarvitse tehdä mitään latauksia ja materiaaleihin pääsee yleensä parissa minuutissa käsiksi, mutta tämä vaatii jatkuvaa verkkoyhteyttä ja on usein aikarajoitettua (MyBinder esimerkiksi irrottaa yhteyden, mikäli mitään muistiota ei käytetä kymmeneen minuuttiin). Selainkäyttö hyvin esimerkiksi demoihin, työpajatoimintaan, ja yksittäisten notebookien jakamiseen opiskelijoille, mutta pidempiä projekteja ja omien materiaalien tekemistä varten kannattaa ladata koneelleen sopiva sovellus (kuten Anaconda) tätä varten.

### 1. Notebookin avaaminen selaimessa

#### MyBinder

1. Etsi sopivan muistion tai GitHub-repon osoite, esim. [https://github.com/cms-opendata-education/cms-jupyter-materials-finnish/blob/master/Demot/Hiukkasfysiikkaa/Higgs-hakusessa-4-leptonia.ipynb](https://github.com/cms-opendata-education/cms-jupyter-materials-finnish/blob/master/Demot/Hiukkasfysiikkaa/Higgs-hakusessa-4-leptonia.ipynb)
1. Mene [MyBinder](https://mybinder.org)-palveluun. Sivu näyttää suunnilleen tältä: ![binder](../assets/img/Binder.png)
1. Kopioi ensimmäisen kohdan osoite kenttiin, joko pelkästään GitHub-hakemiston osoite [https://github.com/cms-opendata-education/cms-jupyter-materials-finnish](https://github.com/cms-opendata-education/cms-jupyter-materials-finnish) (rakentaa koko hakemiston, josta voidaan käyttää kaikkia hakemiston muistioita) tai suoraan yhden muistion osoite paloittelemalla linkki tähän tapaan: ![binder](../assets/img/Binder2.png)
1. Paina "launch" ja odota hetki.
1. Käy hommiin!
1. Opetushommia ajatellen, huomaa kuvan alaosassa näkyvä jakolinkki. Linkin voi jakaa sellaisenaan opiskelijoille tai vaikkapa upottaa verkkosivulle, jolloin muistio aukeaa suoraan linkkiä painamalla. Esimerkiksi äskeisen harjoitteen saa Binderilla auki tästä napista painamalla: [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/cms-opendata-education/cms-jupyter-materials-finnish/master?filepath=Demot%2FHiukkasfysiikkaa%2FHiggs-hakusessa-4-leptonia.ipynb)


#### Google Colab (vaatii Google-tilin)

1. Etsi sopiva tiedosto, käytetään samaa kuin yllä (teknisesti haetaan myöhemmin, mutta tietäminen helpottaa löytämistä).
1. Avaa [Colab](https://colab.research.google.com/notebooks/intro.ipynb).
1. Paina vasemmalta ylhäältä "File"-valikosta "Open Notebook".
1. Avaa "GitHub" -välilehti ja hae haluamaasi repositoriota nimellä. ![colab](../assets/img/Colab.png)
1. Etsi listasta haluamasi tiedosto ja paina avausnappia oikealla: ![colab](../assets/img/Colab2.png)
1. Käy hommiin!
1. Sama juttu pikalinkkien kanssa, Colabiinkin voi viitata suoraan yhdellä klikkauksella:
[![Colaboratory](https://github.com/cms-opendata-education/cms-jupyter-materials-finnish/blob/master/Kuvat/colab_icon.png?raw=true)](https://colab.research.google.com/github/cms-opendata-education/cms-jupyter-materials-finnish/blob/master/Demot/Hiukkasfysiikkaa/Higgs-hakusessa-4-leptonia.ipynb)


### 2. Notebookien käyttö omalla koneella

#### Materiaalien lataaminen

1. Jos haluat käyttää materiaalipankkimme materiaaleja omalla koneellasi, sinun tulee ensin ladata ne [GitHub-sivultamme](https://github.com/cms-opendata-education/cms-jupyter-materials-finnish). Voit ladata kaiken sisällön kerralla zip-pakettina klikkaamalla nappia "Code" ja valitsemalla vaihtoehdon "Download ZIP": ![GitHub-materiaalien lataaminen](../assets/img/github-materiaalien-lataaminen-nuolilla.png)
1. Pura zip-paketti haluamaasi kansioon tietokoneellesi.

#### Materiaalien käyttäminen

1. Asenna koneellesi datatieteen ohjelmisto [Anaconda](https://www.anaconda.com/products/individual), joka sisältää mm. Jupyter Notebookin, Pythonin sekä paljon yleisiä Python-paketteja, joita esimerkkimateriaaleissakin tarvitaan.
1. Avaa Anacondan Navigator.
1. Valitse "Jupyter Notebook", joka avautuu selaimeen. Näet tietokoneesi tiedostot ![ana](../assets/img/ana.png) ![tree](../assets/img/tree.png)
1. Etsi tiedostoistasi haluamasi muistio ja käy töihin.
1. Jos haluat tehdä uusia muistioita, navigoi itsesi puussa kansioon johon haluat tehdä uuden tiedoston ja paina "New" nappia. ![new](../assets/img/tree2.png)
