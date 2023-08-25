

Luo luokkaan `Ohjelma` luokkametodi `public static int summa(int[] taulukko, int mista, int mihin, int pienin, int suurin)`. Metodin tulee laskea sille parametrina annetusta taulukosta indeksien mista ja mihin välillä olevien arvojen summa. Summaan otetaan mukaan vain ne arvot, jotka ovat suurempia tai yhtäsuuria kuin pienin ja pienempiä kuin suurin.

Metodin tulee lisäksi varmistaa, että käsiteltävät indeksit ovat valideja. Mikäli parametri `mista` on pienempi kuin 0, tulee taulukon indeksien läpikäynti alkaa parametrin mista arvon sijaan nollasta. Vastaavasti, mikäli parametri `mihin` on suurempi kuin käsiteltävä taulukko, tulee taulukon indeksien läpikäynti lopettaa  parametrin mihin arvon sijaan taulukon kokoon.

```java
int[] luvut = {3, -1, 8, 4};

System.out.println(summa(luvut, 0, 0, 0, 0));
System.out.println(summa(luvut, 0, 0, 0, 10));
System.out.println(summa(luvut, 0, 1, 0, 10));
System.out.println(summa(luvut, 0, 1, -10, 10));
System.out.println(summa(luvut, -1, 999, -10, 10));
```

<sample-output>

0
0
3
3
14

</sample-output>

