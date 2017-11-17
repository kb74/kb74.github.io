# Project Pepper

[![Pepper robot](pepper.jpg){:style="float: right; width: 300px;"}](pepper.jpg)
Het LUMC en het lectoraat voor Health and Technology wil onderzocht hebben hoe een interactieve robot (Pepper) kan worden ingezet in het revalidatietraject van patiënten die een gewrichtsoperatie hebben ondergaan, bv een knie- of schouderoperatie. Deze patiënten moeten bijvoorbeeld elk uur specifieke oefeningen doen om snel te revalideren. In praktijk doen veel patiënten deze oefeningen vaak niet of niet correct waardoor de revalidatie minder goed verloopt. Dat is slecht voor de patiënt, de wachtlijsten en het ziekenhuis. Het idee is dat een robot langs de patiënt gaat om instructie te geven, te observeren of de oefening correct wordt uitgevoerd, eventueel bij te sturen, en verslag uit te brengen naar de arts hoe ver de patiënt in het revalidatietraject is. In deze eerste 20 weken is het doel om te herkennen of oefeningen correct worden uitgevoerd.


# Posts


## 27 oktober 2017

De afgelopen sprint zijn we weer volop bezig geweest met de KINECT. De programmeurs van ons team hebben een programma geschreven zodat we op een gestructureerde wijze beelden kunnen opslaan vanuit de KINECT.
Door in dit programma op ‘Start’ te klikken worden 2 files aangemaakt en een aparte map. Deze 2 files zijn een .xml file waarin alle skeleton joints ( gewrichten) worden opgeslagen, in de andere file wordt het opgenomen diepte beeld opgeslagen.

