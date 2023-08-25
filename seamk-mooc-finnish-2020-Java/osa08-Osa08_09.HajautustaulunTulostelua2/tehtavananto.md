

Tehtäväpohjassa tulee materiaalista tuttu luokka `Kirja` sekä luokka `Ohjelma`. Luo luokkaan `Ohjelma` seuraavat kaksi luokkametodia:

- `public static void tulostaArvot(HashMap<String, Kirja> hajautustaulu)`, joka tulostaa parametrina annetun hajautustaulun arvot niiden toString-metodia käyttäen.

- `public static void tulostaArvoJosNimessa(HashMap<String, Kirja> hajautustaulu, String merkkijono)`, joka tulostaa parametrina annetun hajautustaulun arvoista ne, joiden nimessä on parametrina annettu merkkijono. Nimen saa selville kirjan metodilla `getNimi`.

Esimerkki luokkametodien käytöstä:

```java
HashMap<String, Kirja> taulu = new HashMap<>();
taulu.put("tunteet", new Kirja("Järki ja tunteet", 1811, "..."));
taulu.put("luulot", new Kirja("Ylpeys ja ennakkoluulo", 1813, "...."));

tulostaArvot(taulu);
System.out.println("---");
tulostaArvoJosNimessa(taulu, "ennakko");
```

<sample-output>
Nimi: Ylpeys ja ennakkoluulo (1813)
Sisältö: ...
Nimi: Järki ja tunteet (1811)
Sisältö: ...
---
Nimi: Ylpeys ja ennakkoluulo (1813)
Sisältö: ...
</sample-output>

Huom! Tulostusjärjestys voi poiketa yllä esitetystä, sillä hajautustaulun sisäinen toteutus ei takaa olioiden järjestystä.

