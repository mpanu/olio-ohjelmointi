

Täydennä tehtäväpohjassa olevaa metodia `summa` siten, että se laskee ja palauttaa parametrina olevien lukujen summan.

Tee metodi seuraavaan runkoon:

```java
public static int summa(int luku1, int luku2, int luku3, int luku4) {
    // kirjoita koodia tähän
    // muista että metodissa on oltava (lopussa) return!
}

public static void main(String[] args) {
    int vastaus = summa(4, 3, 6, 1);
    System.out.println("Summa: " + vastaus);
}
```

Ohjelman tulostus:

<sample-output>

Summa: 14

</sample-output>

**Huom:** kun tehtävässä sanotaan että metodin pitää _palauttaa_ jotain, tarkoittaa tämä sitä että metodissa tulee olla määritelty paluutyyppi ja `return`-komento jolla haluttu asia palautetaan. Metodi ei itse tulosta (eli käytä komentoa `System.out.println(..)`), tulostuksen hoitaa metodin kutsuja, eli tässä tapauksessa pääohjelma.

