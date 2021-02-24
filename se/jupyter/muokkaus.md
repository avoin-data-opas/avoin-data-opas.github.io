---
title: Filbehandling i Notebook
lang: se
ref: muokkaus
category: jupyter
---

## Att ändra en fil i Jupyter Notebook

Notebooks är användarvänliga verktyg: I grunden består de av celler, som kan bestå antingen av text ("markdown-celler") eller kod. Genom att lägga till nya eller ändra befintliga celler kan du skriva en egen analys för de givna materialen.

Jupyter Notebooks kan se ut så här:

![NB](../../assets/img/NBesim.png)

Genom att dubbelklicka celler får man ändra dem, och man kan köra deras kod genom att trycka på **"Run"**-knappen bland verktygen eller använda snabbkommandot **Ctrl+Enter**
När du har valt en cell är den markerad med en blå kant. Eller grön, ifall du håller på att editera den.

Om du trycker på **"Help"** i verktygsmenyn eller trycker **"h"** utan att ha markerat någon cell, så får du se en lista på alla snabbkommandon.

I hakparentesen till vänster om kodcellen syns ett ordningstal. Dessa tal beskriver i vilken ordning cellerna har körts. Om parentesen innehåller en asterisk (**\***), håller cellen på att köras. Ibland tar det en stund att köra cellen, till exempel när den ska skapa en animation eller ladda in stora mängder information, men om inget sådant är på gång och cellen ändå tar lång tid att köra, så finns det troligen någon oändlig loop i koden. Den kan i så fall avslutas genom **"Interrupt"**-kommandot i **"Kernel"**-menyn

Ibland kan det hända att någon felaktig kod t.ex. leder till att en felaktig variabel har stannat i minnet. Om något sådant händer kan det vara bra att köra några celler igen, eller att återställa allt genom **"Kernel"**-menyns **"Restart"**-kommando. Detta påverkar inga ändringar du har gjort i cellerna, endast den information om beräkningar och variabler som finns (dolt) i minne.

