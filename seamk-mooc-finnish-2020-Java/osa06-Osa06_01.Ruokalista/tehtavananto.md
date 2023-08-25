

Kumpulan kampuksella Helsingissä toimivaan Unicafe-nimiseen gourmet-ravintolaan tarvitaan uusi ruokalista. Keittiömestari tietää ohjelmoinnista, ja haluaa listan hallinnointiin tietokonejärjestelmän. Toteutetaan tässä tehtävässä järjestelmän sydän, luokka Ruokalista.

Tehtäväpohjan mukana tulee `Main`-luokka, jossa voit testata ruokalistan toimintaa. Ruokalistan toteuttamista varten saat seuraavanlaisen tehtäväpohjan:


```java
import java.util.ArrayList;

public class Ruokalista {

    private ArrayList<String> ateriat;

    public Ruokalista() {
        this.ateriat = new ArrayList<>();
    }

    // toteuta tänne tarvittavat metodit
}
```

Ruokalistaoliolla on oliomuuttujana ArrayList, jonka on tarkoitus tallentaa ruokalistalla olevien ruokalajien nimet. Ruokalistan tulee tarjota seuraavat metodit:

- `public void lisaaAteria(String ateria)` lisää aterian ruokalistalle. Mikäli ateria on jo listalla, sitä ei lisätä uudestaan.

- `public void tulostaAteriat()` tulostaa ateriat.

- `public void tyhjennaRuokalista()` tyhjentää ruokalistan.

Kun ruokalista on valmis, sitä voi käyttää seuraavalla tavalla.

```java
Ruokalista menu = new Ruokalista();
menu.lisaaAteria("Tofuratatouille");
menu.lisaaAteria("Chili-kookoskana");
menu.lisaaAteria("Chili-kookoskana");
menu.lisaaAteria("Lihapyörykät sinappikastikeella");

menu.tulostaAteriat();
menu.tyhjennaRuokalista();

System.out.println();
menu.lisaaAteria("Tomaatti-mozzarellasalaatti");
menu.tulostaAteriat();
```

<sample-output>

Tofuratatouille
Chili-kookoskana
Lihapyörykät sinappikastikeella

Tomaatti-mozzarellasalaatti

</sample-output>


<h2>Aterian lisääminen</h2>

Toteuta metodi `public void lisaaAteria(String ateria)`, joka lisää uuden aterian listalle `ateriat`. Jos lisättävä ateria on jo listalla, sitä ei tule lisätä uudelleen. Listan metodi `contains` on näppärä olemassaolon tarkastamiseen.


<h2>Aterioiden tulostaminen</h2>

Toteuta metodi `public void tulostaAteriat()`, joka tulostaa ateriat. Voit kokeilla ohjelmaa seuraavalla esimerkkikoodilla.


```java
Ruokalista menu = new Ruokalista();
menu.lisaaAteria("Tofuratatouille");
menu.lisaaAteria("Chili-kookoskana");
menu.lisaaAteria("Chili-kookoskana");
menu.lisaaAteria("Lihapyörykät sinappikastikeella");

menu.tulostaAteriat();
```

<sample-output>

Tofuratatouille
Chili-kookoskana
Lihapyörykät sinappikastikeella

</sample-output>


<h2>Ruokalistan tyhjentäminen</h2>

Toteuta metodi `public void tyhjennaRuokalista()` joka tyhjentää ruokalistan. `ArrayList`-luokalla on metodi josta on tässä hyötyä. NetBeans osaa vihjata käytettävissä olevista metodeista kun kirjoitat olion nimen ja pisteen. Yritä kirjoittaa `ateriat.` metodirungon sisällä ja katso mitä käy.

Kun ruokalista on valmis, kokeile sitä seuraavalla esimerkkikoodilla.

```java
Ruokalista menu = new Ruokalista();
menu.lisaaAteria("Tofuratatouille");
menu.lisaaAteria("Chili-kookoskana");
menu.lisaaAteria("Chili-kookoskana");
menu.lisaaAteria("Lihapyörykät sinappikastikeella");

menu.tulostaAteriat();
menu.tyhjennaRuokalista();

System.out.println();
menu.lisaaAteria("Tomaatti-mozzarellasalaatti");
menu.tulostaAteriat();
```

<sample-output>

Tofuratatouille
Chili-kookoskana
Lihapyörykät sinappikastikeella

Tomaatti-mozzarellasalaatti

</sample-output>


