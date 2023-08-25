

Tehtäväpohjassa on edellisessä esimerkissä rakennettu arvosanojen tallentamiseen tarkoitettu ohjelma. Tässä tehtävässä täydennät luokkaa `Arvosanarekisteri` siten, että se tarjoaa toiminnallisuuden arvosanojen ja koepisteiden keskiarvon laskemiseen.


<h2>Arvosanojen keskiarvo</h2>

Lisää luokalle `Arvosanarekisteri` metodi `public double arvosanojenKeskiarvo()`, joka palauttaa arvosanojen keskiarvon. Mikäli arvosanarekisterissä ei ole yhtäkään arvosanaa, tulee metodin palauttaa luku `-1`.  Laske arvosanojen keskiarvo `arvosanat`-listaa hyödyntäen.

Käyttöesimerkki:

```java
Arvosanarekisteri rekisteri = new Arvosanarekisteri();
rekisteri.lisaaArvosanaPisteidenPerusteella(93);
rekisteri.lisaaArvosanaPisteidenPerusteella(91);
rekisteri.lisaaArvosanaPisteidenPerusteella(92);
rekisteri.lisaaArvosanaPisteidenPerusteella(88);

System.out.println(rekisteri.arvosanojenKeskiarvo());
```

<sample-output>

4.75

</sample-output>



<h2>Koepisteiden keskiarvo</h2>

Lisää luokalle `Arvosanarekisteri` uusi oliomuuttuja lista, johon lisäät koepisteitä aina kun luokkaa käyttävä ohjelma kutsuu metodia `lisaaArvosanaPisteidenPerusteella`. Lisää tämän jälkeen luokalle metodi `public double koepisteidenKeskiarvo()`, joka laskee ja palauttaa koepisteiden keskiarvon. Mikäli arvosanarekisteriin ei ole lisätty yhtäkään koepistettä, tulee metodin palauttaa luku `-1`.

Käyttöesimerkki:

```java
Arvosanarekisteri rekisteri = new Arvosanarekisteri();
rekisteri.lisaaArvosanaPisteidenPerusteella(93);
rekisteri.lisaaArvosanaPisteidenPerusteella(91);
rekisteri.lisaaArvosanaPisteidenPerusteella(92);

System.out.println(rekisteri.koepisteidenKeskiarvo());
```

<sample-output>

92.0

</sample-output>


<h2>Tulostukset käyttöliittymään</h2>

Lisää lopulta edellä toteutetut metodit osaksi käyttöliittymää. Kun sovellus tulostaa arvosanajakauman, tulee sovelluksen tulostaa myös pisteiden ja arvosanojen keskiarvo.

<sample-output>

Syötä koepisteet: **82**
Syötä koepisteet: **83**
Syötä koepisteet: **96**
Syötä koepisteet: **51**
Syötä koepisteet: **48**
Syötä koepisteet: **56**
Syötä koepisteet: **61**
Syötä koepisteet:

5: \*
4: \*\*
3:
2: \*
1: \*\*
0: \*
Koepisteiden keskiarvo: 68.14285714285714
Arvosanojen keskiarvo: 2.4285714285714284

</sample-output>

