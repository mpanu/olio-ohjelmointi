

Tässä tehtävässä harjoitellaan lahjojen pakkaamista. Tehdään luokat `Lahja` ja `Pakkaus`. Lahjalla on nimi ja paino, ja Pakkaus sisältää lahjoja.


<h2>Lahja-luokka</h2>

Tee luokka `Lahja`, josta muodostetut oliot kuvaavat erilaisia lahjoja. Tallennettavat tiedot ovat tavaran nimi ja paino (kg).

Lisää luokkaan seuraavat metodit:

- Konstruktori, jolle annetaan parametrina lahjan nimi ja paino

- Metodi `public String getNimi()`, joka palauttaa lahjan nimen

- Metodi `public int getPaino()`, joka palauttaa lahjan painon

- Metodi `public String toString()`, joka palauttaa merkkijonon muotoa "nimi (paino kg)"


Seuraavassa on luokan käyttöesimerkki:


```java
public class Main {
    public static void main(String[] args) {
        Lahja kirja = new Lahja("Aapiskukko", 2);

        System.out.println("Lahjan nimi: " + kirja.getNimi());
        System.out.println("Lahjan paino: " + kirja.getPaino());

        System.out.println("Lahja: " + kirja);
    }
}
```


Ohjelman tulostuksen tulisi olla seuraava:


<sample-output>

Lahjan nimi: Aapiskukko
Lahjan paino: 2
Lahja: Aapiskukko (2 kg)

</sample-output>


<h2>Pakkaus-luokka</h2>

Tee luokka `Pakkaus`, johon voi lisätä lahjoja, ja joka pitää kirjaa pakkauksessa olevien lahjojen yhteispainosta. Luokassa tulee olla:

- Parametriton konstruktori

- Metodi `public void lisaaLahja(Lahja lahja)`, joka lisää parametrina annettavan lahjan pakkaukseen. Metodi ei palauta mitään arvoa.

- Metodi `public int yhteispaino()`, joka palauttaa pakkauksessa olevien lahjojen yhteispainon.


Tavarat kannattaa tallentaa `ArrayList`-olioon:


```java
ArrayList<Lahja> lahjat = new ArrayList<>();
```

Seuraavassa on luokan käyttöesimerkki:


```java
public class Main {
    public static void main(String[] args) {
        Lahja kirja = new Lahja("Aapiskukko", 2);

        Pakkaus paketti = new Pakkaus();
        paketti.lisaaLahja(kirja);
        System.out.println(paketti.yhteispaino());
    }
}
```

Ohjelman tulostuksen tulisi olla seuraava:

<sample-output>

2

</sample-output>

