

Tehtäväpohjassa on määriteltynä luokka Agentti, jolla on etunimi ja sukunimi. Luokalle on määritelty metodi `tulosta`, joka luo seuraavanlaisen merkkijonoesityksen.

```java
Agentti bond = new Agentti("James", "Bond");
bond.tulosta();
```

<sample-output>

My name is Bond, James Bond

</sample-output>

Poista luokan metodi `tulosta` ja luo luokalle metodi `public String toString()`, joka palauttaa edellämainitun merkkijonoesityksen.

Luokan tulee toimia jatkossa seuraavasti.

```java
Agentti bond = new Agentti("James", "Bond");

bond.toString(); // ei tulosta mitään
System.out.println(bond);

Agentti ionic = new Agentti("Ionic", "Bond");
System.out.println(ionic);
```

<sample-output>

My name is Bond, James Bond
My name is Bond, Ionic Bond

</sample-output>

