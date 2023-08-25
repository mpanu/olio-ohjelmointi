


<h2>Talletettavia</h2>


Muuton yhteydessa tarvitaan muuttolaatikoita. Laatikoihin talletetaan erilaisia esineitä. Kaikkien laatikoihin talletettavien esineiden on toteutettava seuraava rajapinta:


```java
public interface Talletettava {
    double paino();
}
```


Lisää rajapinta ohjelmaasi. Rajapinta lisätään melkein samalla tavalla kuin luokka, <i>new Java class</i> sijaan valitaan <i>new Java interface</i>.


Tee rajapinnan toteuttavat luokat `Kirja` ja `CDLevy`. Kirja saa konstruktorin parametreina kirjan kirjoittajan (String), kirjan nimen (String), ja kirjan painon (double). CD-Levyn konstruktorin parametreina annetaan artisti (String), levyn nimi (String), ja julkaisuvuosi (int). Kaikkien CD-levyjen paino on 0.1 kg.


Muista toteuttaa luokilla myös rajapinta `Talletettava`. Luokkien tulee toimia seuraavasti:


```java
public static void main(String[] args) {
    Kirja kirja1 = new Kirja("Fedor Dostojevski", "Rikos ja Rangaistus", 2);
    Kirja kirja2 = new Kirja("Robert Martin", "Clean Code", 1);
    Kirja kirja3 = new Kirja("Kent Beck", "Test Driven Development", 0.5);

    CDLevy cd1 = new CDLevy("Pink Floyd", "Dark Side of the Moon", 1973);
    CDLevy cd2 = new CDLevy("Wigwam", "Nuclear Nightclub", 1975);
    CDLevy cd3 = new CDLevy("Rendezvous Park", "Closer to Being Here", 2012);

    System.out.println(kirja1);
    System.out.println(kirja2);
    System.out.println(kirja3);
    System.out.println(cd1);
    System.out.println(cd2);
    System.out.println(cd3);
}
```


Tulostus:


<sample-output>

Fedor Dostojevski: Rikos ja Rangaistus
Robert Martin: Clean Code
Kent Beck: Test Driven Development
Pink Floyd: Dark Side of the Moon (1973)
Wigwam: Nuclear Nightclub (1975)
Rendezvous Park: Closer to Being Here (2012)

</sample-output>


Huom! Painoa ei ilmoiteta tulostuksessa.


<h2>Laatikko</h2>


Tee luokka laatikko, jonka sisälle voidaan tallettaa `Talletettava`-rajapinnan toteuttavia tavaroita. Laatikko saa konstruktorissaan parametrina laatikon maksimikapasiteetin kiloina. Laatikkoon ei saa lisätä enempää tavaraa kuin sen maksimikapasiteetti määrää. Laatikon sisältämien tavaroiden paino ei siis koskaan saa olla yli laatikon maksimikapasiteetin.


Seuraavassa esimerkki laatikon käytöstä:


```java
public static void main(String[] args) {
    Laatikko laatikko = new Laatikko(10);

    laatikko.lisaa(new Kirja("Fedor Dostojevski", "Rikos ja Rangaistus", 2)) ;
    laatikko.lisaa(new Kirja("Robert Martin", "Clean Code", 1));
    laatikko.lisaa(new Kirja("Kent Beck", "Test Driven Development", 0.7));

    laatikko.lisaa(new CDLevy("Pink Floyd", "Dark Side of the Moon", 1973));
    laatikko.lisaa(new CDLevy("Wigwam", "Nuclear Nightclub", 1975));
    laatikko.lisaa(new CDLevy("Rendezvous Park", "Closer to Being Here", 2012));

    System.out.println(laatikko);
}
```


Tulostuu


<sample-output>

Laatikko: 6 esinettä, paino yhteensä 4.0 kiloa

</sample-output>


Huom: koska painot esitetään doubleina, saattaa laskutoimituksissa tulla pieniä pyöristysvirheitä. Tehtävässä ei tarvitse välittää niistä.


<h2>Laatikon paino</h2>

Jos teit laatikon sisälle oliomuuttujan `double paino`, joka muistaa laatikossa olevien esineiden painon, korvaa se metodilla, joka laskee painon:


```java
public class Laatikko {
    //...

    public double paino() {
        double paino = 0;
        // laske laatikkoon talletettujen tavaroiden yhteispaino
        return paino;
    }
}
```


Kun tarvitset laatikon sisällä painoa esim. uuden tavaran lisäyksen yhteydessä, riittää siis kutsua laatikon painon laskevaa metodia.


Metodi voisi palauttaa myös oliomuuttujan arvon. Harjoittelemme tässä kuitenkin tilannetta, jossa oliomuuttujaa ei tarvitse eksplisiittisesti ylläpitää vaan se voidaan tarpeentullen laskea. Seuraavan tehtävän jälkeen laatikossa olevaan oliomuuttujaan talletettu painotieto ei kuitenkaan välttämättä enää toimisi. Pohdi tehtävän tekemisen jälkeen miksi näin on.


<h2>Laatikkokin on talletettava!</h2>


Rajapinnan `Talletettava` toteuttaminen siis edellyttää että luokalla on metodi `double paino()`. Laatikollehan lisättiin juuri tämä metodi. Laatikosta voidaan siis tehdä talletettava!


Laatikot ovat olioita joihin voidaan laittaa `Talletettava`-rajapinnan toteuttavia olioita. Laatikot toteuttavat itsekin rajapinnan. Eli **laatikon sisällä voi olla myös laatikoita!**


Kokeile että näin varmasti on, eli tee ohjelmassasi muutama laatikko, laita laatikoihin tavaroita ja laita pienempiä laatikoita isompien laatikoiden sisään. Kokeile myös mitä tapahtuu kun laitat laatikon itsensä sisälle. Miksi näin käy?


