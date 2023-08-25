

Tässä tehtävässä tehdään ohjelma, joka tarjoaa käyttäjälle mahdollisuuden reseptien hakuun reseptin nimen, keittoajan tai raaka-aineen nimen perusteella. Ohjelman tulee lukea reseptit käyttäjän antamasta tiedostosta. *Kannattaa kerrata tiedoston lukeminen materiaalin osasta 4 ennen tehtävän aloitusta.*

Jokainen resepti koostuu kolmesta tai useammasta rivistä reseptitiedostossa. Ensimmäisellä rivillä on reseptin nimi, toisella rivillä reseptin keittoaika (kokonaisluku), ja kolmas ja sitä seuraavat rivit kertovat reseptin raaka-aineet. Reseptin raaka-aineiden kuvaus päättyy tyhjään riviin. Tiedostossa voi olla useampia reseptejä. Alla kuvattuna esimerkkitiedosto.

<sample-output>

Lettutaikina
60
maito
muna
jauho
sokeri
suola
voi

Lihapullat
20
jauheliha
muna
korppujauho

Tofurullat
30
tofu
riisi
vesi
porkkana
kurkku
avokado
wasabi

</sample-output>

Ohjelma toteutetaan osissa. Ensin ohjelmaan luodaan mahdollisuus reseptien lukemiseen sekä listaamiseen. Tämän jälkeen ohjelmaan lisätään mahdollisuus reseptien hakemiseen nimen perusteella, keittoajan perusteella ja lopulta raaka-aineen perusteella.

Tehtäväpohjassa on mukana tiedosto `reseptit.txt`, jota voi käyttää sovelluksen testaamiseen. <em>Huomaa, että ohjelman ei tule listata reseptien raaka-aineita, mutta niitä käytetään hakutoiminnallisuudessa.</em> Tiedoston `reseptit.txt` voi myös ladata [tämän linkin takaa](/data/reseptit.txt).

<br/>


<h2>Reseptien lukeminen ja listaaminen</h2>

Luo ohjelmaan ensin mahdollisuus reseptien lukemiseen sekä listaamiseen. Ohjelman käyttöliittymän tulee olla seuraavanlainen. Voit olettaa, että käyttäjä syöttää aina tiedoston, joka on olemassa. Alla oletetaan, että tehtävänannossa annetut esimerkkireseptit ovat tiedostossa `reseptit.txt`.

<sample-output>

Mistä luetaan? **reseptit.txt**

Komennot:
listaa - listaa reseptit
lopeta - lopettaa ohjelman

Syötä komento: **listaa**

Reseptit:
Lettutaikina, keittoaika: 60
Lihapullat, keittoaika: 20
Tofurullat, keittoaika: 30

Syötä komento:  **lopeta**

</sample-output>


<h2>Reseptien hakeminen nimen perusteella</h2>

Lisää ohjelmaan mahdollisuus reseptien hakemiseen nimen perusteella. Nimen perusteella hakeminen tapahtuu komennolla `hae nimi`, jonka jälkeen käyttäjältä kysytään merkkijonoa, jota etsitään reseptin nimistä. Hakutoiminnallisuuden tulee toimia siten, että se tulostaa kaikki ne reseptit, joiden nimessä esiintyy käyttäjän kirjoittama merkkijono.

<sample-output>

Mistä luetaan? **reseptit.txt**

Komennot:
listaa - listaa reseptit
lopeta - lopettaa ohjelman
hae nimi - hakee reseptiä nimen perusteella

Syötä komento: **listaa**

Reseptit:
Lettutaikina, keittoaika: 60
Lihapullat, keittoaika: 20
Tofurullat, keittoaika: 30

Syötä komento: **hae nimi**
Mitä haetaan: **rulla**

Reseptit:
Tofurullat, keittoaika: 30

Syötä komento:  **lopeta**

</sample-output>


<h2>Reseptien hakeminen keittoajan perusteella</h2>

Lisää seuraavaksi ohjelmaan mahdollisuus reseptien hakemiseen keittoajan perusteella. Keittoajan perusteella hakeminen tapahtuu komennolla `hae keittoaika`, jonka jälkeen käyttäjältä kysytään suurinta hyväksyttävää keittoaikaa. Hakutoiminnallisuuden tulee toimia siten, että se tulostaa kaikki ne reseptit, joiden keittoaika on pienempi tai yhtä suuri kuin käyttäjän syöttämä keittoaika.

<sample-output>

Mistä luetaan? **reseptit.txt**

Komennot:
listaa - listaa reseptit
lopeta - lopettaa ohjelman
hae nimi - hakee reseptiä nimen perusteella
hae keittoaika - hakee reseptiä keittoajan perusteella

Syötä komento: **hae keittoaika**
Keittoaika korkeintaan: **30**

Reseptit:
Lihapullat, keittoaika: 20
Tofurullat, keittoaika: 30

Syötä komento: **hae keittoaika**
Keittoaika korkeintaan: **15**

Reseptit:

Syötä komento: **hae nimi**
Mitä haetaan: **rulla**

Reseptit:
Tofurullat, keittoaika: 30

Syötä komento:  **lopeta**

</sample-output>


<h2>Reseptien hakeminen raaka-aineen perusteella</h2>


Lisää lopulta ohjelmaan mahdollisuus reseptien hakemiseen raaka-aineen perusteella. Raaka-aineen perusteella hakeminen tapahtuu komennolla `hae aine`, jonka jälkeen käyttäjältä kysytään merkkijonoa. Hakutoiminnallisuuden tulee toimia siten, että se tulostaa kaikki ne reseptit, joiden raaka-aineissa esiintyy käyttäjän antama merkkijono. Huomaa, että tässä annetun merkkijonon täytyy vastata täysin haettua raaka-ainetta (esim. "okeri" ei käy ole sama kuin "sokeri").


<sample-output>

Mistä luetaan? **reseptit.txt**

Komennot:
listaa - listaa reseptit
lopeta - lopettaa ohjelman
hae nimi - hakee reseptiä nimen perusteella
hae keittoaika - hakee reseptiä keittoajan perusteella
hae aine - hakee reseptiä raaka-aineen perusteella

Syötä komento: **hae keittoaika**
Keittoaika korkeintaan: **30**

Reseptit:
Lihapullat, keittoaika: 20
Tofurullat, keittoaika: 30

Syötä komento: **hae aine**
Mitä raaka-ainetta haetaan: **sokeri**

Reseptit:
Lettutaikina, keittoaika: 60

Syötä komento: **hae aine**
Mitä raaka-ainetta haetaan: **muna**

Reseptit:
Lettutaikina, keittoaika: 60
Lihapullat, keittoaika: 20

Syötä komento: **hae aine**
Mitä raaka-ainetta haetaan: **una**

Reseptit:

Syötä komento:  **lopeta**

</sample-output>

