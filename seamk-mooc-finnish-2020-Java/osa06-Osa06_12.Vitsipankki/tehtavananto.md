

Tehtäväpohjassa on valmiina seuraava "mainiin" kirjoitettu sovellus.

```java
Scanner lukija = new Scanner(System.in);
ArrayList<String> vitsit = new ArrayList<>();
System.out.println("Voihan vitsi!");

while (true) {
    System.out.println("Komennot:");
    System.out.println(" 1 - lisää vitsi");
    System.out.println(" 2 - arvo vitsi");
    System.out.println(" 3 - listaa vitsit");
    System.out.println(" X - lopeta");

    String komento = lukija.nextLine();

    if (komento.equals("X")) {
        break;
    }

    if (komento.equals("1")) {
        System.out.println("Kirjoita lisättävä vitsi:");
        String vitsi = lukija.nextLine();
        vitsit.add(vitsi);
    } else if (komento.equals("2")) {
        System.out.println("Arvotaan vitsi.");

        if (vitsit.isEmpty()) {
            System.out.println("Vitsit vähissä.");
        } else {
            Random arpa = new Random();
            int indeksi = arpa.nextInt(vitsit.size());
            System.out.println(vitsit.get(indeksi));
        }

    } else if (komento.equals("3")) {
        System.out.println("Tulostetaan vitsit.");
        for (String vitsi : vitsit) {
            System.out.println(vitsi);
        }
    }
}
```

Sovellus on käytännössä vitsipankki. Vitsipankkiin voi lisätä vitsejä, vitsipankista voi arpoa vitsejä, ja vitsipankissa olevat vitsit voidaan tulostaa. Tässä tehtävässä sovellus pilkotaan osiin ohjatusti.

<h2>Vitsipankki</h2>

Luo luokka `Vitsipankki` ja siirrä sinne vitsien hallinnointiin liittyvä toiminnallisuus. Luokalla tulee olla parametriton konstruktori sekä seuraavat metodit:

- `public void lisaaVitsi(String vitsi)` - lisää vitsin vitsipankkiin.
- `public String arvoVitsi()` - arpoo vitsipankin vitseistä yhden vitsin ja palauttaa sen. Mikäli vitsipankissa ei ole vitsejä, palauttaa merkkijonon "Vitsit vähissä.".
- `public void tulostaVitsit()` - tulostaa vitsipankissa olevat vitsit.

Esimerkki luokan käytöstä:

```java
Vitsipankki pankki = new Vitsipankki();
pankki.lisaaVitsi("Mikä on punaista ja tuoksuu siniselle maalille? - Punainen maali.");
pankki.lisaaVitsi("Mikä on sinistä ja tuoksuu punaiselle maalille? - Sininen maali.");

System.out.println("Arvotaan vitsejä:");
for (int i = 0; i < 5; i++) {
    System.out.println(pankki.arvoVitsi());
}

System.out.println("");
System.out.println("Tulostetaan vitsit:");
pankki.tulostaVitsit();
```

Alla ohjelman mahdollinen tulostus. Huomaa, että arvotut vitsit eivät todennäköisesti tulostu alla kuvatun esimerkin mukaisesti.

<sample-output>

Arvotaan vitsejä:
Mikä on sinistä ja tuoksuu punaiselle maalille? - Sininen maali.
Mikä on punaista ja tuoksuu siniselle maalille? - Punainen maali.
Mikä on sinistä ja tuoksuu punaiselle maalille? - Sininen maali.
Mikä on sinistä ja tuoksuu punaiselle maalille? - Sininen maali.
Mikä on sinistä ja tuoksuu punaiselle maalille? - Sininen maali.

Tulostetaan vitsit:
Mikä on punaista ja tuoksuu siniselle maalille? - Punainen maali.
Mikä on sinistä ja tuoksuu punaiselle maalille? - Sininen maali.

</sample-output>


<h2>Käyttöliittymä</h2>

Luo luokka `Kayttoliittyma` ja siirrä sinne sovelluksen käyttöliittymätoiminnallisuus. Luokalla tulee olla kaksiparametrinen konstruktori. Ensimmäisenä parametrina annetaan Vitsipankki-luokan ilmentymä, ja toisena parametrina Scanner-luokan ilmentymä. Tämän lisäksi luokalla tulee olla metodi `public void kaynnista()`, joka käynnistää käyttöliittymän.

Käyttöliittymän tulee tarjota seuraavat komennot:

- `X` - lopettaminen: poistuu metodista `kaynnista`.
- `1` - lisääminen: kysyy käyttäjältä vitsipankkiin lisättävää vitsiä ja lisää käyttäjän syöttämän vitsin vitsipankkiin.
- `2` - arpominen: arpoo vitsipankista vitsin ja tulostaa sen. Mikäli vitsipankissa ei ole vitsejä, tulostaa merkkijonon "Vitsit vähissä.".
- `3` - tulostaminen: tulostaa kaikki vitsipankissa olevat vitsit.

Esimerkki käyttöliittymän käytöstä:

```java
Vitsipankki pankki = new Vitsipankki();
Scanner lukija = new Scanner(System.in);

Kayttoliittyma liittyma = new Kayttoliittyma(pankki, lukija);
liittyma.kaynnista();
```

<sample-output>

Komennot:
 1 - lisää vitsi
 2 - arvo vitsi
 3 - listaa vitsit
 X - lopeta
**1**
Kirjoita lisättävä vitsi:
**Did you hear about the claustrophobic astronaut? -- He just needed a little space.**
Komennot:
 1 - lisää vitsi
 2 - arvo vitsi
 3 - listaa vitsit
 X - lopeta
**3**
Tulostetaan vitsit.
Did you hear about the claustrophobic astronaut? -- He just needed a little space.
Komennot:
 1 - lisää vitsi
 2 - arvo vitsi
 3 - listaa vitsit
 X - lopeta
**X**

</sample-output>

