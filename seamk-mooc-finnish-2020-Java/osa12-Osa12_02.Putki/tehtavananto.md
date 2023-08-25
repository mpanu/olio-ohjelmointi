

Toteuta luokka Putki, jolla on yksi geneerinen tyyppiparametri. Putki toimii siten, että sinne voi lisätä arvoja ja sieltä voi ottaa arvoja. Lisääminen tapahtuu putken toisesta päästä ja ottaminen toisesta päästä, eli toisin sanoen putkesta otetaan aina siellä pisimpään ollut arvo kun taas sinne lisätään aina uusin arvo. Luokan tulee tarjota parametriton konstruktori sekä seuraavat kolme metodia:

- `public void lisaaPutkeen(T arvo)` lisää putkeen luokan tyyppiparametrin mukaisen olion.
- `public T otaPutkesta()` ottaa putkesta siellä pisimpään olleen arvon. Mikäli putkessa ei ole mitään, palautetaan `null`. Metodin kutsuminen palauttaa putkessa pisimpään olleen olion ja poistaa sen putkesta.
- `public boolean onkoPutkessa()` palauttaa arvon `true` mikäli putkessa on arvoja. Mikäli putki on tyhjä, palauttaa arvon `false`.

Tee luokan sisäinen toteutus ArrayListin avulla.

**Luokalle ei ole tehtäväpohjassa testejä**. Palauta tehtävä kun seuraavat esimerkit toimivat toivotulla tavalla.

```java
Putki<String> putki = new Putki<>();
putki.lisaaPutkeen("dibi");
putki.lisaaPutkeen("dab");
putki.lisaaPutkeen("dab");
putki.lisaaPutkeen("daa");
while(putki.onkoPutkessa()) {
    System.out.println(putki.otaPutkesta());
}
```

<sample-output>

dibi
dab
dab
daa

</sample-output>

```java
Putki<Integer> numeroputki = new Putki<>();
numeroputki.lisaaPutkeen(1);
numeroputki.lisaaPutkeen(2);
numeroputki.lisaaPutkeen(3);

int summa = 0;
while(numeroputki.onkoPutkessa()) {
    summa = summa + numeroputki.otaPutkesta();
}
System.out.println(summa);
System.out.println(numeroputki.otaPutkesta());
```

<sample-output>

6
null

</sample-output>

