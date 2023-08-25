

<h2>Lukujen määrä</h2>

Tee luokka `Lukutilasto` (tiedosto luomaasi luokkaa varten on tehtäväpohjassa valmiina), joka tuntee seuraavat toiminnot:

- metodi `lisaaLuku` lisää uuden luvun tilastoon
- metodi `haeLukujenMaara` kertoo lisättyjen lukujen määrän

Luokan ei tarvitse tallentaa mihinkään lisättyjä lukuja, vaan riittää muistaa niiden määrä. Metodin `lisaaLuku` ei tässä vaiheessa tarvitse edes ottaa huomioon, mikä luku lisätään tilastoon, koska ainoa tallennettava asia on lukujen määrä.

Luokan runko on seuraava:

```java
public class Lukutilasto {
    private int lukujenMaara;

    public Lukutilasto() {
        // alusta tässä muuttuja lukujenMaara
    }

    public void lisaaLuku(int luku) {
        // kirjoita koodia tähän
    }

    public int haeLukujenMaara() {
        // kirjoita koodia tähän
    }
}
```

Seuraava ohjelma esittelee luokan käyttöä:

```java
public class Paaohjelma {
    public static void main(String[] args) {
        Lukutilasto tilasto = new Lukutilasto();
        tilasto.lisaaLuku(3);
        tilasto.lisaaLuku(5);
        tilasto.lisaaLuku(1);
        tilasto.lisaaLuku(2);
        System.out.println("Määrä: " + tilasto.haeLukujenMaara());
    }
}
```

Ohjelman tulostus on seuraava:

<sample-output>

Määrä: 4

</sample-output>


<h2>Summa ja keskiarvo</h2>

Laajenna luokkaa seuraavilla toiminnoilla:

- metodi `summa` kertoo lisättyjen lukujen summan (tyhjän lukutilaston summa on 0)
- metodi `keskiarvo` kertoo lisättyjen lukujen keskiarvon (tyhjän lukutilaston keskiarvo on 0)

Luokan runko on seuraava:

```java
public class Lukutilasto {
    private int lukujenMaara;
    private int summa;

    public Lukutilasto() {
        // alusta tässä muuttujat maara ja summa
    }

    public void lisaaLuku(int luku) {
        // kirjoita koodia tähän
    }

    public int haeLukujenMaara() {
        // kirjoita koodia tähän
    }

    public int summa() {
        // kirjoita koodia tähän
    }

    public double keskiarvo() {
        // kirjoita koodia tähän
    }
}
```

Seuraava ohjelma esittelee luokan käyttöä:

```java
public class Main {
    public static void main(String[] args) {
        Lukutilasto tilasto = new Lukutilasto();
        tilasto.lisaaLuku(3);
        tilasto.lisaaLuku(5);
        tilasto.lisaaLuku(1);
        tilasto.lisaaLuku(2);
        System.out.println("Määrä: " + tilasto.haeLukujenMaara());
        System.out.println("Summa: " + tilasto.summa());
        System.out.println("Keskiarvo: " + tilasto.keskiarvo());
    }
}
```

Ohjelman tulostus on seuraava:

<sample-output>

Määrä: 4
Summa: 11
Keskiarvo: 2.75

</sample-output>


<h2>Summa käyttäjältä</h2>


Tee ohjelma, joka kysyy lukuja käyttäjältä, kunnes käyttäjä antaa luvun -1. Sitten ohjelma ilmoittaa lukujen summan.

Ohjelmassa tulee käyttää `Lukutilasto`-oliota summan laskemiseen.

**HUOM:** Älä muuta tässä osassa luokkaa Lukutilasto, vaan toteuta sitä hyödyntäen summan laskemiseen käytetty ohjelma.

<sample-output>

Anna lukuja:
**4**
**2**
**5**
**4**
**-1**
Summa: 15

</sample-output>


<h2>Monta summaa</h2>

Muuta edellistä ohjelmaa niin, että ohjelma laskee myös parillisten ja parittomien lukujen summaa.

**HUOM**: Määrittele ohjelmassa *kolme* Lukutilasto-oliota ja laske ensimmäisen avulla kaikkien lukujen summa, toisen avulla parillisten lukujen summa ja kolmannen avulla parittomien lukujen summa.

**Jotta testi toimisi, on oliot luotava pääohjelmassa edellä mainitussa järjestyksessä (eli ensin kaikkien summan laskeva olio, toisena parillisten summan laskeva ja viimeisenä parittomien summan laskeva olio)!**

**HUOM:** älä muuta Lukutilasto-luokkaa millään tavalla!

Ohjelman tulee toimia seuraavasti:

<sample-output>

Anna lukuja:
**4**
**2**
**5**
**2**
**-1**
Summa: 13
Parillisten summa: 8
Parittomien summa: 5

</sample-output>

