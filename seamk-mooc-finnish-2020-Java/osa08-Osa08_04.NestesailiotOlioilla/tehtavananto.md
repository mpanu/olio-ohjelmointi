

Toteutetaan edellä kuvattu interaktiivinen ohjelma kahden nestesäiliön käsittelyyn uudestaan. Tällä kertaa luodaan ohjelman toteutusta varten luokka "Sailio", jonka vastuulla on säiliön sisällön ylläpito.


<h2>Sailio</h2>

Toteuta luokka Sailio. Säiliöllä tulee olla parametriton konstruktori sekä seuraavat metodit:

- `public int sisalto()` palauttaa säiliössä olevan nesteen määrän kokonaislukuna.

- `public void lisaa(int maara)` lisää parametrina annetun määrän nestettä säiliöön. Mikäli parametrin arvo on negatiivinen, ei nestettä lisätä. Lisäyksen jälkeen säiliössä on korkeintaan 100 yksikköä nestettä.

- `public void poista(int maara)` poistaa parametrina annetun määrän nestettä säiliöstä. Mikäli parametrin arvo on negatiivinen, ei nestettä poisteta. Poistaminen poistaa vain olemassaolevaa nestettä -- poiston takia säiliössä ei voi koskaan olla alle nollaa nesteyksikköä.

- `public String toString()` palauttaa olion merkkijonoesityksen muodossa "<em>sisalto</em>/100", esim "32/100".


Luokan käyttöesimerkki:


```java
Sailio sailio = new Sailio();
System.out.println(sailio);

sailio.lisaa(50);
System.out.println(sailio);
System.out.println(sailio.sisalto());

sailio.poista(60);
System.out.println(sailio);

sailio.lisaa(200);
System.out.println(sailio);
```

<sample-output>

0/100
50/100
50
0/100
100/100

</sample-output>


<h2>Toiminnallisuus</h2>

Kopioi ensimmäisessä osassa toteuttamasi käyttöliittymä ja muokkaa sitä siten, että ohjelmassa käytetään juuri toteuttamiasi säiliöitä. Luokassa `NestesailiotOlioilla` olevan main-metodin suorituksen tulee käynnistää ohjelma.

Alla on esimerkkitulostus. Ohjelman tekstikäyttöliittymän toiminnan tulee olla seuraavanlainen:

<sample-output>

Ensimmäinen: 0/100
Toinen: 0/100
**poista 10**

Ensimmäinen: 0/100
Toinen: 0/100
**lisaa 20**

Ensimmäinen: 20/100
Toinen: 0/100
**poista 5**

Ensimmäinen: 20/100
Toinen: 0/100
**siirra 15**

Ensimmäinen: 5/100
Toinen: 15/100
**poista 5**

Ensimmäinen: 5/100
Toinen: 10/100
**poista 20**

Ensimmäinen: 5/100
Toinen: 0/100
**lopeta**

</sample-output>

