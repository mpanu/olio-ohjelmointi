

Toteuta pääohjelmaluokkaan luokkametodi `palautaKoko`, joka saa parametrina Set-olion ja palauttaa sen koon kokonaislukuna.

Metodin tulee toimia esimerkiksi seuraavasti:


```java
Set<String> nimet = new HashSet<>();
nimet.add("eka");
nimet.add("eka");
nimet.add("toka");
nimet.add("toka");
nimet.add("toka");

System.out.println(palautaKoko(nimet));
```

Tulostaa:

<sample-output>

2

</sample-output>

