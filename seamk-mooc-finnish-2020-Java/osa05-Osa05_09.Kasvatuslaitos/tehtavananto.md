


Tehtäväpohjassasi on valmiina jo tutuksi tullut luokka `Henkilo` sekä runko luokalle `Kasvatuslaitos`. Kasvatuslaitosoliot käsittelevät ihmisiä eri tavalla, esim. punnitsevat ja syöttävät ihmisiä. Rakennamme tässä tehtävässä kasvatuslaitoksen. Luokan Henkilö koodiin ei tehtävässä ole tarkoitus koskea!


<h2>Henkilöiden punnitseminen</h2>

Kasvatuslaitoksen luokkarungossa on valmiina runko metodille `punnitse`:

```java
public class Kasvatuslaitos {

    public int punnitse(Henkilo henkilo) {
        // palautetaan parametrina annetun henkilön paino
        return -1;
    }
}
```

Metodi saa parametrina henkilön ja metodin on tarkoitus palauttaa kutsujalleen parametrina olevan henkilön paino. Paino selviää kutsumalla parametrina olevan henkilön `henkilo` sopivaa metodia. **Eli täydennä metodin koodi!**

Seuraavassa on pääohjelma jossa kasvatuslaitos punnitsee kaksi henkilöä:

```java
public static void main(String[] args) {
    // esimerkkipääohjelma tehtävän ensimmäiseen kohtaan

    Kasvatuslaitos haaganNeuvola = new Kasvatuslaitos();

    Henkilo eero = new Henkilo("Eero", 1, 110, 7);
    Henkilo pekka = new Henkilo("Pekka", 33, 176, 85);

    System.out.println(eero.getNimi() + " paino: " + haaganNeuvola.punnitse(eero) + " kiloa");
    System.out.println(pekka.getNimi() + " paino: " + haaganNeuvola.punnitse(pekka) + " kiloa");
}
```


Tulostuksen pitäisi olla seuraava:

<sample-output>

Eero paino: 7 kiloa
Pekka paino: 85 kiloa

</sample-output>


<h2>Syöttäminen</h2>


Parametrina olevan olion tilaa on mahdollista muuttaa. Tee kasvatuslaitokselle metodi `public void syota(Henkilo henkilo)` joka kasvattaa parametrina olevan henkilön painoa yhdellä.


Seuraavassa esimerkki, jossa henkilöt ensin punnitaan, ja tämän jälkeen neuvolassa syötetään eeroa kolme kertaa. Tämän jälkeen henkilöt taas punnitaan:


```java
public static void main(String[] args) {
    Kasvatuslaitos haaganNeuvola = new Kasvatuslaitos();

    Henkilo eero = new Henkilo("Eero", 1, 110, 7);
    Henkilo pekka = new Henkilo("Pekka", 33, 176, 85);

    System.out.println(eero.getNimi() + " paino: " + haaganNeuvola.punnitse(eero) + " kiloa");
    System.out.println(pekka.getNimi() + " paino: " + haaganNeuvola.punnitse(pekka) + " kiloa");

    haaganNeuvola.syota(eero);
    haaganNeuvola.syota(eero);
    haaganNeuvola.syota(eero);

    System.out.println("");

    System.out.println(eero.getNimi() + " paino: " + haaganNeuvola.punnitse(eero) + " kiloa");
    System.out.println(pekka.getNimi() + " paino: " + haaganNeuvola.punnitse(pekka) + " kiloa");
}
```

Tulostuksen pitäisi paljastaa että Eeron paino on noussut kolmella:

<sample-output>

Eero paino: 7 kiloa
Pekka paino: 85 kiloa

Eero paino: 10 kiloa
Pekka paino: 85 kiloa

</sample-output>


<h2>Punnitusten laskeminen</h2>


Tee kasvatuslaitokselle metodi `public int punnitukset()` joka kertoo kuinka monta punnitusta kasvatuslaitos on ylipäätään tehnyt. *Huom! Tarvitset uuden oliomuuttujan punnitusten lukumäärän laskemiseen!* Testipääohjelma:


```java
public static void main(String[] args) {
    // esimerkkipääohjelma tehtävän ensimmäiseen kohtaan

    Kasvatuslaitos haaganNeuvola = new Kasvatuslaitos();

    Henkilo eero = new Henkilo("Eero", 1, 110, 7);
    Henkilo pekka = new Henkilo("Pekka", 33, 176, 85);

    System.out.println("punnituksia tehty " + haaganNeuvola.punnitukset());

    haaganNeuvola.punnitse(eero);
    haaganNeuvola.punnitse(pekka);

    System.out.println("punnituksia tehty " + haaganNeuvola.punnitukset());

    haaganNeuvola.punnitse(eero);
    haaganNeuvola.punnitse(eero);
    haaganNeuvola.punnitse(eero);
    haaganNeuvola.punnitse(eero);

    System.out.println("punnituksia tehty " + haaganNeuvola.punnitukset());
}
```

Tulostuu:

<sample-output>

punnituksia tehty 0
punnituksia tehty 2
punnituksia tehty 6

</sample-output>

