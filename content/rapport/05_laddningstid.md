---
---
05_laddningstid
=========================

Detta moment, kmom05, i kursen Design handlar om att utvärdera webbplatsers laddningstid och användbarhet.  
Följande är vår uppgiftsbeskrivning:  
Du skall välja ut ett antal olika webbplatser och testa dem för att mäta hur snabbt de laddas och om de innehåller några saker som kan förbättras med tanke på laddningstid och användbarhet.


Urval
-----------------------
När jag valde webbplatser att analysera tänkte jag att det skulle vara roligt att
se hur några av mina vänners sidor fungerar men även testa en av mina egna för att
se om den håller måttet eller inte.  
Jag valde två sidor som vänner till mig äger.

* [Café på bit](http://cafepabit.se/)
* [Core of dekor](http://coreofdecor.se/)

och sedan en sida som jag själv knåpade ihop som projekt i kursen htmlphp.

* [BMO](http://www.student.bth.se/~jiho19/dbwebb-kurser/htmlphp/me/kmom10/main.php)

Metod
-----------------------

Det verktygen som jag använde mig av för att få fram önskad data var:

* Firefox
* PageSpeed Insights
* Devtools nätverkstest i Firefox
* Google spreadsheets.

Jag startade mitt test genom att köra de tre sidorna från de tre webbplatserna i
PageSpeed Insights. Där får man en upp en poäng från (dålig)1 - 100(bra) hur väl
sidan fungerar och ytterligare information som vad som tas in i beräkningen i poängen
och även tips på hur man kan göra sidan snabbare finns att läsa längre ner på sidan.
Sedan inpekternade jag element i Firefox och kikade i Nätverks-fliken där jag kunde
få fram data så som laddningstid, antal resurser som laddades samt sidans totala storlek.
Alla mätningar gjordes på tre olika webbplatser och i dem tre olika undersidor, tre gånger
för att få fram ett snitt.
Resultaten från mätningarna sparades i Google spreadsheets.

Resultat
-----------------------
Här finns kalkylen med samtliga mätresultat: 
[Mätresultat](https://docs.google.com/spreadsheets/d/e/2PACX-1vSXK1HoEEkEp9cOOTxD1r8kwhg_vy8GQSig48USWq1kbMv6T2hIoXTHXaANKbUzoSoS_Ulwrl6A0Abv/pubhtml)


#### Café på bit

[FIGURE src=img/cafe.png caption="*Skärmdump på Café på bits webbplats*"]


Core of decore hade sämst poängen av de tre webbplatserna när den kördes i
PageSpeed Insights med ett medelvärde: 57 på mobil och 89 på dator.  
Webbplatsen hade testets sämsta laddningstider med: 1,27s på mobil och 1,23s på dator.  
Den "dåliga" laddningstiden berodde på en startsida som drog upp snittet.

Detta tipsade PageSpeed Insights om som möjliga åtgärder för att snabba på sidan:  
(top 3)

* Aktivera textkomprimering
* Ta bort resurser som blockerar renderingen
* Ta bort oanvänd CSS

#### Core of Decore

[FIGURE src=img/cod.png caption="*Skärmdump på Core of Decors webbplats*"]


Core of decore hade den sämsta poängen av de tre webbplatserna när den kördes i
PageSpeed Insights med ett medelvärde: 39 på mobil och 72 på dator.  
Webbplatsen hade testets sämsta laddningstider med: 1,04s på mobil och 1,07s på dator.  
Till skillnad från Café på bit hade denna webbplats en jämn och låg laddningstid
på alla testade undersidor.

Detta tipsade PageSpeed Insights om som möjliga åtgärder för att snabba på sidan:  
(top 3)

* Ta bort resurser som blockerar renderingen 
* Ta bort oanvänd CSS 
* Skicka bilder i modernare bildformat 

#### BMO

[FIGURE src=img/bmo.jpg caption="*Skärmdump på BMOs webbplats*"]

BMO hade den bästa poängen av de tre webbplatserna när den kördes i
PageSpeed Insights med ett medelvärde: 92 på mobil och 100 på dator.  
Webbplatsen hade testets näst bästa laddningstider med: 1,12s på mobil och 1,13s på dator.  
Likt Core of decore hade denna webbplats en jämn och låg laddningstid på alla testade undersidor.

Detta tipsade PageSpeed Insights om som möjliga åtgärder för att snabba på sidan:  
(top 3)

* Skicka bilder i modernare bildformat 
* Koda bilder effektivt 
* Ta bort resurser som blockerar renderingen 

Analys
-----------------------

En tydlig vinnare om man går efter Google PageSpeed Insights poäng är BMO, den sidan som jag
själv gjorde i kursen htmlphp. Anledningen till det tror jag är att vi har ett validerings-
verktyg som måste godkänna koden innan den publiseras och då eleminerar många av de problem
som de andra sidorna hade. Det åtgärder som rekomenderades för min sida vad alla kopplade
till mina bilder, tex att skicka bilder i modernare bildformat eller att koda bilderna
mer effektivt. 
De andra webbplatserna har gemensamt att i de top 3 åtgärderna som Google PageSpeed Insights
rekommenderar finns "Ta bort resurser som blockerar renderingen" och "Ta bort oanvänd CSS" 
Att Ta bort resurser som blockerar renderingen hade jag på två av mina sidor när dom testades
på mobil plattform, men tiden som skulle vinnas av att åtgärda det var bara en bråkdel av vad både Café på bits och Core of decors kunde vinna på det. Oanvänd CSS hade jag ingen, vilket är att förväntas då det är något mitt valideringsverkyg direkt skulle reagera på.  
Så egentigen ganska lätta fel att korrigera för att få sidan att laddas snabbare och få upp poängen en hel del, lite slarv i koden bara som möblering och städning kunde fixa.

Laddningstiden vanns av core of decor, tätt följt av BMO, Café på bit som har testets i
särklass enklaste sida hade sämst tider vilket vid närmre inspektion bla verkar bero
på svarstider från servern vilket var listat som åtgärd på samtliga undersidor men inte
på en enda en av de andra webbplatsern.  
Samtliga sidor hölls sig under en laddningstid på 1,30s vilket är enligt en studie
som jag har läst ungefär medelbetyg (1,286s) och jag reagerade då inte det minsta på någon av sidorna att den tog länge att ladda. Jag tycker att det är lite svårt sätta en siffra på hur länge det max får ta för en sida att ladda, man har ju helt klart vant sig att allt ska komma fram nästan på en gång och gör det inte det blir man direkt lite irriterad, men var den gränsen går är svår att sätta. Läste i en undersökning att 55% av användare som går in på en webbplats som laddar längre än 3s lämnar sidan och sitter man och räknar till 3s när man laddar en hemsida så är det ganska lång tid faktiskt, så jag säger att 3s är gränsen för mig.

Skulle jag rangordna webbplatserna med poäng från Google PageSpeed Insights och laddningstiderna från devtools så ser du ut så här:

1. BMO
2. Core of Decor
3. Café på bit


Referenser
-----------------------

* [Café på bit](http://cafepabit.se/)
* [Core of decor](http://coreofdecor.se/)
* [BMO](http://www.student.bth.se/~jiho19/dbwebb-kurser/htmlphp/me/kmom10/main.php)
* [Google PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/?hl=sv)

Övrigt
-----------------------

Jimmy Hortlund 