AFBEELDING 9: KINECT PROGRAMMA VOOR OPSLAAN VAN DATA.
![KINECT programma voor opslaan van data](https://github.com/BorisEnthovenSchool/kb74.github.io/blob/master/pepper/Afbeelding%209.png "KINECT programma") 

Hierop hebben we zelf een test opname gemaakt van een groepslid. De data uit deze testopname hebben we kunnen verwerken d.m.v. Microsoft Excel. Hieruit konden we voorlopig de volgende grafieken laten zien:

![Vergelijking1](https://github.com/BorisEnthovenSchool/kb74.github.io/blob/master/pepper/Vergelijking%201.png "Vergelijking 1") 
Vergelijking 1Hoek rechterschouder tegenover de tijd

Bij vergelijking 1 heeft de persoon alleen zijn rechter arm zijwaarts omhoog bewogen. Je kunt hier zien in welke hoek de schouder zich bewoog afgezet tegen de tijd. 



Uit deze grafiek kun je goed opmaken dat naar mate de tijd oploopt de hoek ook oploopt van pakweg 15 graden naar 120 graden. ( oranje lijn). De blauwe lijn die de linkerschouder aanduidt blijft gelijk. Dit klopt ook omdat deze arm niet bewogen is en dus langs het lichaam hangt.

![Vergelijking2](https://github.com/BorisEnthovenSchool/kb74.github.io/blob/master/pepper/Vergelijking%202.png "Vergelijking 2") 
Vergelijking 2Beide schouder tegenover de tijd


In vergelijk 2 heeft de persoon beide armen zijwaarts bewogen. Je kunt goed zijn dat allebei de armen de hoek vergroot worden tegenover de tijd. Je kunt hier echter zien dat de persoon asymmetrisch heeft bewogen. De rechterarm ( oranje lijn) stagneert in het midden waarna hij daarna weer oploopt. Hieruit kun je aflezen dat de persoon op een moment zijn arm slomer omhoog heeft bewogen.

Na dit inzicht zijn we , op donderdag 28 Oktober,  met de KINECT en 2 videocamera’s opnames gaan maken op de Haagse Hogeschool in het Atrium (zoals beschreven in de test setup van het vorige github bericht).
Er hebben in totaal van 61 personen , 3 verschillende schouder bewegingen opgenomen.  Dit heeft ons een hele berg ( echt héél veel ) data gegeven.
Deze data is omgezet naar .csv bestandsoort zodat dit ingeladen kan worden in Python. De komende weken gaan we ons richten op het bewerken van al deze data in python. Denk hierbij vooral aan het opschonen van de verkregen data.

---

## 22 september 2017 

Inmiddels zitten we alweer aan het einde van week 4 van ons onderzoek. De laatste twee weken zijn voorbijgevlogen, waarin er binnen de onderzoeksgroep en het onderzoek een aantal ontwikkelingen hebben plaatsgevonden. Sinds ons vorige bericht hebben wij twee enthousiaste Informatica studenten mogen verwelkomen in onze groep, waardoor wij nu met meer mankracht het onderzoek uitvoeren. Daarnaast is er een afspraak geweest met de opdrachtgever in het LUMC. Ook is besloten om voortaan de Kinect camera te gebruiken als ondersteuning bij het identificeren van schouderbewegingen van mensen. Een aantal ontwikkelingen zullen hieronder nader besproken worden. 

Uit het gesprek met de opdrachtgever is gebleken dat de doelstelling van het onderzoek gericht is op het vinden van een manier hoe manueel therapeuten van het LUMC gebruik kunnen maken van 3d-camera technieken (en eventueel bijbehorende software), om zo painful arcs* te identificeren. 

In ons vorige bericht lieten wij weten de Intel Real Sense camera - die vergelijkbaar is met de camera die in de Pepper robot zit - te willen gebruiken. Door nader onderzoek naar de output van de Intel Real Sense en de mogelijkheden van de Kinect camera, is gekozen om de laatstgenoemde camera te gebruiken. Uit het door ons uitgevoerde literatuuronderzoek is gebleken dat bij gebruik van deze camera effectiever en efficiënter resultaten gerealiseerd kunnen worden door een drietal voordelen:

1. Er is meer softwareondersteuning voor de Kinect camera waardoor wij hier minder tijd aan hoeven te besteden.
1. De Kinect SDK’s zijn verder ontwikkeld waardoor er meer functies al beschikbaar zijn. Waaronder een skeleton tracking algoritme.
1. Er is literatuuronderzoek beschikbaar over de nauwkeurigheid en betrouwbaarheid van de Kinect camera.

Inmiddels is de Microsoft Kinect aangeschaft en zijn hier een aantal libraries en SDK’s uitgeprobeerd. Deze zijn hieronder afgebeeld. 

#### Afbeelding 1&2: Freenect, OpenNi2, NITE

[![Pepper1](Pepper122092017.png){:style="width: 300px;"}](Pepper122092017.png)
[![Pepper2](Pepper222092017.png){:style="width: 300px;"}](Pepper222092017.png)

#### Afbeelding 3&4: Kinect SDK

[![Pepper3](Pepper322092017.png){:style="width: 300px;"}](Pepper322092017.png) 
[![Pepper4](Pepper422092017.png){:style="width: 300px;"}](Pepper422092017.png)

#### Afbeelding 5&6: Vitruvius 

[![Pepper5](Pepper522092017.png){:style="width: 300px;"}](Pepper522092017.png)
[![Pepper6](Pepper622092017.png){:style="width: 300px;"}](Pepper622092017.png)
 
#### Afbeelding 7: Test Setup

[![Pepper7](Pepper722092017.png){:style="width: 300px;"}](Pepper722092017.png)

In afbeelding 7 is de test setup voor het identificatieproces van de schouderbewegingen te zien. Wij willen dit realiseren aan de hand van een drietal camera’s: een front camera (Kinect), een camera voor het zijaanzicht en een camera die opnames maakt vanaf de grond. De camera’s voor zijaanzicht en onderaanzicht zijn alleen nodig om te valideren of de Kinect camera voldoende nauwkeurig is. Dit gaan wij handmatig meten. De metingen is voor ons de maatstaf voor de vergelijking. 
Wanneer de Kinect nauwkeurig genoeg is gebleken kunnen we afstappen van de twee extra camera’s en ons volledig richten op het automatisch meten d.m.v. de Kinect.

*Een painful arc is de hoek van een schouderbeweging (zie afbeelding 8) die door schouder patiënten - tijdens het uitvoeren van deze beweging - als pijnlijk beschouwen wordt. Deze hoek kan per patiënt verschillen. Hierdoor is het zaak om (nauwkeurig) te achterhalen waar deze hoek zich precies bevindt tijdens het bewegen van de schouder. 

#### Afbeelding 8: De schouderbewegingen om de painful arc te identificeren. 

![schouderoefening](https://upload.wikimedia.org/wikipedia/commons/thumb/8/85/Body_Movements_I.jpg/506px-Body_Movements_I.jpg "Schouderoefening") 

---

## 8 sept 2017
We zijn nu twee weken met veel enthousiasme bezig! Ons team bestaat uit een docent en 7 studenten met verschillende achtergronden (Informatica, Bedrijfskunde, Bedrijfskundige Informatica, Toegepaste Wiskunde). Om voor onszelf tot een haalbare doelstelling te komen, focussen we ons op het schoudergewricht. We willen dus onderzoeken of een pepper robot de oefeningen kan monitoren die patiënten na een schouderoperatie moeten uitvoeren.

De pepper robot is voorzien van een diepte camera die gebruikt maakt van de Intel RealSense libraries. Uit de literatuur weten we ondertussen dat het met vergelijkbare hardware (Kinect) mogelijk is om voldoende naukeurige beelden op te nemen. De standaard software die de Kinect aan boord heeft lijkt op dit punt wel verder ontwikkeld dan de RealSense software. Dat is dus een punt van aandacht.
Aangezien deze literatuur gebruik maakt van skeleton functies, die van een persoon een draadmannetje maken, focust ons onderzoek ons op dit moment op twee punten:
1. Het zoeken naar openbaar beschikbare skeleton algoritmes.
1. Het opnemen van testbeelden en hier handmatig metingen aan proberen te doen.

We hebben ondertussen skeleton algoritmes gevonden, en zijn bezig die op onze eigen systemen te proberen te compileren. [Hier](https://forum.openframeworks.cc/t/openni-skeleton-tracking/5125/2) is een voorbeeld op internet van een van de gevonden algoritmes. Zover proberen wij dus ook te komen.

Wij hebben met een los aangeschafte Realsense camera (dus nog even zonder Pepper robot eromheen) beelden kunnen opnemen. We zien dat de resolutie van de beelden niet direct zo goed is dat we overtuigd zijn dat metingen betrouwbaar zullen zijn. We zijn dus aan het experimenteren met verschillende instellingen. 
Hier twee voorbeelden. Op het eerste voorbeeld een opname op 1 meter afstand.


[![op 1 meter](1meter1frames.jpg){:style="width: 300px;"}](1meter1frames.jpg)


Op het tweede voorbeeld was de afstand 3 meter, en zijn om een beter beeld te krijgen 10 frames samengenomen.


[![op 3 meter, 10 frames](3meter10frames.jpg){:style="width: 300px;"}](3meter10frames.jpg)
