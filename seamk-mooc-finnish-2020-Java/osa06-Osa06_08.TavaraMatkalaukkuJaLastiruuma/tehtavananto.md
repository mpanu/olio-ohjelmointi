

Tässä tehtäväsarjassa tehdään luokat `Tavara`, `Matkalaukku` ja `Lastiruuma`, joiden avulla harjoitellaan lisää olioita, jotka sisältävät toisia olioita.


<h2>Tavara-luokka</h2>


Tee luokka `Tavara`, josta muodostetut oliot vastaavat erilaisia tavaroita. Tallennettavat tiedot ovat tavaran nimi ja paino (kg).

Lisää luokkaan seuraavat metodit:

- Konstruktori, jolle annetaan parametrina tavaran nimi ja paino

- Metodi `public String getNimi()`, joka palauttaa tavaran nimen

- Metodi `public int getPaino()`, joka palauttaa tavaran painon

- Metodi `public String toString()`, joka palauttaa merkkijonon muotoa "nimi (paino kg)"

Seuraavassa on luokan käyttöesimerkki:

```java
public class Main {
    public static void main(String[] args) {
        Tavara kirja = new Tavara("Aapiskukko", 2);
        Tavara puhelin = new Tavara("Nokia 3210", 1);

        System.out.println("Kirjan nimi: " + kirja.getNimi());
        System.out.println("Kirjan paino: " + kirja.getPaino());

        System.out.println("Kirja: " + kirja);
        System.out.println("Puhelin: " + puhelin);
    }
}
```

Ohjelman tulostuksen tulisi olla seuraava:


<sample-output>

Kirjan nimi: Aapiskukko
Kirjan paino: 2
Kirja: Aapiskukko (2 kg)
Puhelin: Nokia 3210 (1 kg)

</sample-output>


<h2>Matkalaukku-luokka</h2>

Tee luokka `Matkalaukku`. Matkalaukkuun liittyy tavaroita ja maksimipaino, joka määrittelee tavaroiden suurimman mahdollisen yhteispainon.

Lisää luokkaan seuraavat metodit:

-  Konstruktori, jolle annetaan maksimipaino

-  Metodi `public void lisaaTavara(Tavara tavara)`, joka lisää parametrina annettavan tavaran matkalaukkuun. Metodi ei palauta mitään arvoa.

-  Metodi `public String toString()`, joka palauttaa merkkijonon muotoa "x tavaraa (y kg)"


Tavarat kannattaa tallentaa `ArrayList`-olioon:


```java
ArrayList<Tavara> tavarat = new ArrayList<>();
```

Luokan `Matkalaukku` tulee valvoa, että sen sisältämien tavaroiden yhteispaino ei ylitä maksimipainoa. Jos maksimipaino ylittyisi lisättävän tavaran vuoksi, metodi `lisaaTavara` ei saa lisätä uutta tavaraa laukkuun.

Seuraavassa on luokan käyttöesimerkki:


```java
public class Main {
    public static void main(String[] args) {
        Tavara kirja = new Tavara("Aapiskukko", 2);
        Tavara puhelin = new Tavara("Nokia 3210", 1);
        Tavara tiiliskivi = new Tavara("tiiliskivi", 4);

        Matkalaukku matkalaukku = new Matkalaukku(5);
        System.out.println(matkalaukku);

        matkalaukku.lisaaTavara(kirja);
        System.out.println(matkalaukku);

        matkalaukku.lisaaTavara(puhelin);
        System.out.println(matkalaukku);

        matkalaukku.lisaaTavara(tiiliskivi);
        System.out.println(matkalaukku);
    }
}
```

Ohjelman tulostuksen tulisi olla seuraava:

<sample-output>

0 tavaraa (0 kg)
1 tavaraa (2 kg)
2 tavaraa (3 kg)
2 tavaraa (3 kg)

</sample-output>


<h2>Kielenhuoltoa</h2>

Ilmoitukset "0 tavaraa" ja "1 tavaraa" eivät ole kovin hyvää suomea -- paremmat muodot olisivat "ei tavaroita" ja "1 tavara". Tee tämä muutos luokassa `Matkalaukku` sijaitsevaan toString-metodiin.

Nyt edellisen ohjelman tulostuksen tulisi olla seuraava:

<sample-output>

ei tavaroita (0 kg)
1 tavara (2 kg)
2 tavaraa (3 kg)
2 tavaraa (3 kg)

</sample-output>


<h2>Kaikki tavarat</h2>


Lisää luokkaan `Matkalaukku` seuraavat metodit:

-  metodi `tulostaTavarat`, joka tulostaa kaikki matkalaukussa olevat tavarat

-  metodi `yhteispaino`, joka palauttaa tavaroiden yhteispainon


Seuraavassa on luokan käyttöesimerkki:


```java
public class Main {
    public static void main(String[] args) {
        Tavara kirja = new Tavara("Aapiskukko", 2);
        Tavara puhelin = new Tavara("Nokia 3210", 1);
        Tavara tiiliskivi = new Tavara("tiiliskivi", 4);

        Matkalaukku matkalaukku = new Matkalaukku(10);
        matkalaukku.lisaaTavara(kirja);
        matkalaukku.lisaaTavara(puhelin);
        matkalaukku.lisaaTavara(tiiliskivi);

        System.out.println("Matkalaukussa on seuraavat tavarat:");
        matkalaukku.tulostaTavarat();
        System.out.println("Yhteispaino: " + matkalaukku.yhteispaino() + " kg");
    }
}
```

