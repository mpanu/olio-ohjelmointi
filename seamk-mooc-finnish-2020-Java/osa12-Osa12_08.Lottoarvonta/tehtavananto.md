

Tehtävänäsi on täydentää luokkaa `Lottorivi`, joka arpoo viikon lottonumerot. Lottonumerot ovat väliltä 1--40 ja niitä arvotaan 7. Lottorivi koostuu siis seitsemästä eri numerosta väliltä 1--40.

Luokalle toivotaan seuraava toiminnot:

- konstruktori `Lottorivi` luo uuden Lottorivi-olion joka sisältää uudet, arvotut numerot
- metodi `numerot` palauttaa tämän lottorivin lottonumerot
- metodi `sisaltaaNumeron` kertoo onko arvotuissa numeroissa annettu numero
- metodi `arvoNumerot` arpoo riville uudet numerot

Luokan runko on seuraava:

```java
import java.util.ArrayList;
import java.util.Random;

    public class LottoRivi {
    private ArrayList<Integer> numerot;

    public LottoRivi() {
        this.arvoNumerot();
    }

    public ArrayList<Integer> numerot() {
        return this.numerot;
    }

    public boolean sisaltaaNumeron(int numero) {
        // Testaa tässä onko numero jo arvottujen numeroiden joukossa
        return false;
    }

    public void arvoNumerot() {
        // alustetaan lista numeroille
        this.numerot = new ArrayList<>();
        // Kirjoita numeroiden arvonta tänne käyttämällä metodia sisaltaaNumeron()
    }

    public boolean equals(Object toinen) {
        return false;
    }
}
```

Tehtäväpohjan mukana tulee seuraava pääohjelma:


```java
import java.util.ArrayList;

public class Ohjelma {
    public static void main(String[] args) {
        Lottorivi rivi = new Lottorivi();
        ArrayList<Integer> lottonumerot = rivi.numerot();

        System.out.println("Lottonumerot:");
        for (int numero: lottonumerot) {
            System.out.print(numero + " ");
        }

        System.out.println("");
    }
}
```

Ohjelman mahdollisia tulostuksia ovat seuraavat:


<sample-output>

Lottonumerot:
3 5 10 14 15 27 37

</sample-output>

<sample-output>

Lottonumerot:
2 9 11 18 23 32 34

</sample-output>


**Huom!** Sama numero saa esiintyä lottorivissä vain kerran. Lottorivin numeroiden ei tarvitse olla järjestyksessä.

