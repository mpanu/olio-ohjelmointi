


Tehtäväpohjassa tulee kaksi luokkaa, `Henkilo` ja `Lemmikki`. Jokaisella henkilöllä on yksi lemmikki. Täydennä luokan `Henkilo` metodia `public String toString` siten, että metodi palauttaa merkkijonon, joka kertoo henkilön nimen lisäksi lemmikin nimen ja rodun.


```java
Lemmikki hulda = new Lemmikki("Hulda", "sekarotuinen koira");
Henkilo leevi = new Henkilo("Leevi", hulda);

System.out.println(leevi);
```

<sample-output>

Leevi, kaverina Hulda, joka on sekarotuinen koira

</sample-output>

