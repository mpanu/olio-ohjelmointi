


<h2>Tähtien tulostus</h2>

Tee metodi `tulostaTahtia`, joka tulostaa annetun määrän tähtiä ja rivinvaihdon.

Tee metodi seuraavaan runkoon:

```java
public static void tulostaTahtia(int maara) {
    // yhden tähden saat tulostettua komennolla
    // System.out.print("*");
    // kutsu tulostuskomentoa n kertaa
    // tulosta lopuksi rivinvaihto komennolla
    // System.out.println("");
}

public static void main(String[] args) {
    tulostaTahtia(5);
    tulostaTahtia(3);
    tulostaTahtia(9);
}
```

Ohjelman tulostus:

<sample-output>
*****
***
*********
</sample-output>

**Huom:** moniosaisen tehtävät voi palauttaa palvelimelle (painamalla testausnapin oikealla puolella olevaa nappia) vaikka kaikki osat eivät olisikaan tehty. Palvelin valittelee tällöin tekemättömien osien testeistä, tehdyt osat palvelin kirjaa.


<h2>Neliön tulostus</h2>

Tee metodi `tulostaNelio(int sivunpituus)` joka tulostaa neliön käyttäen `tulostaTahtia`-metodia. Siis esimerkiksi kutsu `tulostaNelio(4)` tulostaa seuraavaa:

<sample-output>
****
****
****
****
</sample-output>

**Huom:** tehtävässä ei riitä että tulostus näyttää oikealta, tulostaNelio-metodin sisällä neliön "rivien" tulostus tulee tehdä tulostaTahtia-metodia käyttäen.

Ohjelmaa tehdessäsi kannattaa varmistaa main:iin kirjoitetun testikoodin avulla että metodit toimivat vaaditulla tavalla.


<h2>Suorakulmion tulostus</h2>

Tee metodi `tulostaSuorakulmio(int leveys, int korkeus)` joka tulostaa suorakulmion käyttäen `tulostaTahtia`-metodia. Siis esimerkiksi kutsu `tulostaSuorakulmio(17,3)` tulostaa seuraavaa:

<sample-output>
*****************
*****************
*****************
</sample-output>


<h2>Vasemmalle nojaavan kolmion tulostus</h2>

Tee metodi `tulostaKolmio(int koko)` joka tulostaa kolmion käyttäen `tulostaTahtia`-metodia. Siis esimerkiksi kutsu `tulostaKolmio(4)` tulostaa seuraavaa:

<sample-output>
*
**
***
****
</sample-output>

