

Luo luokka nimeltä `Pilli`. Lisää luokalle oliomuuttuja `private String aani`. Luo tämän jälkeen konstruktori `public Pilli(String pillinAani)`, jonka avulla luodaan uusi pilli, jolle annetaan ääni.

Lisää pillille vielä metodi `public void soi()`, joka tulostaa pillin äänen.

Pillin tulee toimia seuraavasti.


```java
Pilli sorsapilli = new Pilli("Kvaak");
Pilli kukkopilli = new Pilli("Peef");

sorsapilli.soi();
kukkopilli.soi();
sorsapilli.soi();
```

<sample-output>

Kvaak
Peef
Kvaak

</sample-output>

