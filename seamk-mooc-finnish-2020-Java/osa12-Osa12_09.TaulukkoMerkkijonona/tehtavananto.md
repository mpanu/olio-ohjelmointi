

Luo tehtäväpohjaan metodi `public static String taulukkoMerkkijonona(int[][] taulukko)`, joka muodostaa parametrina saamastaan taulukosta merkkijonomuotoisen esityksen ja palauttaa sen.

Kertaa yhdeksännestä osasta StringBuilderin käyttö ennen tehtävän tekoa. Alla muutamia esimerkkejä metodin odotetusta toiminnasta.


```java
int rivit = 2;
int sarakkeet = 3;
int[][] matriisi = new int[rivit][sarakkeet];
matriisi[0][1] = 5;
matriisi[1][0] = 3;
matriisi[1][2] = 7;
System.out.println(taulukkoMerkkijonona(matriisi));
```

<sample-output>

050
307

</sample-output>

```java
int[][] matriisi = {
    {3, 2, 7, 6},
    {2, 4, 1, 0},
    {3, 2, 1, 0}
};

System.out.println(taulukkoMerkkijonona(matriisi));
```

<sample-output>

3276
2410
3210

</sample-output>

