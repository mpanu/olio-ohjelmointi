

Pakka on tietorakenne, johon voi lisätä ja josta voi ottaa. Aina päälle tai päältä.

<h2>Pakkaan lisääminen ja tyhjyyden tarkastaminen</h2>

Luo luokka `Pakka`, jolla on oliomuuttujana merkkijonoja sisältävä listan. Lisää luokalle seuraavat metodit:

- `public boolean onTyhja()` - palauttaa `boolean`-tyyppisen arvon (true tai false), joka kertoo onko pakka tyhjä.

- `public void lisaa(String arvo)` - lisää pakan päälle parametrina annetun arvon.

- `public ArrayList<String> arvot()` - palauttaa pakan sisältämän arvot listana.

Voit kokeilla luokkaasi seuraavalla koodilla:

```java
Pakka p = new Pakka();
System.out.println(p.onTyhja());
System.out.println(p.arvot());
p.lisaa("Arvo");
System.out.println(p.onTyhja());
System.out.println(p.arvot());
```

<sample-output>

true
[]
false
[Arvo]

</sample-output>


<h2>Pakasta ottaminen</h2>

Lisää luokalle `Pakka` metodi `public String ota()`, joka palauttaa pakan päällimmäisenä olevan arvon (eli pakkaan viimeisenä lisätyn arvon) ja poistaa sen pakasta.

```java
Pakka p = new Pakka();
System.out.println(p.onTyhja());
System.out.println(p.arvot());
p.lisaa("Arvo");
System.out.println(p.onTyhja());
System.out.println(p.arvot());
String otettu = p.ota();
System.out.println(p.onTyhja());
System.out.println(p.arvot());
System.out.println(otettu);
```

<sample-output>

true
[]
false
[Arvo]
true
[]
Arvo

</sample-output>

```java
Pakka p = new Pakka();
p.lisaa("1");
p.lisaa("2");
p.lisaa("3");
p.lisaa("4");
p.lisaa("5");

while (!p.onTyhja()) {
    System.out.println(p.ota());
}
```

<sample-output>

5
4
3
2
1

</sample-output>

Vinkki! Kun ArrayListiin lisätään arvo, se menee listan loppuun. Viimeksi lisätty arvo on siis listan viimeisessä indeksissä -- listan tarjoamasta `size`-metodista on hyötyä viimeisen indeksin selvittämisessä. Poistaminen tietystä indeksistä onnistuu listan tarjoaman `remove`-metodin avulla.

