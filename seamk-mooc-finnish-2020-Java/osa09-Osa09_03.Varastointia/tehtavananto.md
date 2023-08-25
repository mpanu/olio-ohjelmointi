


Tehtäväpohjassa tulee mukana luokka `Varasto`, jonka tarjoamat konstruktorit ja metodit ovat seuraavat:



- **public Varasto(double tilavuus)** - Luo tyhjän varaston, jonka vetoisuus eli tilavuus annetaan parametrina; sopimaton tilavuus (<=0) luo käyttökelvottoman varaston, jonka tilavuus on 0.

- **public double getSaldo()** - Palauttaa arvonaan varaston saldon, eli varastossa olevan tavaran tilavuuden.

- **public double getTilavuus()** - Palauttaa arvonaan varaston kokonaistilavuuden (eli sen, joka annettiin konstruktorille).

- **public double paljonkoMahtuu()** - Palauttaa arvonaan tiedon, paljonko varastoon vielä mahtuu.

- **public void lisaaVarastoon(double maara)** - Lisää varastoon pyydetyn määrän; jos määrä on negatiivinen, mikään ei muutu, jos kaikki pyydetty ei enää mahdu, varasto laitetaan täydeksi ja loput määrästä "heitetään menemään", "vuotaa yli".

- **public double otaVarastosta(double maara)** - Otetaan varastosta pyydetty määrä, metodi palauttaa paljonko **saadaan**. Jos pyydetty määrä on negatiivinen, mikään ei muutu ja palautetaan nolla. Jos pyydetään enemmän kuin varastossa on, annetaan mitä voidaan ja varasto tyhjenee.

- **public String toString()** - Palauttaa olion tilan merkkijonoesityksenä tyyliin `saldo = 64.5, tilaa 123.5`


Tehtävässä rakennetaan `Varasto`-luokasta useampia erilaisia varastoja.


<h2>Tuotevarasto, vaihe 1</h2>

Luokka `Varasto` hallitsee tuotteen määrään liittyvät toiminnot. Nyt tuotteelle halutaan lisäksi tuotenimi ja nimen käsittelyvälineet. **Ohjelmoidaan Tuotevarasto Varaston aliluokaksi!** Toteutetaan ensin pelkkä yksityinen oliomuuttuja tuotenimelle, konstruktori ja getteri nimikentälle:

- **public Tuotevarasto(String tuotenimi, double tilavuus)** - Luo tyhjän tuotevaraston. Tuotteen nimi ja varaston tilavuus annetaan parametrina.

- **public String getNimi()** - Palauttaa arvonaan tuotteen nimen.


*Muista millä tavoin konstruktori voi ensi toimenaan suorittaa yliluokan konstruktorin!*


Käyttöesimerkki:


```java
Tuotevarasto mehu = new Tuotevarasto("Juice", 1000.0);
mehu.lisaaVarastoon(1000.0);
mehu.otaVarastosta(11.3);
System.out.println(mehu.getNimi()); // Juice
System.out.println(mehu);           // saldo = 988.7, tilaa 11.3
```

<sample-output>
Juice
saldo = 988.7, vielä tilaa 11.3
</sample-output>


<h2>Tuotevarasto, vaihe 2</h2>


Kuten edellisestä esimerkistä näkee, Tuotevarasto-olion perimä `toString()` ei tiedä (tietenkään!) mitään tuotteen nimestä. *Asialle on tehtävä jotain!* Lisätään samalla myös setteri tuotenimelle:


- **public void setNimi(String uusiNimi)** - asettaa tuotteelle uuden nimen.

- **public String toString()** - palauttaa olion tilan merkkijonoesityksenä tyyliin `Juice: saldo = 64.5, tilaa 123.5`


Uuden `toString()`-metodin voisi toki ohjelmoida käyttäen yliluokalta perittyjä gettereitä, joilla perittyjen, mutta piilossa pidettyjen kenttien arvoja saa käyttöönsä. Koska yliluokkaan on kuitenkin jo ohjelmoitu tarvittava taito varastotilanteen merkkiesityksen tuottamiseen, miksi nähdä vaivaa sen uudelleen ohjelmointiin. Käytä siis hyväksesi perittyä `toString`iä.


*Muista miten korvattua metodia voi kutsua aliluokassa!*


Käyttöesimerkki:


```java
Tuotevarasto mehu = new Tuotevarasto("Juice", 1000.0);
mehu.lisaaVarastoon(1000.0);
mehu.otaVarastosta(11.3);
System.out.println(mehu.getNimi()); // Juice
mehu.lisaaVarastoon(1.0);
System.out.println(mehu);           // Juice: saldo = 989.7, tilaa 10.299999999999955
```

<sample-output>

Juice
Juice: saldo = 989.7, tilaa 10.299999999999955

</sample-output>


<h2>Muutoshistoria</h2>


Toisinaan saattaa olla kiinnostavaa tietää, millä tavoin jonkin tuotteen varastotilanne muuttuu: onko varasto usein hyvin vajaa, ollaanko usein ylärajalla, onko vaihelu suurta vai pientä, jne. Varustetaan siksi `Tuotevarasto`-luokka taidolla muistaa tuotteen määrän muutoshistoriaa.


Aloitetaan apuvälineen laadinnalla.


Muutoshistorian muistamisen voisi toki toteuttaa suoraankin `ArrayList<Double>`-oliona luokassa *Tuotevarasto*, mutta nyt laaditaan kuitenkin oma *erikoistettu väline* tähän tarkoitukseen. Väline tulee toteuttaa kapseloimalla `ArrayList<Double>`-olio.


