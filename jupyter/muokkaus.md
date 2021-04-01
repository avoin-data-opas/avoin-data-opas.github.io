---
title: Materiaalien kanssa työskentely
lang: fi
ref: muokkaus
category: jupyter
---

## Omien Notebook-materiaalien kanssa työskentely

Notebookit ovat helppokäyttöisiä työkaluja: pohjimmiltaan muistio koostuu soluista, jotka voivat sisältää joko koodia tai tekstiä. Näitä lisäämällä ja muotoilemalla voi kirjoittaa omia materiaalipohjiaan minkä tahansa aineistojen analysointiin tai muuhun ohjelmointiin liittyvään toimintaan.

Jupyter Notebookien perusilme näyttää tältä:

![NB](../assets/img/NBesim.png)

Soluja pääsee muokkaamaan kaksoisklikkaamalla ja solun sisällön suorittaminen onnistuu joko työkalurivin **"Run"**-painikkeesta tai suoraan näppäimistöltä painamalla **Ctrl+Enter**. Jos solu on valittu, sen ympärillä on sininen reunus, joka muuttuu vihreäksi muokkaustilassa.

Työkalurivin **"Help"**-valikosta (tai painamalla **"h"** ilman soluvalintaa) löytyy lista pikanäppäimistä.

Solujen vasemmalla puolella näkyvissä sulkeissa on järjestysnumero, joka kertoo missä vaiheessa kyseinen solu on ajettu. Mikäli siinä näkyy tähti (**\***), solua ajetaan yhä. Joskus ajo voi kestää pitkään, esimerkiksi animaatioita tai isoja latauksia tehdessä, mutta jos näin ei pitäisi olla kyseisessä koodissa on todennäköisesti loppumaton silmukka. Tällöin solun suorittamisen voi keskeyttää työkalurivin **interrupt**-painikkeella ( ■ ).

Jos koodi ei toimi tai se antaa outoja tuloksia, kannattaa kokeilla tyhjentää muisti **"Kernel"**-valikon **"Restart"**-käskyillä (joilla voi myös pyyhkiä aiemmat tulokset tai ajaa alusta lähtien kaikki muistion solut).
Muistin tyhjentäminen tai keskeytys ei vaikuta millään tapaa muistion muotoiluun tehtyihin toimiin, vain kullakin hetkellä muistissa oleviin tuloksiin, muuttujiin ja vastaaviin olioihin.
