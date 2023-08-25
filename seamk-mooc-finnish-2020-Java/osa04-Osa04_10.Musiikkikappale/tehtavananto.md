

Luo luokka nimeltä `Musiikkikappale`. Musiikkikappaleella on oliomuuttujat `nimi` (merkkijono) ja `pituus` sekunteina (kokonaisluku). Molemmat asetetaan konstruktorissa `public Musiikkikappale(String kappaleenNimi, int kappaleenPituus)`. Lisää oliolle myös metodit `public String nimi()`, joka palauttaa kappaleen nimen, ja `public int pituus()`, joka palauttaa kappaleen pituuden.

Luokan tulee toimia seuraavasti.

```java
Musiikkikappale garden = new Musiikkikappale("In The Garden", 10910);
System.out.println("Kappaleen " + garden.nimi() + " pituus on " + garden.pituus() + " sekuntia.");
```

<sample-output>

Kappaleen In The Garden pituus on 10910 sekuntia.

</sample-output>

