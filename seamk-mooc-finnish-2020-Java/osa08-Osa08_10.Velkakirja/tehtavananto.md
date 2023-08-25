

Luo luokka `Velkakirja`, jolla on seuraavat toiminnot:


- konstruktori `public Velkakirja()` luo uuden velkakirjan

- metodi `public void asetaLaina(String kenelle, double maara)` tallettaa velkakirjaan merkinnän lainasta tietylle henkilölle.

- metodi `public double paljonkoVelkaa(String kuka)` palauttaa velan määrän annetun henkilön nimen perusteella. Jos henkilöä ei löydy, palautetaan 0.


Luokkaa käytetään seuraavalla tavalla:

```java
Velkakirja matinVelkakirja = new Velkakirja();
matinVelkakirja.asetaLaina("Arto", 51.5);
matinVelkakirja.asetaLaina("Mikael", 30);

System.out.println(matinVelkakirja.paljonkoVelkaa("Arto"));
System.out.println(matinVelkakirja.paljonkoVelkaa("Joel"));
```

Yllä oleva esimerkki tulostaisi:

<sample-output>

51.5
0.0

</sample-output>

Ole tarkkana tilanteessa, jossa kysytään velattoman ihmisen velkaa.

Huom! Velkakirjan ei tarvitse huomioida vanhoja lainoja. Kun asetat uuden velan henkilölle jolla on vanha velka, vanha velka unohtuu.

```java
Velkakirja matinVelkakirja = new Velkakirja();
matinVelkakirja.asetaLaina("Arto", 51.5);
matinVelkakirja.asetaLaina("Arto", 10.5);

System.out.println(matinVelkakirja.paljonkoVelkaa("Arto"));
```

<sample-output>

10.5

</sample-output>

