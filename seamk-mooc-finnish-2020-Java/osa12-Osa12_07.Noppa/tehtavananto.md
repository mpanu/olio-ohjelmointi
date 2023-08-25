

Tehtäväpohjassa on luokka `Noppa`, jonka runko on seuraava:

```java
import java.util.Random;

public class Noppa {
    private Random random;
    private int tahkojenMaara;

    public Noppa(int tahkojenMaara) {
        this.random = new Random();
        // Alusta oliomuuttuja tahkojenMaara tässä
    }

    public int heita() {
        // arvo täällä luku jonka tulee olla yhdestä tahkojen määrään
        // ja palauta se
    }
}
```

Muokkaa luokkaa siten, että sen konstruktori`Noppa(int tahkojenMaara)` luo uuden noppa-olion annetulla nopan tahkojen (eri oman numeronsa sisältämien "puolien") määrällä. Muokkaa myös metodia `heita` siten, että se antaa satunnaisen nopanheiton tuloksen, jonka arvon tulee olla väliltä `1...tahkojen määrä`.

Seuraavassa noppaa testaava pääohjelma:


```java
public class Ohjelma {
    public static void main(String[] args) {
        Noppa noppa = new Noppa(6);

        for (int i = 0; i < 10; i++) {
            System.out.println(noppa.heita());
        }
    }
}
```

Tulostus voisi olla esimerkiksi seuraava:

<sample-output>

1
6
3
5
3
3
2
2
6
1

</sample-output>

