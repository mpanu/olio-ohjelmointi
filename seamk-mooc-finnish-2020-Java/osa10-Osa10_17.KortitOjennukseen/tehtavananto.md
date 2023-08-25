

Tehtäväpohjan mukana on luokka, jonka oliot kuvaavat pelikortteja. Kortilla on arvo ja maa. Kortin arvo on esitetään numerona *2, 3, ..., 14* ja maa *Risti, Ruutu, Hertta* tai *Pata*. Ässä on siis arvo 14. Arvo esitetään kokonaislukuna ja maa enum-tyyppisenä oliona. Kortilla on myös metodi toString, jota käyttäen kortin arvo ja maa tulostuvat "ihmisystävällisesti".

Korttien luominen tapahtuu seuraavasti.


```java
Kortti eka = new Kortti(2, Maa.RUUTU);
Kortti toka = new Kortti(14, Maa.PATA);
Kortti kolmas = new Kortti(12, Maa.HERTTA);

System.out.println(eka);
System.out.println(toka);
System.out.println(kolmas);
```

Tulostuu:

<sample-output>

RUUTU 2
PATA A
HERTTA Q

</sample-output>


<h2>Kortti-luokasta Comparable</h2>

Tee Kortti-luokasta `Comparable`. Toteuta `compareTo`-metodi niin, että korttien järjestys on arvon mukaan nouseva. Jos verrattavien Korttien arvot ovat samat, verrataan niitä maan perusteella nousevassa järjestyksessä: *risti ensin, ruutu toiseksi, hertta kolmanneksi, pata viimeiseksi.*

Maiden järjestämisessä apua löytynee <a href="https://docs.oracle.com/javase/8/docs/api/java/lang/Enum.html#ordinal--"  target="_blank" norel>Enum-luokan ordinal-metodista</a>.

Järjestyksessä pienin kortti siis olisi ristikakkonen ja suurin pataässä.


<h2>Käsi</h2>

Tee seuraavaksi luokka `Kasi` joka edustaa pelaajan kädessään pitämää korttien joukkoa. Tee kädelle seuraavat metodit:

- `public void lisaa(Kortti kortti)` lisää käteen kortin
- `public void tulosta()` tulostaa kädessä olevat kortit alla olevan esimerkin tyylillä


```java
Kasi kasi = new Kasi();

kasi.lisaa(new Kortti(2, Maa.RUUTU));
kasi.lisaa(new Kortti(14, Maa.PATA));
kasi.lisaa(new Kortti(12, Maa.HERTTA));
kasi.lisaa(new Kortti(2, Maa.PATA));

kasi.tulosta();
```

Tulostuu:

<sample-output>

RUUTU 2
PATA A
HERTTA Q
PATA 2

</sample-output>

Käytä ArrayListiä korttien tallentamiseen.


<h2>Käden järjestäminen</h2>

Tee kädelle metodi `public void jarjesta()` jota kutsumalla käden sisällä olevat kortit menevät suuruusjärjestykseen. Järjestämisen jälkeen kortit tulostuvat järjestyksessä:

```java
Kasi kasi = new Kasi();

kasi.lisaa(new Kortti(2, Maa.RUUTU));
kasi.lisaa(new Kortti(14, Maa.PATA));
kasi.lisaa(new Kortti(12, Maa.HERTTA));
kasi.lisaa(new Kortti(2, Maa.PATA));

kasi.jarjesta();

kasi.tulosta();
```

Tulostuu:

<sample-output>

RUUTU 2
PATA 2
HERTTA Q
PATA A

</sample-output>


<h2>Käsien vertailu</h2>


Eräässä korttipelissä kahdesta korttikädestä arvokkaampi on se, jonka sisältämien korttien arvon summa on suurempi. Tee luokasta `Kasi` vertailtava tämän kriteerin mukaan, eli laita luokka toteuttamaan rajapinta `Comparable<Kasi>`.

Esimerkkiohjelma, jossa vertaillaan käsiä:


```java
Kasi kasi1 = new Kasi();

kasi1.lisaa(new Kortti(2, Maa.RUUTU));
kasi1.lisaa(new Kortti(14, Maa.PATA));
kasi1.lisaa(new Kortti(12, Maa.HERTTA));
kasi1.lisaa(new Kortti(2, Maa.PATA));

Kasi kasi2 = new Kasi();

kasi2.lisaa(new Kortti(11, Maa.RUUTU));
kasi2.lisaa(new Kortti(11, Maa.PATA));
kasi2.lisaa(new Kortti(11, Maa.HERTTA));

int vertailu = kasi1.compareTo(kasi2);

if (vertailu < 0) {
    System.out.println("arvokkaampi käsi sisältää kortit");
    kasi2.tulosta();
} else if (vertailu > 0){
    System.out.println("arvokkaampi käsi sisältää kortit");
    kasi1.tulosta();
} else {
    System.out.println("kädet yhtä arvokkaat");
}
```

