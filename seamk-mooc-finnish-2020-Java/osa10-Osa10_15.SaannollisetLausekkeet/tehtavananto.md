

Harjoitellaan hieman säännöllisten lausekkeiden käyttöä. Tehtävissä haetut metodit tehdään luokkaan `Tarkistin`.


<h2>Viikonpäivä</h2>

Tee säännöllisen lausekkeen avulla metodi `public boolean onViikonpaiva(String merkkijono)`, joka palauttaa `true` jos sen parametrina saama merkkijono on viikonpäivän lyhenne (ma, ti, ke, to, pe, la tai su).

Esimerkkitulostuksia metodia käyttävästä ohjelmasta:

<sample-output>

Anna merkkijono: **ti**
Muoto on oikea.

</sample-output>

<sample-output>

Anna merkkijono: **abc**
Muoto ei ole oikea.

</sample-output>


<h2>Vokaalitarkistus</h2>

Tee metodi `public boolean kaikkiVokaaleja(String merkkijono)` joka tarkistaa säännöllisen lausekkeen avulla ovatko parametrina olevan merkkijonon kaikki merkit vokaaleja.

Esimerkkitulostuksia metodia käyttävästä ohjelmasta:

<sample-output>

Anna merkkijono: **aie**
Muoto on oikea.

</sample-output>

<sample-output>

Anna merkkijono: **ane**
Muoto ei ole oikea.

</sample-output>


<h2>Kellonaika</h2>


Säännölliset lausekkeet sopivat tietynlaisiin tilanteisiin. Joissain tapaukseesa lausekkeista tulee liian monimutkaisia, ja merkkijonon "sopivuus" kannattaa tarkastaa muulla tyylillä tai voi olla tarkoituksenmukaista käyttää säännöllisiä lausekkeita vain osaan tarkastuksesta.

Tee  metodi `public boolean kellonaika(String merkkijono)`  ohjelma, joka tarkistaa säännöllisen lausekkeen avulla onko parametrina oleva merkkijono muotoa `tt:mm:ss` oleva kellonaika (tunnit, minuutit ja sekunnit kaksinumeroisina).

Esimerkkitulostuksia metodia käyttävästä ohjelmasta:

<sample-output>

Anna merkkijono: **17:23:05**
Muoto on oikea.

</sample-output>

<sample-output>

Anna merkkijono: **abc**
Muoto ei ole oikea.

</sample-output>

<sample-output>

Anna merkkijono: **33:33:33**
Muoto ei ole oikea.

</sample-output>

