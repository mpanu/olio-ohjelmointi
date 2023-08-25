

Tässä tehtävässä on useampi osa. Jokainen osa vastaa yhtä tehtäväpistettä.

Tehtäväpohjan mukana tulee osittain valmiiksi toteutettu luokka `VahenevaLaskuri`:

```java
public class VahenevaLaskuri {
    private int arvo;   // oliomuuttuja joka muistaa laskurin arvon

    public VahenevaLaskuri(int arvoAlussa) {
        this.arvo = arvoAlussa;
    }

    public void tulostaArvo() {
        System.out.println("arvo: " + this.arvo);
    }

    public void vahene() {
        // kirjoita tänne metodin toteutus
        // laskurin arvon on siis tarkoitus vähentyä yhdellä
    }

    // ja tänne muut metodit
}
```

Seuraavassa esimerkki miten pääohjelma käyttää vähenevää laskuria:

```java
public class Paaohjelma {
    public static void main(String[] args) {
        VahenevaLaskuri laskuri = new VahenevaLaskuri(10);

        laskuri.tulostaArvo();

        laskuri.vahene();
        laskuri.tulostaArvo();

        laskuri.vahene();
        laskuri.tulostaArvo();
    }
}
```

Yllä olevalla ohjelmalla tulostuksen pitäisi olla seuraava.

<sample-output>

arvo: 10
arvo: 9
arvo: 8

</sample-output>

`VahenevaLaskuri`-luokan konstruktorille annetaan parametrina alkuarvo. Esimerkin oliota `laskuri` luodessa laskurille välitetään parametrina arvo `10`. Esimerkin `laskuri`-olioon liittyvään oliomuuttujaan `arvo` asetetaan siis aluksi arvo `10`. Laskurin arvon voi tulostaa metodilla `tulostaArvo()`. Laskurilla tulee myös olla metodi `vahene()` joka vähentää laskurin arvoa yhdellä.


<h2>Metodin vahene() toteutus</h2>

Täydennä luokan runkoon metodin `vahene()` toteutus sellaiseksi, että se vähentää kutsuttavan olion oliomuuttujan `arvo` arvoa yhdellä. Kun olet toteuttanut metodin `vahene()`, edellisen esimerkin pääohjelman tulee toimia esimerkkitulosteen mukaan.


<h2>Laskurin arvo ei saa olla negatiivinen</h2>

Täydennä metodin `vahene()` toteutus sellaiseksi, ettei laskurin arvo mene koskaan negatiiviseksi. Eli jos laskurin arvo on jo 0, ei vähennys sitä enää vähennä. Ehtolause auttaa tässä.

```java
public class Paaohjelma {
    public static void main(String[] args) {
        VahenevaLaskuri laskuri = new VahenevaLaskuri(2);

        laskuri.tulostaArvo();

        laskuri.vahene();
        laskuri.tulostaArvo();

        laskuri.vahene();
        laskuri.tulostaArvo();

        laskuri.vahene();
        laskuri.tulostaArvo();
    }
}
```

Tulostuu:

<sample-output>

arvo: 2
arvo: 1
arvo: 0
arvo: 0

</sample-output>


<h2>Laskurin arvon nollaus</h2>

Tee laskurille metodi `public void nollaa()` joka nollaa laskurin arvon, esim:

```java
public class Paaohjelma {
    public static void main(String[] args) {
        VahenevaLaskuri laskuri = new VahenevaLaskuri(100);

        laskuri.tulostaArvo();

        laskuri.nollaa();
        laskuri.tulostaArvo();

        laskuri.vahene();
        laskuri.tulostaArvo();
    }
}
```

Tulostuu:

<sample-output>

arvo: 100
arvo: 0
arvo: 0

</sample-output>


