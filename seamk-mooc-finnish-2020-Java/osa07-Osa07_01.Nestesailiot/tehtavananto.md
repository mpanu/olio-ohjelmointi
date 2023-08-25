

Toteutetaan interaktiivinen ohjelma kahden nestesäiliön käsittelyyn. Säiliöt ovat nimeltään "ensimmäinen" ja "toinen". Kumpikin voi sisältää korkeintaan sata yksikköä nestettä.

Ohjelma tarjoaa toiminnallisuuden nesteen lisäämiseen, nesteen siirtämiseen, ja nesteen poistamiseen. Nesteen lisääminen lisää nestettä ensimmäiseen säiliöön, nesteen siirtäminen siirtää nestettä ensimmäisestä säiliöstä toiseen ja nesteen poistaminen poistaa nestettä toisesta säiliöstä.

Ohjelman komentojen tulee olla seuraavat:

- `lisaa maara` lisää ensimmäiseen säiliöön parametrina annetun määrän nestettä. Annettu määrä kuvataan kokonaislukuna. Säiliössä ei voi olla yli sataa yksikköä nestettä ja liialliset lisäykset menevät hukkaan.

- `siirra maara` siirtää ensimmäisestä säiliöstä toiseen parametrina annetun määrän nestettä. Annettu määrä kuvataan kokonaislukuna. Säiliössä ei voi olla yli sataa yksikköä nestettä. Mikäli ohjelmassa yritetään siirtää enemmän kuin ensimmäisessä säiliössä on, siirretään ensimmäisen säiliön koko sisältö. Mikäli ohjelmassa yritetään siirtää enemmän kuin toiseen säiliöön mahtuu, valuu toiseen säiliöön mahtumaton osa hukkaan.

- `poista maara` poistaa toisesta säiliöstä parametrina annetun määrän nestettä. Mikäli ohjelmaa pyydetään poistamaan enemmän kuin mitä säiliössä on, poistetaan säiliöstä vain säiliön sisältö.


Jokaisen komennon suorituksen jälkeen tulostetaan säiliöden sisältö. Negatiivisia määriä ei tule ottaa huomioon.

Toteuta ohjelma proseduraalista ohjelmointityyliä noudattaen ilman omia luokkia. Kaikki toiminnallisuus tulee lisätä luokassa `Nestesailiot` olevaan metodiin `main` (älä siis tee omia metodeja). Tehtäväpohjassa on valmiina toistolause, mistä poistutaan kun käyttäjä kirjoittaa "lopeta".

Alla on muistutuksena merkkijonon pilkkominen osiin.


```java
String luettu = lukija.nextLine();
String[] osat = luettu.split(" ");

String komento = osat[0];
int maara = Integer.valueOf(osat[1]);
```


<h2>Lisääminen</h2>

Toteuta toiminnallisuus nesteen lisäämiseen ensimmäiseen säiliöön. Ohjelman toiminnan tulee olla seuraavanlainen:


<sample-output>

Ensimmäinen: 0/100
Toinen: 0/100
**lisaa 5**

Ensimmäinen: 5/100
Toinen: 0/100
**lisaa 25**

Ensimmäinen: 30/100
Toinen: 0/100
**lisaa 60**

Ensimmäinen: 90/100
Toinen: 0/100
**lisaa 1000**

Ensimmäinen: 100/100
Toinen: 0/100
**lisaa -5**

Ensimmäinen: 100/100
Toinen: 0/100
**lopeta**

</sample-output>


<h2>Siirtäminen</h2>

Toteuta toiminnallisuus nesteen siirtämiseen ensimmäisestä säiliöstä toiseen.  Ohjelman toiminnan tulee olla seuraavanlainen:


<sample-output>

Ensimmäinen: 0/100
Toinen: 0/100
**lisaa 1000**

Ensimmäinen: 100/100
Toinen: 0/100
**siirra 50**

Ensimmäinen: 50/100
Toinen: 50/100
**lisaa 100**

Ensimmäinen: 100/100
Toinen: 50/100
**siirra 100**

Ensimmäinen: 0/100
Toinen: 100/100
**lopeta**

</sample-output>


Toinen esimerkki:


<sample-output>

Ensimmäinen: 0/100
Toinen: 0/100
**siirra 30**

Ensimmäinen: 0/100
Toinen: 0/100
**lisaa 10**

Ensimmäinen: 10/100
Toinen: 0/100
**siirra -5**

Ensimmäinen: 10/100
Toinen: 0/100
**siirra 20**

Ensimmäinen: 0/100
Toinen: 10/100
**siirra 10**

Ensimmäinen: 0/100
Toinen: 10/100
**lopeta**

</sample-output>


<h2>Poistaminen</h2>

Toteuta toiminnallisuus nesteen poistamiseen toisesta säiliöstä. Ohjelman toiminnan tulee olla seuraavanlainen:

<sample-output>

Ensimmäinen: 0/100
Toinen: 0/100
**poista 10**

Ensimmäinen: 0/100
Toinen: 0/100
**lisaa 20**

Ensimmäinen: 20/100
Toinen: 0/100
**poista 5**

Ensimmäinen: 20/100
Toinen: 0/100
**siirra 15**

Ensimmäinen: 5/100
Toinen: 15/100
**poista 5**

Ensimmäinen: 5/100
Toinen: 10/100
**poista 20**

Ensimmäinen: 5/100
Toinen: 0/100
**lopeta**

</sample-output>


