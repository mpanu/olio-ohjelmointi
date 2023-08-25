

Tehtäväpohjan mukana tulee valmis luokka `Tili`. Luokan `Tili` olio esittää pankkitiliä, jolla on saldo (eli jossa on jokin määrä rahaa). Tilejä käytetään näin:

```java
Tili artonTili = new Tili("Arton tili", 100.00);
Tili artonSveitsilainenTili = new Tili("Arton tili Sveitsissä", 1000000.00);

System.out.println("Alkutilanne");
System.out.println(artonTili);
System.out.println(artonSveitsilainenTili);

artonTili.otto(20);
System.out.println("Arton tilin saldo on nyt: " + artonTili.saldo());
artonSveitsilainenTili.pano(200);
System.out.println("Arton toisen tilin saldo on nyt: " + artonSveitsilainenTili.saldo());

System.out.println("Lopputilanne");
System.out.println(artonTili);
System.out.println(artonSveitsilainenTili);
```

Tee ohjelma, joka luo tilin jonka saldo on 100.0, panee tilille 20.0 ja tulostaa tilin. **Huom!** tee kaikki nämä operaatiot täsmälleen tässä järjestyksessä.

