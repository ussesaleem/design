---
---
Utvärdering av laddningstid
=======================

Uppgiften handlar om att välja ett antal webbplatser som analyseras med avseende på deras
laddningstid och användbarhet.

Urval
-----------------------

För att välja vilka webbplatser som skulle jämföras ville jag gärna testa hur pass väl dagens framstående hemsidor med webbshoppar mäter sig mot varandra. En bra utgångspunkt i att välja hemsidorna var hur pass starkt varumärket är då det är dessa sidor som behöver ha högst prestanda (i teorin) på grund av mer trafik. De hemsidor som jag identifierade var [H&M](www2.hm.com/sv_se/index.html), [MQ](www.marqetstores.se) och [Volt Fashion](www.voltfashion.com/sv/).


Metod
-----------------------

Verktygen som jag använde mig utav var:  
- Google Chrome  
- PageSpeed Insights  
- Chromes devtools för nätverkstest  
- Google Sheets


Då samtliga av testobjekten kräver att man har ett inlogg på dessa sociala plattformar, vilket jag har, valde jag först att jämföra laddningstiden på förstasidan, inloggningssidan. Jag använde verktyget PageSpeed Insights för att se vilken mätning dessa sidor fick samt eventuella förbättringsområden som rekommenderas.

Därefter gick jag in på respektive sida i Google Chrome och öppnade upp devtools för att utforska nätverksfliken för att se antal resurser (requests), sidans storlek, finish tiden, DOMContentload tiden och laddningstiden för både mobil (iPhone X) och desktop. Sidan laddades om tre gånger och mätvärden togs samtliga gånger vars snitt presenteras i följande Excel-ark på [Google Sheets](https://docs.google.com/spreadsheets/d/18_th7zu7i83u_h-NJC8vPZrStfyVlHOHpkh7nwx1D6c/edit?usp=sharing).


Resultat
-----------------------

[FIGURE src="http://localhost:8080/dbwebb/design/me/redovisa/htdocs/cimage/img.php?src=hm_forstasida.jpg" caption="H&Ms förstasida." class="center"]

H&Ms förstasida, kontakta oss sidan och våra butiker, fick följande resultat i PageSpeed poäng:  

<u>Mobil</u>  
Förstasida: 14/100  
Kontakta oss: 12/100  
Våra butiker: 5/100  

Förbättringsområden för H&Ms mobilsida, på Våra Butiker som visade lägst resultat i PageSpeed poäng är:  
- Ta bort resurser som blockerar renderingen.  
- Ta bort oanvänd CSS.  
- Minska svarstiden från servern.  

<u>Desktop</u>  
Förstasida: 80/100  
Kontakta oss: 74/100  
Våra butiker: 72/100  

Förbättringsområden för H&Ms desktopsida, på Våra Butiker som visade lägst resultat i PageSpeed poäng är:  
- Läs in viktiga resurser i förväg.  
- Ta bort resurser som blockerar renderingen.  
- Ta bort oanvänd CSS.

För att se resterande resultat, se tabell på [Google Sheets](https://docs.google.com/spreadsheets/d/18_th7zu7i83u_h-NJC8vPZrStfyVlHOHpkh7nwx1D6c/edit?usp=sharing).


[FIGURE src="http://localhost:8080/dbwebb/design/me/redovisa/htdocs/cimage/img.php?src=mq_forstasida.jpg" caption="MQs förstasida." class="center"]

MQs förstasida, kontakta oss sidan och våra butiker, fick följande resultat i PageSpeed poäng:  

<u>Mobil</u>  
Förstasida: 33/100  
Kontakta oss: 42/100  
Våra butiker: 35/100  

Förbättringsområden för MQs mobilsida, på förstasidan som visade lägst resultat i PageSpeed poäng är:  
- Läsa in resurser i förväg.  
- Skicka bilder i modernare bildformat.  
- Ta bort oanvänd CSS.  

<u>Desktop</u>  
Förstasida: 70/100  
Kontakta oss: 79/100  
Våra butiker: 73/100  

Förbättringsområden för MQs desktopsida, på förstasidan som visade lägst resultat i PageSpeed poäng är:  
- Läsa in resurser i förväg.  
- Minska svarstiderna från servern.  
- Använd bilder med rätt storlek.  

För att se resterande resultat, se tabell på [Google Sheets](https://docs.google.com/spreadsheets/d/18_th7zu7i83u_h-NJC8vPZrStfyVlHOHpkh7nwx1D6c/edit?usp=sharing).


[FIGURE src="http://localhost:8080/dbwebb/design/me/redovisa/htdocs/cimage/img.php?src=volt_forstasida.jpg" caption="Volts förstasida." class="center"]

Volts förstasida, kontakta oss sidan och våra butiker, fick följande resultat i PageSpeed poäng:  

<u>Mobil</u>  
Förstasida: 27/100  
Kontakta oss: 11/100  
Våra butiker: 20/100  

Förbättringsområden för Volts mobilsida, på kontakta oss sidan som visade lägst resultat i PageSpeed poäng är:  
- Ta bort resurser som blockerar renderingen.  
- Aktivera textkomprimering.  
- Ta bort oanvänd CSS.  

<u>Desktop</u>  
Förstasida: 72/100  
Kontakta oss: 60/100  
Våra butiker: 63/100  

Förbättringsområden för Volts desktopsida, på kontakta oss sidan som visade lägst resultat i PageSpeed poäng är:  
- Se till att all text förblir synlig medan webbteckensnitten läses in.  
- Minska påverkan från tredjepartskod.  
- Undvik onödigt stort DOM-träd.  

För att se resterande resultat, se tabell på [Google Sheets](https://docs.google.com/spreadsheets/d/18_th7zu7i83u_h-NJC8vPZrStfyVlHOHpkh7nwx1D6c/edit?usp=sharing).


Analys
-----------------------

Generellt ser man att de sidor som mäter ett lågt PageSpeed värde på mobil även har det lägsta värdet på desktop. Vad gäller Våra Butiker sidan som H&M hade lägst poäng på går det att argumentera om huruvida detta låga resultat, speciellt på mobil, beror på att det är en karta som läses in som först behöver hitta användaren som en del av inläsningen av sidan. En snabb överblick på mätvärden i Google Sheets visar att H&Ms Våra Butiker sida fick sin första uppritning av innehåll på mobil efter 8,1 sekunder, vilket var mycket längre tid än för MQ och Volt (1,6 s respektive 4,4 s). Detta kan potentiellt härledas till fler resurser jämfört med de andra mobilsidorna, 248 requests för H&M jämfört med 121 requests för MQ och 118 requests för Volt. Dock är det här som förbättringsförslaget kan ha störst inverkan, nämligen att ta bort de resurser som blockerar renderingen. Detta skulle nog förbättra svarstiden nämnvärt och göra en snabbare inläsning av innehållet.  

På desktopsidan hade samtliga sidor på dessa webbplatser snarlika poäng. Den som hamnade lägst i denna mätning var dock Volts kontakta oss sida, med 60/100 PageSpeed poäng. Vidare analys visar på att det även var denna sida som tog längst tid på att ladda, 6,08 s jämfört med MQs 4,57 s och H&Ms 3,69 s. Detta trots att resurserna för Volts kontaktsida var färre än för H&M och MQ (90 requests mot 243 requests och 119 requests). De största förbättringsområdet som kan förbättra denna inläsning kan vara att minska DOM trädet.  

Med hänsyn tagen till inläsning och innehåll samt laddningstid av både mobila sidan och desktop sidan kombinerat, skulle jag rangordna dessa hemsidor enligt följande:  
1. MQ  
2. Volt  
3. H&M  

Detta på grund av att användarvänligheten i MQ och Volts sidor var mycket smidigare vad gäller laddningstid och interaktivitet jämfört med H&M där sidan konstant laddades under en lång stund och fler resurser lästes in.  

En snabb laddningstid i min personliga åsikt ligger någonstans mellan 3-4 sekunder. Skulle man sätta det i perspektiv till det analysresultat som jag har samlat så stämmer det relativt väl överens med användarupplevelsen för vad som kändes som "för länge". Skulle laddningstiden för dessa sidor analyseras så är de mer än 4 sekunder, ex Volts kontaktsida på desktop sidan (6,08 s). 

Referenser
-----------------------

[Google Sheets](https://docs.google.com/spreadsheets/d/18_th7zu7i83u_h-NJC8vPZrStfyVlHOHpkh7nwx1D6c/edit?usp=sharing)  
[H&M](www2.hm.com/sv_se/index.html)  
[MQ](www.marqetstores.se)  
[Volt Fashion](www.voltfashion.com/sv/)


Övrigt
-----------------------

Usama Saleem
