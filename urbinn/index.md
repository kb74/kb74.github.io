# Project Urbinn

[![Urbinn](urbinn.png){:style="float: right; width: 300px;"}](urbinn.png)
Binnen het project Urbinn wordt een duurzame zelfrijdende stadsauto ontwikkeld door een samenwerkingsverband van o.a. de Betafactory, Accenda, het lectoraat Smart Sensor Systems, 6 faculteiten van de HHS, TU Delft en Accenda. De bijdrage aan Urbinn vanuit KB-74 is om camera beelden te gebruiken om de exacte positie en richting van de auto te bepalen en vaste en bewegende obstakels te classificeren zodat deze informatie in een vervolgtraject kan worden gebruikt om het autonoom rijden te onderzoeken.

Milestone 1 - Orientatie project
----------

In de eerste week hebben we ons georienteerd op de opdracht. Voor een inschatting van de locatie en het mappen van de omgeving worden Simultaneous Localization and Mapping (SLAM) algoritmes gebruikt. Die kunnen werken met verschillende sensoren zoals LIDAR, SONAR, aucoustisch en/of camera beelden. Omdat we in een volgende stap moeten herkennen wat het object is lijken camera beelden in ieder geval nodig. Bij het verkennen van SLAM-algoritmes blijken stereo camera beelden behoorlijk acurate resultaten op te leveren in real-time.

Er bestaan veel verschillende SLAM-algoritmes, die in veel gevallen het resultaat zijn van wetenschappelijk onderzoek. Op de site van de [KITTI Dataset](http://www.cvlibs.net/datasets/kitti/eval_odometry.php) staat een vergelijking van de verschillende algoritmes. We hebben een vooropige selectie gemaakt van de meest interessante algoritmes op basis van de resultaten, kwaliteit van de beschrijving, de beschikbaarheid van open source en de mate van ondersteuning. Voorlopig gaan we aan de slag met [SVO](https://www.google.nl/url?sa=t&rct=j&q=&esrc=s&source=web&cd=3&cad=rja&uact=8&ved=0ahUKEwjb_Z26m5PWAhXNZVAKHRQmBBAQFgg4MAI&url=http%3A%2F%2Frpg.ifi.uzh.ch%2Fdocs%2FICRA14_Forster.pdf&usg=AFQjCNH7yos-_jmOo3WUp8tUGLP-z9Jppw) en [ORB2](https://arxiv.org/abs/1610.06475).

Een voorbeeld van ORB2 SLAM op de KITTI Dataset (klik voor video) [![ORB2 SLAM op KITTI Dataset](https://i.ytimg.com/vi/sr9H3ZsZCzc/maxresdefault.jpg)](https://www.youtube.com/watch?v=8DISRmsO2YQ)


Milestone 2 - ORB localization gang Slinger/Kitti
----------

In week 3 zijn we begonnen met het maken van de eigen dataset gebasseerd op the gang (Slinger) van de Haagse Hogeschool. Onze milesstone is dat voor het einde van sprint 2 het mogelijk is om middels onze eigen dataset of de KITTI dataset (http://www.cvlibs.net/datasets/kitti/) in te kunnen laden in het ORB-SLAM2 algoritme.
ORB-SLAM2 is inmiddels geinstalleerd op de server waarmee we de eerste testen hebben gedraaid. Daarnaast zijn er twee nieuwe groepsleden toegevoegd aan het Urbinn project die het totaal aantal leden op 10 brengt. We experimenteren met verschillende soorten camera's om te bepalen welke settings (fps, resolutie, etc) het beste zijn voor dit project. 
Ook is het inmiddels mogelijk om de pointcloude van de map op te slaan waarmee het mogelijk moet worden om een semantische map van de omgeving te kunnen maken. Tot slot is er gewerkt aan de juiste kalibratie van de camera's.   