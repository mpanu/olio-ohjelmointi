

Tehtäväpohjassa on annettuna metodirunko `public static ArrayList<Integer> jaolliset(ArrayList<Integer> luvut)`. Toteuta metodirunkoon toiminnallisuus, joka kerää parametrina saadulta listalta kahdella, kolmella tai viidellä jaolliset luvut, ja palauttaa ne uudessa listassa. Metodille parametrina annetun listan ei tule muuttua.

```java
ArrayList<Integer> luvut = new ArrayList<>();
luvut.add(3);
luvut.add(2);
luvut.add(-17);
luvut.add(-5);
luvut.add(7);

ArrayList<Integer> jaolliset = jaolliset(luvut);

jaolliset.stream()
    .forEach(luku -> System.out.println(luku));
```

<sample-output>

3
2
-5

</sample-output>

