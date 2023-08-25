


Toteuta luokka Piilo, jolla on yksi geneerinen tyyppiparametri. Luokasta tehdyssä oliossa voi olla yksi olio kerralaan piilossa. Luokan tulee tarjota parametriton konstruktori sekä seuraavat kolme metodia:


- `public void laitaPiiloon(T piilotettava)` laittaa piiloon luokan tyyppiparametrin mukaisen olion. Mikäli piilossa on jo olio, vanha olio katoaa.
- `public T otaPiilosta()` ottaa piilosta luokan tyyppiparametrin mukaisen olion. Mikäli piilossa ei ole mitään, palautetaan `null`. Metodin kutsuminen palauttaa piilossa olevan olion ja poistaa olion piilosta.
- `public boolean onkoPiilossa()` palauttaa arvon `true` mikäli piilossa on olio. Mikäli piilossa ei ole oliota, palauttaa arvon `false`.

**Luokalle ei ole tehtäväpohjassa testejä**. Palauta tehtävä kun seuraavat esimerkit toimivat toivotulla tavalla.


```java
Piilo<String> jemma = new Piilo<>();
System.out.println(jemma.onkoPiilossa());
jemma.laitaPiiloon("kukkuu");
System.out.println(jemma.onkoPiilossa());
System.out.println(jemma.otaPiilosta());
System.out.println(jemma.onkoPiilossa());
jemma.laitaPiiloon("kukkuluuruu");
jemma.laitaPiiloon("huhuu");
System.out.println(jemma.onkoPiilossa());
System.out.println(jemma.otaPiilosta());
System.out.println(jemma.onkoPiilossa());
```

<sample-output>

false
true
kukkuu
false
true
huhuu
false

</sample-output>

```java
Piilo<Integer> jemma = new Piilo<>();
System.out.println(jemma.onkoPiilossa());
jemma.laitaPiiloon(1);
System.out.println(jemma.onkoPiilossa());
System.out.println(jemma.onkoPiilossa());
System.out.println(jemma.otaPiilosta());
System.out.println(jemma.onkoPiilossa());
```

<sample-output>

false
true
true
1
false

</sample-output>

