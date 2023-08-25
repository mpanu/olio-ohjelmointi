

Tehtävässä käsitellään CSV-muodossa tallennettuja urheilutilastoja. Tiedosto sisältää pilkulla erotettuna kotijoukkeen, vierasjoukkueen, kotijoukkueen pisteet, sekä vierasjoukkueen pisteet.

Alla on esimerkki tiedon sisällöstä. Alla oleva tiedosto on tallennettuna myös tehtäväpohjaan nimellä "data.csv".

<sample-data>

ENCE,Vitality,9,16
ENCE,Vitality,16,12
ENCE,Vitality,9,16
ENCE,Heroic,10,16
SJ,ENCE,0,16
SJ,ENCE,3,16
FURIA,NRG,7,16
FURIA,Prospects,16,1

</sample-data>

Kirjoita ohjelma, joka kysyy käyttäjältä tiedoston nimeä, jonka jälkeen ohjelma lukee tiedostosta ottelutilastot. Tämän jälkeen ohjelma kysyy käyttäjältä joukkueen nimeä, ja tulostaa joukkueeseen liittyen seuraavissa osissa määritellyt tiedot.


<h2>Otteluiden määrä</h2>

Toteuta ohjelmaan mahdollisuus annetun joukkueen otteluiden lukumäärän tulostamiseen. Alla olevassa esimerkissä käytetään edellä kuvattua **data.csv**-tiedostoa.

<sample-output>

Minkä niminen tiedosto luetaan?
**data.csv**
Minkä nimisen joukkueen tiedot tulostetaan?
**FURIA**
Otteluita: 2

</sample-output>


<sample-output>

Minkä niminen tiedosto luetaan?
**data.csv**
Minkä nimisen joukkueen tiedot tulostetaan?
**ENCE**
Otteluita: 6

</sample-output>


<h2>Voittojen ja tappioiden määrä</h2>

Lisää ohjelmaan toiminnallisuus annetun joukkueen voittojen ja tappioiden määrän tulostamiseen. Voittaja on se joukkue, joka saa ottelussa enemmän pisteitä.

Voit olettaa, ettei pelit pääty koskaan tasapeliin. Alla olevassa esimerkissä käytetään edellä kuvattua **data.csv**-tiedostoa.


<sample-output>

Minkä niminen tiedosto luetaan?
**data.csv**
Minkä nimisen joukkueen tiedot tulostetaan?
**FURIA**
Otteluita: 2
Voittoja: 1
Tappioita: 1

</sample-output>


<sample-output>

Minkä niminen tiedosto luetaan?
**data.csv**
Minkä nimisen joukkueen tiedot tulostetaan?
**ENCE**
Otteluita: 6
Voittoja: 3
Tappioita: 3

</sample-output>



