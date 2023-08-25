

Luo kuutiota (eli säännöllistä kuusitahokasta) esittävä luokka `Kuutio`. Luo luokalle konstruktori `public Kuutio(int sarmanPituus)`, joka saa parametrinaan kuution särmän pituuden.


Tee kuutiolle metodi `public int tilavuus()`, joka laskee ja palauttaa kuution tilavuuden. Kuution tilavuus lasketaan kaavalla `sarmanPituus * sarmanPituus * sarmanPituus`. Tee tämän jälkeen kuutiolle vielä metodi `public String toString()`, joka palauttaa kuutiota kuvaavan merkkijonoesityksen. Merkkijonoesityksen tulee olla muotoa "`Kuution särmän pituus on p, tilavuus on t`", missä `p`on pituus ja `t` on tilavuus -- sekä pituus että tilavuus tulee kuvata kokonaislukuina.


Alla esimerkkejä


```java
Kuutio oSheaJackson = new Kuutio(4);
System.out.println(oSheaJackson.tilavuus());
System.out.println(oSheaJackson);

System.out.println();

Kuutio suola = new Kuutio(2);
System.out.println(suola.tilavuus());
System.out.println(suola);
```

<sample-output>

64
Kuution särmän pituus on 4, tilavuus on 64

8
Kuution särmän pituus on 2, tilavuus on 8

</sample-output>

