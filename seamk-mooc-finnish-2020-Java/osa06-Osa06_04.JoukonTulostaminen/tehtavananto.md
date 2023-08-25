

Tehtäväpohjassa on valmiina luokka `Joukko`, jota käytetään arvoja sisältävän joukon kuvaamiseen. Luokalta puuttuu tulostamiseen käytettävä `toString`-metodi.

Toteuta luokalle `toString`-metodi, jonka avulla tulostus toimii seuraavien esimerkkien kuvaamalla tavalla.


```java
Joukko j = new Joukko("aakkoset");
System.out.println(j);

System.out.println();

j.lisaa("a");
System.out.println(j);

System.out.println();

j.lisaa("b");
System.out.println(j);

System.out.println();

j.lisaa("c");
System.out.println(j);
```

<sample-output>

Joukko aakkoset on tyhjä.

Joukossa aakkoset on 1 alkio:
a

Joukossa aakkoset on 2 alkiota:
a
b

Joukossa aakkoset on 3 alkiota:
a
b
c

</sample-output>


```java
Joukko j = new Joukko("hahmot");
System.out.println(j);

System.out.println();

j.lisaa("magneto");
System.out.println(j);

System.out.println();

j.lisaa("mystique");
System.out.println(j);

System.out.println();

j.lisaa("phoenix");
System.out.println(j);
```

<sample-output>

Joukko hahmot on tyhjä.

Joukossa hahmot on 1 alkio:
magneto

Joukossa hahmot on 2 alkiota:
magneto
mystique

Joukossa hahmot on 3 alkiota:
magneto
mystique
phoenix

</sample-output>

