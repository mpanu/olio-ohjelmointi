

Tehtäväpohjassa tulee luokka `Ohjelma`. Luo luokkaan seuraavat kolme luokkametodia:

- `public static void tulostaAvaimet(HashMap<String, String> hajautustaulu)`, joka tulostaa parametrina annetun hajautustaulun avaimet.

- `public static void tulostaAvaimetJoissa(HashMap<String, String> hajautustaulu, String merkkijono)`, joka tulostaa parametrina annetun hajautustaulun avaimista ne, jotka sisältävät parametrina annetun merkkijonon.

- `public static void tulostaArvotJosAvaimessa(HashMap<String, String> hajautustaulu, String merkkijono)`, joka tulostaa parametrina annetun hajautustaulun ne arvot, joihin liittyvät avaimet sisältävät parametrina annetun merkkijonon.

Esimerkki luokkametodien käytöstä:

```java
HashMap<String, String> taulu = new HashMap<>();
taulu.put("esim.", "esimerkiksi");
taulu.put("jne.", "ja niin edelleen");
taulu.put("yms.", "ynnä muuta sellaista");

tulostaAvaimet(taulu);
System.out.println("---");
tulostaAvaimetJoissa(taulu, "m");
System.out.println("---");
tulostaArvotJosAvaimessa(taulu, "ne");
```

<sample-output>
esim.
jne.
yms.
---
esim.
yms.
---
ja niin edelleen
</sample-output>

Huom! Tulostusjärjestys voi poiketa yllä esitetystä, sillä hajautustaulun sisäinen toteutus ei takaa olioiden järjestystä.

