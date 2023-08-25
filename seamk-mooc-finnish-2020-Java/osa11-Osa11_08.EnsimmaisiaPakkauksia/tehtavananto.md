


<h2>Käyttöliittymä-rajapinta</h2>

Tehtäväpohjassa on valmiina pakkaus `mooc`. Rakennetaan tämän pakkauksen sisälle sovelluksen toiminta. Lisää pakkaukseen mooc pakkaus `ui` (tämän jälkeen käytössä pitäisi olla pakkaus `mooc.ui`), ja lisää sinne rajapinta `Kayttoliittyma`.

Rajapinnan `Kayttoliittyma` tulee määritellä metodi `void paivita()`.


<h2>Tekstikäyttöliittymä</h2>

Luo samaan pakkaukseen luokka `Tekstikayttoliittyma`, joka toteuttaa rajapinnan `Kayttoliittyma`. Toteuta luokassa `Tekstikayttoliittyma` rajapinnan `Kayttoliittyma` vaatima metodi `public void paivita()` siten, että sen ainut tehtävä on merkkijonon "`Päivitetään käyttöliittymää`"-tulostaminen `System.out.println`-metodikutsulla.


<h2>Sovelluslogiikka</h2>

Luo tämän jälkeen pakkaus `mooc.logiikka`, ja lisää sinne luokka `Sovelluslogiikka`. Sovelluslogiikan tarjoaman toiminnallisuuden tulee olla seuraavanlainen.


- `public Sovelluslogiikka(Kayttoliittyma kayttoliittyma)`<br/>Sovelluslogiikka-luokan konstruktori. Saa parametrina Kayttoliittyma-rajapinnan toteuttavan luokan. Huom: jotta sovelluslogiikka näkisi rajapinnan, on sen "importoitava" se, eli tarvitset tiedoston alkuun rivin `import mooc.ui.Kayttoliittyma;`


- `public void suorita(int montaKertaa)`<br/>Tulostaa `montaKertaa`-muuttujan määrittelemän määrän merkkijonoa "Sovelluslogiikka toimii". Jokaisen "Sovelluslogiikka toimii"-tulostuksen jälkeen tulee kutsua konstruktorin parametrina saadun rajapinnan `Kayttoliittyma`-toteuttaman olion määrittelemää `paivita()`-metodia.


Voit testata sovelluksen toimintaa seuraavalla pääohjelmaluokalla.


```java
import mooc.logiikka.Sovelluslogiikka;
import mooc.ui.Kayttoliittyma;
import mooc.ui.Tekstikayttoliittyma;

public class Main {

    public static void main(String[] args) {
        Kayttoliittyma kayttoliittyma = new Tekstikayttoliittyma();
        new Sovelluslogiikka(kayttoliittyma).suorita(3);
    }
}
```

<sample-output>

Sovelluslogiikka toimii
Päivitetään käyttöliittymää
Sovelluslogiikka toimii
Päivitetään käyttöliittymää
Sovelluslogiikka toimii
Päivitetään käyttöliittymää

</sample-output>

