---
title: Materiaalien kanssa työskentely
lang: fi
ref: muokkaus
category: jupyter
---

## Omien Notebook-materiaalien kanssa puuhailu

Notebookit ovat helppokäyttöisiä työkaluja: pohjimmiltaan muistio koostuu soluista, joille voi valita joko teksti- tai koodistatuksen. Näitä lisäämällä ja muotoilemalla voi kirjoittaa omia materiaalipohjiaan ties minkä aineistojen analysointiin.

Jupyter Notebookien perusilme näyttää tältä (MyBinderissa on natiivina sama):

![NB](../assets/img/NBesim.png)

Soluja pääsee muokkaamaan kaksoisklikkaamalla ja niiden sisällön ajaminen ytimen kautta onnistuu joko työkalurivin **"Run"**-painikkeesta tai suoraan näppäimistöltä painamalla **Ctrl+Enter**. Jos solu on valittu, sen ympärillä on sininen reunus, joka muuttuu vihreäksi muokkaustilassa.

Työkalurivin **"Help"**-valikosta (tai painamalla **"h"** ilman soluvalintaa) löytyy lista pikanäppäimistä.

Solujen vasemmalla puolella näkyvissä sulkeissa on järjestysnumero, joka kertoo missä vaiheessa kyseinen solu on ajettu. Mikäli siinä näkyy tähti (**\***), solua ajetaan yhä. Joskus ajo kestää pitkään, esimerkiksi animaatioita tai isoja latauksia tehdessä, mutta jos näin ei pitäisi olla kyseisessä koodissa on todennäköisesti loppumaton silmukka joka pitää keskeyttää **"Kernel"**-valikon kautta keskeyttämällä ajo **"Interrupt"**-käskyllä.

Välillä voi myös käydä niin, että ytimeen on jäänyt sotkuinen muuttuja joka aiheuttaa virheitä myöhemmissä komennoissa. Tällöin voi olla aiheellista ajaa määrittelevät solut uudelleen tai tyhjentää kaikki **"Kernel"**-valikon **"Restart"**-käskyillä (joilla voi myös pyyhkiä aiemmat tulokset tai ajaa alusta lähtien koko muistion kerralla yksittäisten solujen napsuttelun sijaan). Ytimen uudelleenkäynnistys tai keskeytys ei vaikuta millään tapaa muistion muotoiluun tehtyihin toimiin, vain kullakin hetkellä muistissa oleviin tuloksiin, muuttujiin ja vastaaviin olioihin.