Ohjelman tulostuksen tulisi olla seuraava:

<sample-output>

Matkalaukussa on seuraavat tavarat:
Aapiskukko (2 kg)
Nokia 3210 (1 kg)
Tiiliskivi (4 kg)
Yhteispaino: 7 kg

</sample-output>

Muokkaa myös luokkaasi siten, että käytät vain kahta oliomuuttujaa. Toinen sisältää maksimipainon, toinen on lista laukussa olevista tavaroista.


<h2>Raskain tavara</h2>

Lisää vielä luokkaan `Matkalaukku` metodi `raskainTavara`, joka palauttaa painoltaan suurimman tavaran. Jos yhtä raskaita tavaroita on useita, metodi voi palauttaa minkä tahansa niistä. Metodin tulee palauttaa olioviite. Jos laukku on tyhjä, palauta arvo <em>null</em>.

Seuraavassa on luokan käyttöesimerkki:

```java
public class Main {
    public static void main(String[] args) {
        Tavara kirja = new Tavara("Aapiskukko", 2);
        Tavara puhelin = new Tavara("Nokia 3210", 1);
        Tavara tiiliskivi = new Tavara("Tiiliskivi", 4);

        Matkalaukku matkalaukku = new Matkalaukku(10);
        matkalaukku.lisaaTavara(kirja);
        matkalaukku.lisaaTavara(puhelin);
        matkalaukku.lisaaTavara(tiiliskivi);

        Tavara raskain = matkalaukku.raskainTavara();
        System.out.println("Raskain tavara: " + raskain);
    }
}
```

Ohjelman tulostuksen tulisi olla seuraava:


<sample-output>

Raskain tavara: Tiiliskivi (4 kg)

</sample-output>


<h2>Lastiruuma-luokka</h2>


Tee luokka `Lastiruuma`, johon liittyvät seuraavat metodit:


-  konstruktori, jolle annetaan maksimipaino

-  metodi `public void lisaaMatkalaukku(Matkalaukku laukku)`, joka lisää parametrina annetun matkalaukun lastiruumaan

-  metodi `public String toString()`, joka palauttaa merkkijonon muotoa "x matkalaukkua (y kg)"


Tallenna matkalaukut sopivaan `ArrayList`-rakenteeseen.

Luokan `Lastiruuma` tulee valvoa, että sen sisältämien matkalaukkujen yhteispaino ei ylitä maksimipainoa. Jos maksimipaino ylittyisi uuden matkalaukun vuoksi, metodi `lisaaMatkalaukku` ei saa lisätä uutta matkalaukkua.

Seuraavassa on luokan käyttöesimerkki:

```java
public class Main {
    public static void main(String[] args) {
        Tavara kirja = new Tavara("Aapiskukko", 2);
        Tavara puhelin = new Tavara("Nokia 3210", 1);
        Tavara tiiliskivi = new Tavara("tiiliskivi", 4);

        Matkalaukku adanLaukku = new Matkalaukku(10);
        adanLaukku.lisaaTavara(kirja);
        adanLaukku.lisaaTavara(puhelin);

        Matkalaukku pekanLaukku = new Matkalaukku(10);
        pekanLaukku.lisaaTavara(tiiliskivi);

        Lastiruuma lastiruuma = new Lastiruuma(1000);
        lastiruuma.lisaaMatkalaukku(adanLaukku);
        lastiruuma.lisaaMatkalaukku(pekanLaukku);

        System.out.println(lastiruuma);
    }
}
```

Ohjelman tulostuksen tulisi olla seuraava:

<sample-output>

2 matkalaukkua (7 kg)

</sample-output>


<h2>Lastiruuman sisältö</h2>

Lisää luokkaan `Lastiruuma` metodi `public void tulostaTavarat()`, joka tulostaa kaikki lastiruuman matkalaukuissa olevat tavarat.

Seuraavassa on luokan käyttöesimerkki:

```java
public class Main {
    public static void main(String[] args) {
        Tavara kirja = new Tavara("Aapiskukko", 2);
        Tavara puhelin = new Tavara("Nokia 3210", 1);
        Tavara tiiliskivi = new Tavara("tiiliskivi", 4);

        Matkalaukku adanLaukku = new Matkalaukku(10);
        adanLaukku.lisaaTavara(kirja);
        adanLaukku.lisaaTavara(puhelin);

        Matkalaukku pekanLaukku = new Matkalaukku(10);
        pekanLaukku.lisaaTavara(tiiliskivi);

        Lastiruuma lastiruuma = new Lastiruuma(1000);
        lastiruuma.lisaaMatkalaukku(adanLaukku);
        lastiruuma.lisaaMatkalaukku(pekanLaukku);

        System.out.println("Ruuman matkalaukuissa on seuraavat tavarat:");
        lastiruuma.tulostaTavarat();
    }
}
```

Ohjelman tulostuksen tulisi olla seuraava:

<sample-output>

Ruuman matkalaukuissa on seuraavat tavarat:
Aapiskukko (2 kg)
Nokia 3210 (1 kg)
tiiliskivi (4 kg)

</sample-output>

