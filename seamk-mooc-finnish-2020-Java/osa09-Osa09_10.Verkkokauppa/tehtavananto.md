


Teemme tehtävässä muutamia verkkokaupan hallinnointiin soveltuvia ohjelmakomponentteja.


<h2>Varasto</h2>

Tee luokka Varasto jolla on seuraavat metodit:

- `public void lisaaTuote(String tuote, int hinta, int saldo)` lisää varastoon tuotteen jonka hinta ja varastosaldo ovat parametrina annetut luvut
- `public int hinta(String tuote)` palauttaa parametrina olevan tuotteen hinnan, jos tuotetta ei ole varastossa, palauttaa metodi arvon `-99`.


Varaston sisällä tuotteiden hinnat (ja seuraavassa kohdassa saldot) tulee tallettaa `Map<String, Integer>`-tyyppiseksi määriteltyyn muuttujaan! Luotava olio voi olla tyypiltään `HashMap`, muuttujan tyyppinä on käytettävä `Map`-rajapintaa.


Seuraavassa esimerkki varaston käytöstä:


```java
Varasto varasto = new Varasto();
varasto.lisaaTuote("maito", 3, 10);
varasto.lisaaTuote("kahvi", 5, 7);

System.out.println("hinnat:");
System.out.println("maito: " + varasto.hinta("maito"));
System.out.println("kahvi: " + varasto.hinta("kahvi"));
System.out.println("sokeri: " + varasto.hinta("sokeri"));
```

Tulostuu:


<sample-output>

hinnat:
maito: 3
kahvi: 5
sokeri: -99

</sample-output>


<h2>Tuotteen varastosaldo</h2>


Aseta tuotteiden varastosaldot samaan tapaan `Map<String, Integer>`-tyyppiseen muuttujaan kuin hinnat. Täydennä varastoa seuraavilla metodeilla:


- `public int saldo(String tuote)` palauttaa parametrina olevan tuotteen varastosaldon. Jos tuotetta ei ole varastossa lainkaan, tulee palauttaa 0.
- `public boolean ota(String tuote)` vähentää parametrina olevan tuotteen saldoa yhdellä ja palauttaa *true* jos tuotetta oli varastossa. Jos tuotetta ei ole varastossa, palauttaa metodi *false*, tuotteen saldo ei saa laskea alle nollan.


Esimerkki varaston käytöstä:


```java
Varasto varasto = new Varasto();
varasto.lisaaTuote("kahvi", 5, 1);

System.out.println("saldot:");
System.out.println("kahvi:  " + varasto.saldo("kahvi"));
System.out.println("sokeri: " + varasto.saldo("sokeri"));

System.out.println("otetaan kahvi " + varasto.ota("kahvi"));
System.out.println("otetaan kahvi " + varasto.ota("kahvi"));
System.out.println("otetaan sokeri " + varasto.ota("sokeri"));

System.out.println("saldot:");
System.out.println("kahvi:  " + varasto.saldo("kahvi"));
System.out.println("sokeri: " + varasto.saldo("sokeri"));
```


Tulostuu:


<sample-output>

saldot:
kahvi:  1
sokeri: 0
otetaan kahvi true
otetaan kahvi false
otetaan sokeri false
saldot:
kahvi:  0
sokeri: 0

</sample-output>


<h2>Tuotteiden listaus</h2>


Listätään varastolle vielä yksi metodi:


- `public Set<String> tuotteet()` palauttaa *joukkona* varastossa olevien tuotteiden nimet.


Metodi on helppo toteuttaa HashMapin avulla. Saat tietoon varastossa olevat tuotteet kysymällä ne joko hinnat tai saldot muistavalta Map:iltä metodin `keySet` avulla.


Esimerkki varaston käytöstä:


```java
Varasto varasto = new Varasto();
varasto.lisaaTuote("maito", 3, 10);
varasto.lisaaTuote("kahvi", 5, 6);
varasto.lisaaTuote("piima", 2, 20);
varasto.lisaaTuote("jugurtti", 2, 20);

System.out.println("tuotteet:");

for (String tuote: varasto.tuotteet()) {
    System.out.println(tuote);
}
```