Tulostuu

<sample-output>

arvokkaampi käsi sisältää kortit
RUUTU J
PATA J
HERTTA J

</sample-output>


<h2>Korttien järjestäminen eri kriteerein</h2>

Entä jos haluaisimme välillä järjestää kortit hieman eri tavalla, esim. kaikki saman maan kortit peräkkäin? Luokalla voi olla vain yksi `compareTo`-metodi, joten joudumme muunlaisia järjestyksiä saadaksemme turvautumaan muihin keinoihin.


Vaihtoehtoiset järjestämistavat toteutetaan erillisten vertailun suorittavien luokkien avulla. Korttien vaihtoehtoisten järjestyksen määräävän luokkien tulee toteuttaa `Comparator<Kortti>`-rajapinta. Järjestyksen määräävän luokan olio vertailee kahta parametrina saamaansa korttia. Metodeja on ainoastaan yksi compare(Kortti k1, Kortti k2), jonka tulee palauttaa negatiivinen arvo, jos kortti k1 on järjestyksessä ennen korttia k2, positiivinen arvo jos k2 on järjestyksessä ennen k1:stä ja 0 muuten.


Periaatteena on luoda jokaista järjestämistapaa varten oma vertailuluokka, esim. saman maan kortit vierekkäin vievän järjestyksen määrittelevä luokka:


```java
import java.util.Comparator;

public class SamatMaatVierekkain implements Comparator<Kortti> {
    public int compare(Kortti k1, Kortti k2) {
        return k1.getMaa().ordinal() - k2.getMaa().ordinal();
    }
}
```

Maittainen järjestys on sama kuin kortin metodin `compareTo` maille määrittelemä järjestys eli *ristit ensin, ruudut toiseksi, hertat kolmanneksi, padat viimeiseksi.*


Järjestäminen tapahtuu edelleen luokan Collections metodin sort avulla. Metodi saa nyt toiseksi parametrikseen järjestyksen määräävän luokan olion:

```java
ArrayList<Kortti> kortit = new ArrayList<>();

kortit.add(new Kortti(3, Maa.PATA));
kortit.add(new Kortti(2, Maa.RUUTU));
kortit.add(new Kortti(14, Maa.PATA));
kortit.add(new Kortti(12, Maa.HERTTA));
kortit.add(new Kortti(2, Maa.PATA));

SamatMaatVierekkain samatMaatVierekkainJarjestaja = new SamatMaatVierekkain();
Collections.sort(kortit, samatMaatVierekkainJarjestaja);

kortit.stream().forEach(k -> System.out.println(k));
```

Tulostuu:

<sample-output>

RUUTU 2
HERTTA Q
PATA 3
PATA A
PATA 2

</sample-output>


Järjestyksen määrittelevä olio voidaan myös luoda suoraan sort-kutsun yhteydessä:


```java
Collections.sort(kortit, new SamatMaatVierekkain());
```

Mikäli luokkaa ei halua toteuttaa, järjestyksen voi antaa `Collections`-luokan `sort`-metodille myös lambda-lausekkeena.


```java
Collections.sort(kortit, (k1, k2) -> k1.getMaa().ordinal() - k2.getMaa().ordinal());
  ```


Tarkempia ohjeita vertailuluokkien tekemiseen <a href="http://leepoint.net/data/collections/comparators.html">täällä</a>


Tee nyt luokka Comparator-rajapinnan toteuttava luokka `SamatMaatVierekkainArvojarjestykseen` jonka avulla saat kortit muuten samanlaiseen järjestykseen kuin edellisessä esimerkissä paitsi, että saman maan kortit järjestyvät arvon mukaisesti.


<h2>Käden järjestäminen maittain</h2>


Lisää luokalle `Kasi` metodi `public void jarjestaMaittain()` jota kutsumalla käden sisällä olevat kortit menevät edellisen tehtävän vertailijan määrittelemään järjestykseen. Järjestämisen jälkeen kortit tulostuvat järjestyksessä:


```java
Kasi kasi = new Kasi();

kasi.lisaa(new Kortti(12, Maa.HERTTA));
kasi.lisaa(new Kortti(4, Maa.PATA));
kasi.lisaa(new Kortti(2, Maa.RUUTU));
kasi.lisaa(new Kortti(14, Maa.PATA));
kasi.lisaa(new Kortti(7, Maa.HERTTA));
kasi.lisaa(new Kortti(2, Maa.PATA));

kasi.jarjestaMaittain();

kasi.tulosta();
```

Tulostuu:

<sample-output>

RUUTU 2
HERTTA 7
HERTTA Q
PATA 2
PATA 4
PATA A

</sample-output>

