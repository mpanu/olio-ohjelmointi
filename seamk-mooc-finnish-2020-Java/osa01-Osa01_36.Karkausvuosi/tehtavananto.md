

Vuosi on karkausvuosi, jos se on jaollinen 4:llä. Kuitenkin jos vuosi on jaollinen 100:lla, se on karkausvuosi vain silloin, kun se on jaollinen myös 400:lla.

Tee ohjelma, joka lukee käyttäjältä vuosiluvun, ja tarkistaa, onko vuosi karkausvuosi.

<sample-output>

Anna vuosi: **2011**
Vuosi ei ole karkausvuosi.

</sample-output>

<sample-output>

Anna vuosi: **2012**
Vuosi on karkausvuosi.

</sample-output>

<sample-output>

Anna vuosi: **1800**
Vuosi ei ole karkausvuosi.

</sample-output>

<sample-output>

Anna vuosi: **2000**
Vuosi on karkausvuosi.

</sample-output>

Vihje 1: Jollain luvulla jaollisuuden voi tarkastaa jakojäännösoperaation `%` avulla seuraavasti.

```java
int luku = 5;

if (luku % 5 == 0) {
    System.out.println("Luku on viidellä jaollinen!");
}

if (luku % 6 != 0) {
    System.out.println("Luku ei ole kuudella jaollinen!")
}
```

<sample-output>

Luku on viidellä jaollinen!
Luku ei ole kuudella jaollinen!

</sample-output>

Vihje 2: mieti ongelmaa if, else if, else if, ... -vertailujen ketjuna ja aloita ohjelman rakentaminen tilanteesta, missä voit olla varma, että ohjelma ei ole karkausvuosi.


```java
Scanner lukija = new Scanner(System.in);
int luku = Integer.valueOf(lukija.nextLine());

if (luku % 4 != 0) {
    System.out.println("Vuosi ei ole karkausvuosi.");
} else if (...) {
    ...
} ...
```

