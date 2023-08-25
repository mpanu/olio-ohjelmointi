

Luo luokka `Velka`, jolla on double-tyyppiset oliomuuttujat `saldo` ja `korkokerroin`. Saldo ja korkokerroin annetaan konstruktorin parametrina `public Velka(double saldoAlussa, double korkokerroinAlussa)`.

Luo luokalle myös metodit `public void tulostaSaldo()` sekä `public void odotaVuosi()`. Metodi tulostaSaldo tulostaa tämän hetkisen saldon, ja metodi odotaVuosi kasvattaa velan määrää.

Velan määrän kasvattaminen tapahtuu kertomalla saldo korkokertoimella.

Luokan tulee toimia seuraavasti:

```java
public class Paaohjelma {
    public static void main(String[] args) {

        Velka asuntolaina = new Velka(120000.0, 1.01);
        asuntolaina.tulostaSaldo();

        asuntolaina.odotaVuosi();
        asuntolaina.tulostaSaldo();

        int vuosia = 0;

        while (vuosia < 20) {
            asuntolaina.odotaVuosi();
            vuosia = vuosia + 1;
        }

        asuntolaina.tulostaSaldo();
    }
}
```

Ylläolevassa esimerkissä havainnollistetaan asuntolainan kehitystä prosentin korolla.

Tulostus:

<sample-output>

120000.0
121200.0
147887.0328416936

</sample-output>

Kun saat ohjelman toimimaan, tarkastele edelläolevaa esimerkkiä myös 1990-luvun alkupuolen laman korkokertoimilla. Tällöin korko oli jopa 15-20 prosenttia -- muuta yllä olevan esimerkin korkokertoimeksi `1.20` ja katso miten käy.

