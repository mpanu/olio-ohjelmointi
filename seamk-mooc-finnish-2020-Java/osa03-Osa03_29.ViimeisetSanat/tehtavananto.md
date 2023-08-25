

Kirjoita ohjelma, joka lukee käyttäjältä merkkijonoja. Mikäli syötetty merkkijono on tyhjä, ohjelma ei jatka lukemista ja ohjelman suoritus päättyy. Mikäli merkkijono ei ole tyhjä, ohjelma pilkkoo syötetyn merkkijonon osiksi välilyöntien ` ` kohdalta ja tulostaa kunkin pilkotun merkkijonon viimeisen osan.

<sample-output>

**yksi kaksi kolme neljä**
neljä
**viestin purku tässä selvä**
selvä

</sample-output>


Vinkki: saat taulukon pituuden selville seuraavalla tavalla:

```java
String[] osat = {"eka", "toka", "kolmas"};
System.out.println("Osia yhteensä: " + osat.length);
```

<sample-output>

Osia yhteensä: 3

</sample-output>

