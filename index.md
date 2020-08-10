## Lyhyesti

Täältä pääset nopeasti alkuun tai voit kerrata perusasiat, jos jo opitut taidot ovat päässeet unohtumaan.

{% for subtopic in site.data.docs %}
                {{ subtopic.time }}
{% endfor %}

- mistä löydän materiaalit ({{ site.data.docs.time[0] }})
- kuinka avaan Jupyter notebook -sivun ({{ site.data.docs.time[1] }})
- kuinka muokkaan materiaalia omaan käyttööni ({{ site.data.docs.time[2] }})
- kuinka luon kokonaan uuden jupyter notebook -sivun ({{ site.data.docs.time[3] }})
- kuinka oppilaat voivat tallentaa omat harjoituksensa ja avata ne uudestaan ({{ site.data.docs.time[4] }})
