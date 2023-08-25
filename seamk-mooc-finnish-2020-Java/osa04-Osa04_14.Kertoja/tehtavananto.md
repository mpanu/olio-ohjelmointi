

Luo luokka `Kertoja` jolla on:

- Konstruktori `public Kertoja(int luku)`.
- Metodi `public int kerro(int luku)` joka palauttaa sille annetun luvun `luku` kerrottuna konstruktorille annetulla luvulla `luku`.

Tarvinnet tässä myös oliomuuttujan...

Esimerkki luokan käytöstä:

```java
Kertoja kolmellaKertoja = new Kertoja(3);

System.out.println("kolmellaKertoja.kerro(2): " + kolmellaKertoja.kerro(2));

Kertoja neljallaKertoja = new Kertoja(4);

System.out.println("neljallaKertoja.kerro(2): " + neljallaKertoja.kerro(2));
System.out.println("kolmellaKertoja.kerro(1): " + kolmellaKertoja.kerro(1));
System.out.println("neljallaKertoja.kerro(1): " + neljallaKertoja.kerro(1));
```

Tulostus

<sample-output>

kolmellaKertoja.kerro(2): 6
neljallaKertoja.kerro(2): 8
kolmellaKertoja.kerro(1): 3
neljallaKertoja.kerro(1): 4

</sample-output>

