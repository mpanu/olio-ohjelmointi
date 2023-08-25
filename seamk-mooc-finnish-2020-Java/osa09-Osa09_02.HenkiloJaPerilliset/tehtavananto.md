


<h2>Henkilo</h2>

Luo luokka `Henkilo`. Luokan tulee toimia seuraavan esimerkin mukaisesti.


```java
Henkilo ada = new Henkilo("Ada Lovelace", "Korsontie 1 03100 Vantaa");
Henkilo esko = new Henkilo("Esko Ukkonen", "Mannerheimintie 15 00100 Helsinki");
System.out.println(ada);
System.out.println(esko);
```

<sample-output>
Ada Lovelace
  Korsontie 1 03100 Vantaa
Esko Ukkonen
  Mannerheimintie 15 00100 Helsinki
</sample-output>


<h2>Opiskelija</h2>


Luo luokka `Opiskelija` joka perii luokan `Henkilo`.


Opiskelijalla on aluksi 0 opintopistettä. Aina kun opiskelija opiskelee, opintopistemäärä kasvaa. Luokan tulee toimia seuraavan esimerkin mukaisesti.


```java
Opiskelija olli = new Opiskelija("Olli", "Ida Albergintie 1 00400 Helsinki");
System.out.println(olli);
System.out.println("opintopisteitä " + olli.opintopisteita());
olli.opiskele();
System.out.println("opintopisteitä "+ olli.opintopisteita());
```

<sample-output>
Olli
  Ida Albergintie 1 00400 Helsinki
opintopisteitä 0
opintopisteitä 1
</sample-output>


<h2>Opiskelijalle toString</h2>

Edellisessä tehtävässä `Opiskelija` perii toString-metodin luokalta `Henkilo`. Perityn metodin voi myös ylikirjoittaa, eli korvata omalla versiolla. Tee luokalle Opiskelija oma versio toString-metodista. Metodin tulee toimia seuraavan esimerkin mukaisesti.


```java
Opiskelija olli = new Opiskelija("Olli", "Ida Albergintie 1 00400 Helsinki");
System.out.println(olli);
olli.opiskele();
System.out.println(olli);
```

<sample-output>
Olli
  Ida Albergintie 1 00400 Helsinki
  opintopisteitä 0
Olli
  Ida Albergintie 1 00400 Helsinki
  opintopisteitä 1
</sample-output>


<h2>Opettaja</h2>


Luo luokan Henkilo perivä luokka Opettaja. Opettajalla on palkka joka tulostuu opettajan merkkijonoesityksessä.


Luokan tulee toimia seuraavan esimerkin mukaisesti.

```java
Opettaja ada = new Opettaja("Ada Lovelace", "Korsontie 1 03100 Vantaa", 1200);
Opettaja esko = new Opettaja("Esko Ukkonen", "Mannerheimintie 15 00100 Helsinki", 5400);
System.out.println(ada);
System.out.println(esko);

Opiskelija olli = new Opiskelija("Olli", "Ida Albergintie 1 00400 Helsinki");

int i = 0;
while (i < 25) {
  olli.opiskele();
  i = i + 1;
}
System.out.println(olli);
```

<sample-output>
Ada Lovelace
  Korsontie 1 03100 Vantaa
  palkka 1200 euroa/kk
Esko Ukkonen
  Mannerheimintie 15 00100 Helsinki
  palkka 5400 euroa/kk
Olli
  Ida Albergintie 1 00400 Helsinki
  opintopisteitä 25
</sample-output>


<h2>Kaikki Henkilot listalle</h2>


Toteuta pääohjelmaluokkaan `Main` luokkametodi `public static void tulostaHenkilot(ArrayList<Henkilo> henkilot)`, joka tulostaa kaikki metodille parametrina annetussa listassa olevat henkilöt. Metodin tulee toimia seuraavasti `main`-metodista kutsuttaessa.


```java
public static void main(String[] args) {
    ArrayList<Henkilo> henkilot = new ArrayList<Henkilo>();
    henkilot.add(new Opettaja("Ada Lovelace", "Korsontie 1 03100 Vantaa", 1200));
    henkilot.add(new Opiskelija("Olli", "Ida Albergintie 1 00400 Helsinki"));

    tulostaHenkilot(henkilot);
}
```

<sample-output>
Ada Lovelace
  Korsontie 1 03100 Vantaa
  palkka 1200 euroa/kk
Olli
  Ida Albergintie 1 00400 Helsinki
  opintopisteitä 0
</sample-output>

