

Tehtäväpohjassa on valmiina luokka `Henkilo`. Henkilöllä on nimi ja pituus. Toteutetaan tässä tehtävässä luokka `Huone`, jonne voi lisätä henkilöitä, ja jota voi käyttää henkilöiden pituusjärjestykseen asettamiseen -- henkilön ottaminen huoneesta palauttaa aina lyhyimmän henkilön.

Luokka tulee lopulta toimimaan seuraavalla tavalla.


<h2>Huone</h2>

Luo luokka `Huone`. Luokan `Huone` tulee sisältää oliomuuttujana listan henkilöitä, ja sillä tulee olla parametriton konstruktori. Lisää luokalle myös seuraavat metodit:

- `public void lisaa(Henkilo henkilo)` - lisää huoneeseen parametrina annetun henkilön.

- `public boolean onTyhja()` - palauttaa `boolean`-tyyppisen arvon `true` tai `false`, joka kertoo onko huone tyhjä.

- `public ArrayList<Henkilo> getHenkilot()` - palauttaa listan huoneessa olevista henkilöistä.

```java
Huone huone = new Huone();
System.out.println("Huone tyhjä? " + huone.onTyhja());
huone.lisaa(new Henkilo("Lea", 183));
huone.lisaa(new Henkilo("Kenya", 182));
huone.lisaa(new Henkilo("Auli", 186));
huone.lisaa(new Henkilo("Nina", 172));
huone.lisaa(new Henkilo("Terhi", 185));
System.out.println("Huone tyhjä? " + huone.onTyhja());

System.out.println("");
for (Henkilo henkilo : huone.getHenkilot()) {
    System.out.println(henkilo);
}
```

<sample-output>

Huone tyhjä? true
Huone tyhjä? false

Lea (183 cm)
Kenya (182 cm)
Auli (186 cm)
Nina (172 cm)
Terhi (185 cm)

</sample-output>


<h2>Lyhin henkilö</h2>

Lisää luokalle `Huone` metodi `public Henkilo lyhin()`, joka palauttaa huoneeseen lisätyistä henkilöistä lyhimmän. Mikäli huone on tyhjä, palauttaa `null`-viitteen. Metodin ei tule poistaa henkilöä huoneesta.


```java
Huone huone = new Huone();
System.out.println("Lyhin: " + huone.lyhin());
System.out.println("Huone tyhjä? " + huone.onTyhja());
huone.lisaa(new Henkilo("Lea", 183));
huone.lisaa(new Henkilo("Kenya", 182));
huone.lisaa(new Henkilo("Auli", 186));
huone.lisaa(new Henkilo("Nina", 172));
huone.lisaa(new Henkilo("Terhi", 185));
System.out.println("Huone tyhjä? " + huone.onTyhja());

System.out.println("");
for (Henkilo henkilo : huone.getHenkilot()) {
    System.out.println(henkilo);
}

System.out.println();
System.out.println("Lyhin: " + huone.lyhin());
System.out.println("");
for (Henkilo henkilo : huone.getHenkilot()) {
    System.out.println(henkilo);
}
```

<sample-output>

Lyhin: null
Huone tyhjä? true
Huone tyhjä? false

Lea (183 cm)
Kenya (182 cm)
Auli (186 cm)
Nina (172 cm)
Terhi (185 cm)

Lyhin: Nina (172 cm)

Lea (183 cm)
Kenya (182 cm)
Auli (186 cm)
Nina (172 cm)
Terhi (185 cm)

</sample-output>


<h2>Huoneesta ottaminen</h2>

Lisää luokalle `Huone` metodi `public Henkilo ota()`, ottaa huoneesta lyhimmän henkilön. Mikäli huone on tyhjä, metodi palauttaa `null`-viitteen.

```java
Huone huone = new Huone();
huone.lisaa(new Henkilo("Lea", 183));
huone.lisaa(new Henkilo("Kenya", 182));
huone.lisaa(new Henkilo("Auli", 186));
huone.lisaa(new Henkilo("Nina", 172));
huone.lisaa(new Henkilo("Terhi", 185));

System.out.println("");
for (Henkilo henkilo : huone.getHenkilot()) {
    System.out.println(henkilo);
}

System.out.println();
System.out.println("Lyhin: " + huone.ota());
System.out.println("");
for (Henkilo henkilo : huone.getHenkilot()) {
    System.out.println(henkilo);
}
```

<sample-output>

Lea (183 cm)
Kenya (182 cm)
Auli (186 cm)
Nina (172 cm)
Terhi (185 cm)

Lyhin: Nina (172 cm)

Lea (183 cm)
Kenya (182 cm)
Auli (186 cm)
Terhi (185 cm)

</sample-output>

Nyt henkilöt saadaan haluttaessa tulostettua myös pituusjärjestyksessä.

```java
Huone huone = new Huone();
huone.lisaa(new Henkilo("Lea", 183));
huone.lisaa(new Henkilo("Kenya", 182));
huone.lisaa(new Henkilo("Auli", 186));
huone.lisaa(new Henkilo("Nina", 172));
huone.lisaa(new Henkilo("Terhi", 185));

while (!huone.onTyhja()) {
    System.out.println(huone.ota());
}
```

<sample-output>

Nina (172 cm)
Kenya (182 cm)
Lea (183 cm)
Terhi (185 cm)
Auli (186 cm)

</sample-output>