<sample-output>

tuotteet:
piima
jugurtti
kahvi
maito

</sample-output>


<h2>Ostos</h2>


Ostoskoriin lisätään *ostoksia*. Ostoksella tarkoitetaan tiettyä määrää tiettyjä tuotteita. Koriin voidaan laittaa esim. ostos joka vastaa yhtä leipää tai ostos joka vastaa 24:ää kahvia.


Tee luokka `Ostos` jolla on seuraavat toiminnot:


- `public Ostos(String tuote, int kpl, int yksikkohinta)` konstruktori joka luo ostoksen joka vastaa parametrina annettua tuotetta. Tuotteita ostoksessa on *kpl* kappaletta ja yhden tuotteen hinta on kolmantena parametrina annettu *yksikkohinta*
- `public int hinta()` palauttaa ostoksen hinnan. Hinta saadaan kertomalla kappalemäärä yksikköhinnalla
- `public void kasvataMaaraa()` kasvattaa ostoksen kappalemäärää yhdellä
- `public String toString()` palauttaa ostoksen merkkijonomuodossa, joka on alla olevan esimerkin mukainen


Esimerkki ostos-luokan käytöstä:


```java
Ostos ostos = new Ostos("maito", 4, 2);
System.out.println("ostoksen joka sisältää 4 maitoa yhteishinta on " + ostos.hinta());
System.out.println(ostos);
ostos.kasvataMaaraa();
System.out.println(ostos);
```

<sample-output>

ostoksen joka sisältää 4 maitoa yhteishinta on 8
maito: 4
maito: 5

</sample-output>


Huom: *toString* on siis muotoa *tuote: kpl* -- hintaa ei merkkijonoesitykseen tule!


<h2>Ostoskori</h2>


Vihdoin pääsemme toteuttamaan luokan ostoskori!


Ostoskori tallettaa sisäisesti koriin lisätyt tuotteet *Ostos-olioina*. Ostoskorilla tulee olla oliomuuttuja jonka tyyppi on joko `Map<String, Ostos>` tai `List<Ostos>`. Älä laita mitään muita oliomuuttujia ostoskorille kuin ostosten talletukseen tarvittava Map tai List.


Huom: jos talletat Ostos-oliot Map-tyyppiseen apumuuttujaan, on tässä ja seuraavassa tehtävässä hyötyä Map:in metodista values(), jonka avulla on helppo käydä läpi kaikki talletetut ostos-oliot.


Tehdään aluksi ostoskorille parametriton konstruktori ja metodit:


- `public void lisaa(String tuote, int hinta)` lisää ostoskoriin ostoksen joka vastaa parametrina olevaa tuotetta ja jolla on parametrina annettu hinta.
- `public int hinta()` palauttaa ostoskorin kokonaishinnan


Esimerkki ostoskorin käytöstä:


```java
Ostoskori kori = new Ostoskori();
kori.lisaa("maito", 3);
kori.lisaa("piima", 2);
kori.lisaa("juusto", 5);
System.out.println("korin hinta: " + kori.hinta());
kori.lisaa("tietokone", 899);
System.out.println("korin hinta: " + kori.hinta());
```

<sample-output>

korin hinta: 10
korin hinta: 909

</sample-output>


<h2>Ostoskorin tulostus</h2>


Tehdään ostoskorille metodi `public void tulosta()` joka tulostaa korin sisältämät *Ostos*-oliot. Tulostusjärjestyksessä ei ole merkitystä. Edellisen esimerkin ostoskori tulostetuna olisi:


<sample-output>

piima: 1
juusto: 1
tietokone: 1
maito: 1

</sample-output>


Huomaa, että tulostuva numero on siis tuotteen korissa oleva kappalemäärä, ei hinta!


<h2>Yksi ostos tuotetta kohti</h2>


Täydennetään Ostoskoria siten, että jos korissa on jo tuote joka sinne lisätään, ei koriin luoda uutta Ostos-olioa vaan päivitetään jo korissa olevaa tuotetta vastaavaa ostosolioa kutsumalla sen metodia *kasvataMaaraa()*.


Esimerkki:


```java
Ostoskori kori = new Ostoskori();
kori.lisaa("maito", 3);
kori.tulosta();
System.out.println("korin hinta: " + kori.hinta() + "\n");

kori.lisaa("piima", 2);
kori.tulosta();
System.out.println("korin hinta: " + kori.hinta() + "\n");

kori.lisaa("maito", 3);
kori.tulosta();
System.out.println("korin hinta: " + kori.hinta() + "\n");

kori.lisaa("maito", 3);
kori.tulosta();
System.out.println("korin hinta: " + kori.hinta() + "\n");
```

<sample-output>

maito: 1
korin hinta: 3

piima: 1
maito: 1
korin hinta: 5

piima: 1
maito: 2
korin hinta: 8

piima: 1
maito: 3
korin hinta: 11

</sample-output>


Eli ensin koriin lisätään maito ja piimä ja niille omat ostos-oliot. Kun koriin lisätään lisää maitoa, ei luoda uusille maidoille omaa ostosolioa, vaan päivitetään jo korissa olevan maitoa kuvaavan ostosolion kappalemäärää.


<h2>Kauppa</h2>


Nyt meillä on valmiina kaikki osat "verkkokauppaa" varten. Verkkokaupassa on varasto joka sisältää kaikki tuotteet. Jokaista asiakkaan asiointia varten on oma ostoskori. Aina kun asiakas valitsee ostoksen, lisätään se asiakkaan ostoskoriin jos tuotetta on varastossa. Samalla varastosaldoa pienennetään yhdellä.

Seuraavassa on valmiina verkkokaupan tekstikäyttöliittymän runko. Tee projektiin luokka `Kauppa` ja kopioi alla oleva koodi luokkaan.


```java
import java.util.Scanner;

public class Kauppa {

    private Varasto varasto;
    private Scanner lukija;

    public Kauppa(Varasto varasto, Scanner lukija) {
        this.varasto = varasto;
        this.lukija = lukija;
    }

    // metodi jolla hoidetaan yhden asiakkaan asiointi kaupassa
    public void asioi(String asiakas) {
        Ostoskori kori = new Ostoskori();
        System.out.println("Tervetuloa kauppaan " + asiakas);
        System.out.println("valikoimamme:");

        for (String tuote: this.varasto.tuotteet()) {
            System.out.println(tuote);
        }

        while (true) {
            System.out.print("mitä laitetaan ostoskoriin (pelkkä enter vie kassalle):");
            String tuote = lukija.nextLine();
            if (tuote.isEmpty()) {
                break;
            }

            // tee tänne koodi joka lisää tuotteen ostoskoriin jos sitä on varastossa
            // ja vähentää varastosaldoa
            // älä koske muuhun koodiin!

        }

        System.out.println("ostoskorissasi on:");
        kori.tulosta();
        System.out.println("korin hinta: " + kori.hinta());
    }
}
```

Seuraavassa pääohjelma joka täyttää kaupan varaston ja laittaa Pekan asioimaan kaupassa:


```java
Varasto varasto = new Varasto();
varasto.lisaaTuote("kahvi", 5, 10);
varasto.lisaaTuote("maito", 3, 20);
varasto.lisaaTuote("piima", 2, 55);
varasto.lisaaTuote("leipa", 7, 8);

Kauppa kauppa = new Kauppa(varasto, new Scanner(System.in));
kauppa.asioi("Pekka");
```


Kauppa on melkein valmiina. Yhden asiakkaan asioinnin hoitavan metodin `public void asioi(String asiakas)` on kommenteilla merkitty kohta jonka joudut täydentämään. Lisää kohtaan koodi joka tarkastaa onko asiakkaan haluamaa tuotetta varastossa. Jos on, vähennä tuotteen varastosaldoa ja lisää tuote ostoskoriin.


*Todellisuudessa verkkokauppa toteutettaisiin hieman eri tavalla. Verkkosovelluksia tehtäessä käyttöliittymä toteutetaan HTML-sivuna, ja sivuilla tapahtuvat klikkaukset ohjataan palvelinohjelmistolle. Teemaan liittyen löytyy useampia kursseja Helsingin yliopistolta.*

