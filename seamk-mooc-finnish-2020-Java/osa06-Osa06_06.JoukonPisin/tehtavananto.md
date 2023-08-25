

Tehtäväpohjassa on mukana aiemmasta tehtävästä tuttu luokka `Joukko`. Toteuta luokkaan metodi `public String pisin()`, joka palauttaa joukon pisimmän merkkijonon. Mikäli joukko on tyhjä, metodin tulee palauttaa `null`-viite.

```java
Joukko j = new Joukko("hahmot");
System.out.println("Pisin: " + j.pisin());

j.lisaa("magneto");
j.lisaa("mystique");
j.lisaa("phoenix");

System.out.println("Pisin: " + j.pisin());
```

<sample-output>

Pisin: null
Pisin: mystique

</sample-output>

