

Luo luokka `Mittari`. Mittarilla on oliomuuttuja `private int mitta`, parametriton konstruktori (asettaa muuttujan mitta alkuarvoksi 0), sekä seuraavat neljä metodia:

- Metodi `public void lisaa()` kasvattaa oliomuuttujan `mitta` arvoa yhdellä. Ei kasvata arvoa yli viiden.
- Metodi `public void vahenna()` vähentää oliomuuttujan `mitta` arvoa yhdellä. Ei vähennä arvoa negatiiviseksi.
- Metodi `public int mitta()` palauttaa oliomuuttujan `mitta` arvon.
- Metodi `public boolean taynna()` palauttaa `true` mikäli oliomuuttujan `mitta` on viisi, palauttaa muulloin false.

Esimerkki luokan käytöstä.

```java
Mittari m = new Mittari();

while(!m.taynna()) {
    System.out.println("Ei täynnä! Mitta: " + m.mitta());
    m.lisaa();
}

System.out.println("Täynnä! Mitta: " + m.mitta());
m.vahenna();
System.out.println("Ei täynnä! Mitta: " + m.mitta());

```

<sample-output>

Ei täynnä! Mitta: 0
Ei täynnä! Mitta: 1
Ei täynnä! Mitta: 2
Ei täynnä! Mitta: 3
Ei täynnä! Mitta: 4
Täynnä! Mitta: 5
Ei täynnä! Mitta: 4

</sample-output>

