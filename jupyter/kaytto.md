---
category: jupyter
---

## Jupyter Notebookien käyttöönotto

<p>Jupyter Notebookeja voi käsitellä joko lokaalisti omalta tietokoneeltaan tai verkon yli selaimella virtuaalisella työtasolla.</p>

<p>Selaimessa ajettaessa ei tarvitse tehdä mitään latauksia ja materiaaleihin pääsee yleensä parissa minuutissa käsiksi, mutta tämä vaatii jatkuvaa verkkoyhteyttä
ja on usein aikarajoitettua (MyBinder esimerkiksi irrottaa yhteyden, mikäli mitään laskentaa ei tehdä kymmeneen minuuttiin). Sopii hyvin esimerkiksi demoihin tai intensiiviseen
työpajatoimintaan, mutta pidempiä projekteja varten kannattaa suosiolla ladata koneelleen sopiva sovellus tätä varten.

</p>

### 1. Pikaohje selaimessa avaamiseen

#### MyBinder

I Etsi sopivan muistion tai GitHub-repon osoite, esim. [https://github.com/cms-opendata-education/cms-jupyter-materials-finnish/blob/master/Demot/Hiukkasfysiikkaa/Higgs-hakusessa-4-leptonia.ipynb](https://github.com/cms-opendata-education/cms-jupyter-materials-finnish/blob/master/Demot/Hiukkasfysiikkaa/Higgs-hakusessa-4-leptonia.ipynb)


II Avaa [MyBinder](https://mybinder.org), joka rakentaa virtuaalisen työtilan. Sivu näyttää suunnilleen tältä:

![binder](../assets/img/Binder.png)


III Kopioi ensimmäisen kohdan osoite kenttiin, joko pelkkä [https://github.com/cms-opendata-education/cms-jupyter-materials-finnish](https://github.com/cms-opendata-education/cms-jupyter-materials-finnish) (rakentaa koko repon ja avaa puurakenteen) tai suoraan tiedostoon paloittelemalla linkki tähän tapaan:

![binder](../assets/img/Binder2.png)
 

IV Paina "launch" ja odota hetki.


V Käy hommiin!


VI Opetushommia ajatellen, huomaa kuvan alaosassa näkyvä valmiiden materiaalien jakolinkki joka on helppoa upottaa verkkosivuille tai viesteihin niin että opiskelijat pääsevät suoraan töihin yhdellä klikkauksella. Esimerkiksi äskeisen harjoitteen saa Binderilla auki tästä HTML-napista painamalla:

[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/cms-opendata-education/cms-jupyter-materials-finnish/master?filepath=Demot%2FHiukkasfysiikkaa%2FHiggs-hakusessa-4-leptonia.ipynb)


#### Google Colab

I Etsi sopiva tiedosto, käytetään samaa kuin yllä (teknisesti haetaan myöhemmin, mutta tietäminen helpottaa löytämistä).


II Avaa [Colab](https://colab.research.google.com/notebooks/intro.ipynb).


III Paina vasemmalta ylhäältä "File"-valikosta "Open Notebook".


IV Avaa "GitHub" -välilehti ja hae haluamaasi repositoriota nimellä.

![colab](../assets/img/Colab.png)


V Etsi listasta haluamasi tiedosto ja paina avausnappia oikealla:

![colab](../assets/img/Colab2.png)


VI Käy hommiin!
  
VII Sama juttu pikalinkkien kanssa, Colabiinkin voi viitata suoraan yhdellä klikkauksella:
[![Colaboratory](https://github.com/cms-opendata-education/cms-jupyter-materials-finnish/blob/master/Kuvat/colab_icon.png?raw=true)](https://colab.research.google.com/github/cms-opendata-education/cms-jupyter-materials-finnish/blob/master/Demot/Hiukkasfysiikkaa/Higgs-hakusessa-4-leptonia.ipynb)


### 2. Pikaohje omalla koneella toimimiseen

I Asenna koneellesi sopiva sovellus, kuten itse [Jupyter Notebook](https://jupyter.org/) tai laajempi datatieteen paketti kuten [Anaconda](https://www.anaconda.com/products/individual), jossa on aiempi mukana.

II Avaa äskeinen (Anacondan tapauksessa löytynee nimellä Anaconda Navigator).

III Valitse "Jupyter Notebook", joka avaa verkkoselaimeesi koneesi paikallisen puurakenteen. 

![ana](../assets/img/ana.png)

![tree](../assets/img/tree.png)

IV Etsi tiedostoistasi haluamasi muistio ja käy töihin.

V Jos haluat tehdä uusia muistioita, navigoi itsesi puussa kansioon johon haluat tehdä uuden tiedoston ja paina "New" nappia.

![new](../assets/img/tree2.png)





