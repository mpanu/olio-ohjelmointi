

Luo luokka Elokuva, jolla on oliomuuttujat `nimi` (String) ja `ikaraja` (int). Tee luokalle konstruktori `public Elokuva(String elokuvanNimi, int elokuvanIkaraja)` sekä metodit `public String nimi()` ja `public int ikaraja()`. Ensimmäinen palauttaa elokuvan nimen ja toinen elokuvan ikärajan.

Esimerkki luokan käytöstä.

```java
Elokuva chipmunks = new Elokuva("Alvin and the Chipmunks: The Squeakquel", 0);

Scanner lukija = new Scanner(System.in);

System.out.println("Minkä ikäinen olet?");
int ika = Integer.valueOf(lukija.nextLine());

System.out.println();
if (ika >= chipmunks.ikaraja()) {
    System.out.println("Saat katsoa elokuvan " + chipmunks.nimi());
} else {
    System.out.println("Et saa katsoa elokuvaa " + chipmunks.nimi());
}
```

<sample-output>

Minkä ikäinen olet?
**7**

Saat katsoa elokuvan Alvin and the Chipmunks: The Squeakquel

</sample-output>

