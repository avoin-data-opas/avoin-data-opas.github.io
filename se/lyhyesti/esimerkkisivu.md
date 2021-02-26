---
title: Exempel på Notebook
lang: se
ref: esimerkkisivu
category: lyhyesti
---

## Att läsa in en datafil och framställa den visuellt

Vi går genom ett enkelt exempel!

- Vi söker upp en datafil, exempelvis [den här från SIDCs hemsida](http://sidc.oma.be/silso/datafiles), som berör solfläckar.
- Vi skapar en Notebook som kan öppna den:

![kuva](../../assets/img/aurinko1.png)

- Det verkar som om tabellen läses in lite dåligt. Vi testar att ändra tabellens titel (header):

![kuva](../../assets/img/aurinko2.png)

- Det här verkar inte riktigt rätt heller. Problemet är att värdena i tabellen är separerade med semikolon. ".csv" står för "comma separated values", så vi måste ändra inställningarna för att tolka semikolon. Vi kan göra detta med hjälp av parametern "sep" (separator):

![kuva](../../assets/img/aurinko3.png)


- Det var bättre. För att göra tabellen lättare att förstå vill vi namnge kolumnerna. På SIDCs hemsida kan vi se vad värdena betyder. Genom att lägga till "names"-parametern kan vi ge varje kolumn en rubrik.



![kuva](../../assets/img/aurinko4.png)


- Nu börjar det kännas som att tabellen går att förstå! Vi skapar en graf över solfläckarna på solens norra och södra halvklot:

![kuva](../../assets/img/aurinko5.png)

- Nu är vi snart klara. VI gör ännu några ändringar för att göra grafen mer läslig:



![kuva](../../assets/img/aurinko6.png)

Där var det gjort. Vi läste in data, såg hurudant det var, gjorde det prydligare och framställde det visuellt. Med hjälp av grafen vi fick kan vi till exempel studera solens mångåriga cykler, och utgående från värdena i tabellen kan vi göra noggrannare beräkningar. (Vi kan till exempel ta reda på medeltalet solfläckar per dag under ett visst år, och förändringstakten från år till år)

Pröva själv att skapa en ny Notebook och söka upp något intressant dataset, eller använd filen från detta exempel!
