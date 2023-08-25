

Kirjoita ohjelma, joka lukee käyttäjältä merkkijonoja. Mikäli syötetty merkkijono on tyhjä, ohjelma lopettaa käyttäjältä lukemisen ja ohjelman suoritus päättyy. Mikäli merkkijono ei ole tyhjä, ohjelma pilkkoo syötetyn merkkijonon osiksi välilyöntien ` ` kohdalta ja tulostaa omille riveilleen pilkotusta merkkijonosta ne merkkijonot (merkkijonon osat), joissa esiintyy merkkijono `av`.


<sample-output>

**java on ohjelmointikieli**
java
**avaa ovi!**
avaa

</sample-output>

<sample-output>

**aivot avaavat ovia**
avaavat
**tavat sinua kaunistavat**
tavat
kaunistavat
**was it a cat i saw**

</sample-output>

Vinkki: Merkkijonolla on metodi `contains`, jolla voit tarkastaa esiintyykö jokin merkkijono merkkijonossa. Metodi toimii seuraavasti.

```java
String merkkijono = "saippuakauppias";

if (merkkijono.contains("aka")) {
    System.out.println("aka löytyi");
}

if (!merkkijono.contains("hiisi")) {
    System.out.println("hiisi ei löytynyt");
}
```

<sample-output>

aka löytyi
hiisi ei löytynyt

</sample-output>

