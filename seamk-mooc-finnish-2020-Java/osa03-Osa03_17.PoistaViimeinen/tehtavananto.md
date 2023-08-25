

Luo tehtäväpohjaan metodi `public static void poistaViimeinen(ArrayList<String> mjonot)`. Metodin tulee poistaa parametrina saadusta listasta viimeisin arvo. Mikäli lista on tyhjä, metodin ei tule tehdä mitään.

```java
ArrayList<String> merkkijonot = new ArrayList<>();

merkkijonot.add("Eka");
merkkijonot.add("Toka");
merkkijonot.add("Kolmas");

System.out.println(merkkijonot);

poistaViimeinen(merkkijonot);
poistaViimeinen(merkkijonot);

System.out.println(merkkijonot);
```

<sample-output>
[Eka, Toka, Kolmas]
[Eka]
</sample-output>