`Muutoshistoria`-luokan julkiset konstruktorit ja metodit:


- **public Muutoshistoria()** luo tyhjän `Muutoshistoria`-olion.

- **public void lisaa(double tilanne)** lisää muutoshistorian viimeisimmäksi muistettavaksi määräksi parametrina annetun tilanteen.

- **public void nollaa()** tyhjää muistin.

- **public String toString()** palauttaa muutoshistorian merkkijonoesityksen. *ArrayList-luokan antama merkkijonoesitys kelpaa sellaisenaan.*


<h2>Muutoshistoria, vaihe 2</h2>

Täydennä `Muutoshistoria`-luokkaa analyysimetodein:


- **public double maxArvo()** palauttaa muutoshistorian suurimman arvon. Jos historia on tyhjä, metodi palauttaa nollan.

- **public double minArvo()** palauttaa muutoshistorian pienimmän arvon. Jos historia on tyhjä, metodi palauttaa nollan.

- **public double keskiarvo()** palauttaa muutoshistorian arvojen keskiarvon. Jos historia on tyhjä, metodi palauttaa nollan.


Metodien ei tule muokata sisäisen listan järjestystä.


<h2>Muistava tuotevarasto, vaihe 1</h2>

Toteuta luokan `Tuotevarasto` aliluokkana `MuistavaTuotevarasto`. Uusi versio tarjoaa vanhojen lisäksi varastotilanteen muutoshistoriaan liittyviä palveluita. Historiaa hallitaan `Muutoshistoria`-oliolla.

Julkiset konstruktorit ja metodit:

- **public MuistavaTuotevarasto(String tuotenimi, double tilavuus, double alkuSaldo)**	luo tuotevaraston. Tuotenimi, vetoisuus ja alkusaldo annetaan parametrina.
Aseta alkusaldo sekä varaston alkusaldoksi että muutoshistorian ensimmäiseksi arvoksi.

- **public String historia()** palauttaa tuotehistorian tyyliin `[0.0, 119.2, 21.2]`.  Käytä Muutoshistoria-olion merkkiesitystä sellaisenaan.


**Huomaa** että tässä esiversiossa historia ei vielä toimi kunnolla; nyt vasta vain aloitussaldo muistetaan.


Käyttöesimerkki:


```java
// tuttuun tapaan:
MuistavaTuotevarasto mehu = new MuistavaTuotevarasto("Juice", 1000.0, 1000.0);
mehu.otaVarastosta(11.3);
System.out.println(mehu.getNimi()); // Juice
mehu.lisaaVarastoon(1.0);
System.out.println(mehu);           // Juice: saldo = 989.7, vielä tilaa 10.3

// jne

// mutta vielä historia() ei toimi kunnolla:
System.out.println(mehu.historia()); // [1000.0]
// saadaan siis vasta konstruktorin asettama historian alkupiste...
```

<sample-output>
Juice
Juice: saldo = 989.7, vielä tilaa 10.299999999999955
[1000.0]
</sample-output>


<h2>Muistava tuotevarasto, vaihe 2</h2>


*On aika aloittaa historia!* Ensimmäinen versio ei historiasta tiennyt kuin alkupisteen. Täydennä luokkaa metodein


- **public void lisaaVarastoon(double maara)** toimii kuin *Varasto*-luokan metodi, mutta muuttunut tilanne kirjataan historiaan.**Huom:** historiaan tulee kirjata lisäyksen jälkeinen varastosaldo, ei lisättävää määrää!

- **public double otaVarastosta(double maara)** toimii kuin `Varasto`-luokan metodi, mutta muuttunut tilanne kirjataan historiaan. **Huom:** historiaan tulee kirjata poiston jälkeinen varastosaldo, ei poistettavaa määrää!


Käyttöesimerkki:


```java
// tuttuun tapaan:
MuistavaTuotevarasto mehu = new MuistavaTuotevarasto("Juice", 1000.0, 1000.0);
mehu.otaVarastosta(11.3);
System.out.println(mehu.getNimi()); // Juice
mehu.lisaaVarastoon(1.0);
System.out.println(mehu);           // Juice: saldo = 989.7, vielä tilaa 10.3

// jne

// mutta nyt on historiaakin:
System.out.println(mehu.historia()); // [1000.0, 988.7, 989.7]
```

<sample-output>
Juice
Juice: saldo = 989.7, vielä tilaa 10.299999999999955
[1000.0, 988.7, 989.7]
</sample-output>


*Muista miten korvaava metodi voi käyttää hyväkseen korvattua metodia!*



<h2>Muistava tuotevarasto, vaihe 3</h2>


Täydennä luokkaa metodilla


- **public void tulostaAnalyysi()**, joka tulostaa tuotteeseen liittyviä historiatietoja esimerkin esittämään tapaan.


Käyttöesimerkki:


```java
MuistavaTuotevarasto mehu = new MuistavaTuotevarasto("Juice", 1000.0, 1000.0);
mehu.otaVarastosta(11.3);
mehu.lisaaVarastoon(1.0);
//System.out.println(mehu.historia()); // [1000.0, 988.7, 989.7]

mehu.tulostaAnalyysi();
```

<sample-output>

Tuote: Juice
Historia: [1000.0, 988.7, 989.7]
Suurin tuotemäärä: 1000.0
Pienin tuotemäärä: 988.7
Keskiarvo: 992.8

</sample-output>


