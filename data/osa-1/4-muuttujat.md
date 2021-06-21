---
path: "/osa-1/4-muuttujat"
title: "Muuttujat"
hidden: false
---

<text-box variant='learningObjectives' name='Oppimistavoitteet'>

- Tunnet käsitteen muuttuja. Tiedät mitä ovat muuttujan tyyppi, muuttujan nimi, ja muuttujan arvo.
- Osaat luoda ja käsitellä merkkijono-, kokonaisluku-, liukuluku-, ja totuusarvomuuttujia.

</text-box>

<ab-study id="1a2faee2-7287-4277-ac4a-329220042a27">

<only-for-ab-group group="1">

<text-box variant="hint" name="Median ja tekniikan käyttöön liittyvä kysely">
Tässä kohtaa vastaat median ja tekniikan käyttöön liittyvään kyselyyn. Kyselyllä kartoitetaan median ja tekniikan käyttöä sekä näihin suhtautumista. Kyselyn vastauksia käytetään osana Ohjelmoinnin MOOC -kurssin kehitystä sekä kurssiin ja oppimiseen liittyvää tutkimusta. <google-form-link href="https://docs.google.com/forms/d/e/1FAIpQLSdRWwKpDzcR7PHtSmeL4o8-JOXyR5ajAeuHz2aw4gnMTikwLg/viewform?usp=pp_url" emailfieldname="entry.575150039">Avaa kysely tätä linkkiä klikkaamalla</google-form-link>.
</text-box>

</only-for-ab-group>

<only-for-ab-group group="2">

<text-box variant="hint" name="Median ja tekniikan käyttöön liittyvä kysely">
Tässä kohtaa vastaat median ja tekniikan käyttöön liittyvään kyselyyn. Kyselyllä kartoitetaan median ja tekniikan käyttöä sekä näihin suhtautumista. Kyselyn vastauksia käytetään osana Ohjelmoinnin MOOC -kurssin kehitystä sekä kurssiin ja oppimiseen liittyvää tutkimusta.
<google-form-link href="https://docs.google.com/forms/d/e/1FAIpQLSfKGPCqp-9H8as73RfwqXkdCFbCL-O85TlqJ5tOZYr-MH-eDA/viewform?usp=pp_url" emailfieldname="entry.575150039">Avaa kysely tätä linkkiä klikkaamalla</google-form-link>.
</text-box>

</only-for-ab-group>

</ab-study>

<quiz id="1fce6fab-fcad-5d58-b68b-8faead42d83e"></quiz>


Tutustuimme syötteen lukemisen yhteydessä jo pikaisesti merkkijonomuuttujiin. Tutustutaan seuraavaksi muihin usein käytettyihin Javan muuttujatyyppeihin.

Muuttujaa kannattaa ajatella lokerona, johon voi tallettaa annetun tyyppistä tietoa. Tyyppejä ovat esimerkiksi teksti eli merkkijono (`String`), kokonaisluku (`int`), liukuluku (`double`) eli desimaaliluku, ja totuusarvo (`boolean`). Muuttujaan asetetaan arvo yhtäsuuruusmerkillä (`=`).

```java
int kuukausia = 12;
```

Yllä olevassa lauseessa asetetaan kokonaisluku-tyyppiä (int) olevaan muuttujaan nimeltä kuukausia arvo 12. Lause luetaan "muuttuja kuukausia saa arvon 12".

Muuttujan arvo voidaan yhdistää merkkijonoon +-merkillä seuraavan esimerkin mukaisesti.

```java
String teksti = "sisältää tekstiä";
int kokonaisluku = 123;
double liukuluku = 3.141592653;
boolean totuusarvo = true;

System.out.println("Tekstimuuttuja: " + teksti);
System.out.println("Kokonaislukumuuttuja: " + kokonaisluku);
System.out.println("Liukulukumuuttuja: " + liukuluku);
System.out.println("Totuusarvo: " + totuusarvo);
```

Tulostus:

<sample-output>

Tekstimuuttuja: sisältää tekstiä
Kokonaislukumuuttuja: 123
Liukulukumuuttuja: 3.141592653
Totuusarvo: true

</sample-output>

<programming-exercise name="Muuttuvat muuttujat" tmcname='osa01-Osa01_11.MuuttuvatMuuttujat'>

Tehtäväpohja sisältää ohjelman, joka tulostaa seuraavaa.

<sample-output>

Kanoja:
3
Pekonia (kg):
5.5
Traktori:
Ei ole!

Tässä vielä tiivistelmä:
3
5.5
Ei ole!

</sample-output>

Muuta ohjelmaa annetuista kohdista niin että tuloste on:

<sample-output>

Kanoja:
9000
Pekonia (kg):
0.1
Traktori:
Zetor

Tässä vielä tiivistelmä:
9000
0.1
Zetor

</sample-output>

</programming-exercise>

Muuttujien nimet ovat uniikkeja, eikä kahdella muuttujalla saa olla ohjelmassa samaa nimeä. Seuraavassa esimerkissä oleva ohjelma on virheellinen, koska ohjelmassa yritetään luoda kahteen kertaan muuttujaa nimeltä `pii`. Muuttujan luominen tapahtuu kun muuttuja esitellään ensimmäistä kertaa.

```java
public class Esimerkki {
    public static void main(String[] args) {
        double pii = 3.14;
        double pii = 3.141592653;

        System.out.println("Piin arvo on: " + pii);
    }
}
```

Muuttujan tyyppi kerrotaan kun muuttuja esitellään ensimmäistä kertaa. Kun muuttujaan asetetaan uusi arvo, ei muuttujan tyyppiä enää kerrota.

```java
int luku = 10;
System.out.println(luku);
luku = 4;
System.out.println(luku);
```

<sample-output>

10
4

</sample-output>


## Muuttujaan asetetun arvon muuttaminen

Muuttuja on olemassa sen esittelyhetkestä lähtien, ja sen arvo säilyy kunnes muuttujaan asetetaan toinen arvo. Muuttujan arvon muuttaminen onnistuu lauseella, jossa on muuttujan nimi, yhtäsuuruusmerkki, ja muuttujan uusi arvo. Huomaa että muuttujan tyyppi kirjoitetaan vain kun muuttuja esitellään ohjelmassa ensimmäistä kertaa.



```java
int luku = 123;
System.out.println("Muuttujan arvo on " + luku);

luku = 42;
System.out.println("Muuttujan arvo on " + luku);
```

Tulostus:

<sample-output>

Muuttujan arvo on 123
Muuttujan arvo on 42

</sample-output>

Tarkastellaan edellisen ohjelmakoodin suoritusta askel askeleelta. Kun muuttuja esitellään ohjelmakoodissa ensimmäistä kertaa, eli sekä muuttujan tyyppi (tässä `int`) että sen nimi (tässä `luku`) kerrotaan tietokoneelle, tietokone luo muuttujaa varten "nimetyn lokeron". Tämän jälkeen yhtäsuuruusmerkin oikealla puolella oleva arvo kopioidaan tähän nimettyyn lokeroon.

![](../img/drawings/muuttujan-arvon-vaihto-1.png)

Kun ohjelmakoodissa viitataan muuttujaan sen nimellä -- tässä halutaan tulostaa merkkijono "Muuttujan arvo on " sekä muuttujan `luku` arvo, muuttujan `luku` arvo haetaan sen nimellä löytyvästä lokerosta.

![](../img/drawings/muuttujan-arvon-vaihto-2.png)

Kun muuttujaan asetetaan arvo (tässä `luku = 42`), tarkistetaan ensin löytyykö muuttujan nimistä lokeroa. Jos lokero löytyy, uusi arvo kopioidaan lokeroon vanhan arvon tilalle ja vanha arvo katoaa. Jos muuttujan nimellä ei löydy lokeroa, ohjelman suoritus päättyy virheilmoitukseen tai ohjelmaa ei voida käynnistää.

![](../img/drawings/muuttujan-arvon-vaihto-3.png)

Seuraavaksi ohjelmakoodissa viitataan taas muuttujaan sen nimellä -- tässäkin halutaan tulostaa merkkijono "Muuttujan arvo on " sekä muuttujan `luku` arvo. Toimitaan kuten normaalisti, eli haetaan muuttujan `luku` arvo sen nimellä löytyvästä lokerosta.

![](../img/drawings/muuttujan-arvon-vaihto-4.png)

Kuten huomaat, ohjelman lopputilanteessa muuttujan alkuperäinen arvo on kadonnut. Muuttuja voi sisältää kerrallaan aina vain yhden arvon.

## Muuttujan tyyppi pysyy

Kun muuttujan tyyppi on kertaalleen määritelty, ei sitä voi enää muuttaa. Totuusarvoa ei siis voi esimerkiksi asettaa kokonaislukutyyppiseen muuttujaan, eikä totuusarvomuuttujaan voi asettaa kokonaislukua.

```java
boolean onnistuukoKokonaisLuvunAsetus = false;
onnistuukoKokonaisLuvunAsetus = 42; // Ei onnistu

int luku = 10;
onnistuukoKokonaisLuvunAsetus = luku; // Ei myöskään onnistu
```

Poikkeus kuitenkin löytyy: liukulukutyyppiseen muuttujaan voi asettaa kokonaisluvun, sillä Java osaa muuttaa kokonaisluvun liukuluvuksi asetuksen yhteydessä.

```java
double liukuluku = 0.42;
liukuluku = 1; // Onnistuu

int luku = 10;
liukuluku = luku; // Onnistuu myös

```


Liukulukua ei kuitenkaan voi asettaa kokonaislukuun. Tämä johtuu siitä, että ohjelmointikielen suunnittelijat yrittävät suojella ohjelmoijaa tietoa kadottavilta ohjelmointivirheiltä.

```java
int luku = 4.2; // Ei onnistu

double liukuluku = 0.42;
luku = liukuluku; // Ei myöskään onnistu
```

## Muuttujan nimentä

Muuttujien nimentä on oleellinen osa ohjelman kuvausta. Tarkastellaan kahta esimerkkiä.

```java
double a = 3.14;
double b = 22.0;
double c = a * b * b;

System.out.println(c);
```

<sample-output>

1519.76

</sample-output>

```java
double pii = 3.14;
double sade = 22.0;
double pintaAla = pii * sade * sade;

System.out.println(pintaAla);
```

<sample-output>

1519.76

</sample-output>


Edellä olevat kaksi esimerkkiä sisältävät täsmälleen saman toiminnallisuuden ja tuottavat saman tulostuksen. Toinen esimerkeistä on kuitenkin paljon ymmärrettävämpi. Kyseessä on ympyrän pinta-alan laskevan ohjelman koodi. Ensimmäisellä rivillä määritellään piin arvo, toisella rivillä ympyrän säde, ja kolmannella rivillä lasketaan pinta-ala. Tämän jälkeen pinta-ala tulostetaan.

<text-box variant='hint' name="Muuttujat sanoittavat ohjelmaa ja ratkaistavaa ongelmaa">

Ohjelmointi on ongelmanratkaisuväline. Ohjelmoidessa luodaan ratkaisua jonkinlaiseen ongelmaan kuten autojen automaattiseen ohjaamiseen. Kun ongelmaa ratkaistaan, ohjelmoija päättää termeistä, joilla ongelmaa kuvataan. Tämä termistö, esimerkiksi ohjelmassa käytettävien muuttujien nimet, tulevat kuvaamaan ongelmaa ohjelman parissa tulevaisuudessa työskenteleville.

Kun sanoitat ratkaistavaa ongelmaa, mieti ongelmaan liittyviä käsitteitä ja niitä kuvaavia sanoja. Jos et keksi sopivia termejä, pohdi ensin mitkä sanat eivät ainakaan kuvaa ongelmaa. Valitse tämän jälkeen jonkinlainen termistö -- voit tyypillisesti onneksi parantaa käyttämääsi termistöä myös jälkikäteen.

</text-box>

Muuttujan nimeämistä rajoittavat tietyt ehdot.

Muuttujan nimessä ei saa olla tiettyjä erikoismerkkejä, kuten huutomerkkejä (!). Välilyönti ei ole sallittu, sillä se erottaa komentojen osat toisistaan. Välilyönti kannattaa korvata [camelCase](http://fi.wikipedia.org/wiki/CamelCase "CamelCase – Wikipedia")-tyylillä, jolloin nimi `muistuttaneeKamelia`. **Huom!** Muuttujien nimien ensimmäinen kirjain kirjoitetaan aina pienellä:

```java
int camelCaseMuuttuja = 7;
```

Numeroita voidaan käyttää muuttujan nimessä, kunhan nimi ei ala numerolla. Nimi ei myöskään voi koostua pelkistä numeroista.

```java
int 7muuttuja = 4; // Ei sallittu!
int muuttuja7 = 4; // Sallittu, mutta ei kuvaava muuttujan nimi
```


Muuttujan nimi ei saa olla jo entuudestaan käytössä. Tällaisia nimiä ovat mm. aikaisemmin määritellyt muuttujat ja Javan valmiit komennot, kuten `System.out.print` ja `System.out.println`.

```java
int camelCase = 2;
int camelCase = 5; // Ei sallittu -- muuttuja camelCase on jo käytössä!
```

Muuttujien nimissä ei tule myöskään käyttää ääkkösiä. Voit korvata ääkköset aakkosilla, eli muuta ä -> a ja ö -> o.

### Sallittuja muuttujien nimiä

* kuukaudenViimeinenPaiva = 20
* ensimmainenVuosi = 1952
* nimi = "Essi"

### Virheellisiä muuttujien nimiä

* kuukauden viimeinen päivä = 20
* 1paiva = 1952
* varo! = 1910
* 1920 = 1

## Muuttujan tyyppi kertoo muuttujan mahdollisista arvoista

Muuttujan tyyppi kerrotaan muuttujan esittelyn yhteydessä. Esimerkiksi merkkijonon "teksti" sisältävä merkkijonomuuttuja luodaan lauseella `String merkkijono = "teksti";` ja kokonaisluvun 42 sisältävä kokonaislukumuuttuja luodaan lauseella `int luku = 42;`.

Muuttujan tyyppi määrää arvot, joita muuttuja voi saada. `String`-tyyppiset muuttujat saavat arvokseen merkkijonoja, `int`-tyyppiset muuttujat saavat arvokseen kokonaislukuja, `double`-tyyppiset muuttujat saavat arvokseen liukulukuja, ja `boolean`-tyyppiset muuttujat saavat arvokseen totuusarvoja.

Kunkin tyypin mahdolliset arvot ovat siis rajattuja. Esimerkiksi merkkijonomuuttuja ei voi sisältää kokonaislukuarvoa, eikä liukuluku voi sisältää totuusarvoa. Alla on listattu käyttämillemme muuttujille niiden mahdolliset arvoalueet.


| Tyyppi | Esimerkki | Sallitut arvot |
|--------|-----------|----------------|
| Kokonaisuluku, eli `int` | <span class="singleline-code">`int luku = 4;`</span>| Kokonaislukumuuttuja voi sisältää kokonaislukuja, joiden arvot ovat välillä -2147483648 ja 2147483647. |
| Liukuluku, eli `double` | <span class="singleline-code">`double luku = 4.2;`</span> | Liukulukumuuttuja sisältää desimaalilukuja, joiden suurin mahdollinen arvo on noin 2<sup>1023</sup>  Kun desimaaliluku esitetään liukuluvun avulla, voi luku olla epätarkka;  liukuluvulla ei pysty esittämään mitä tahansa desimaalilukua.  Taustasyihin palataan kurssilla Tietokoneen toiminta. |
| Merkkijono, eli `String` | <span class="singleline-code">`String teksti = "Hei!";`</span> | Merkkijonomuuttuja voi sisältää merkkijonoja. Merkkijonot rajataan hipsuilla. |
| Totuusarvo, eli `boolean` | <span class="singleline-code">`boolean tosi = true;`</span> | Totuusarvomuuttuja sisältää joko arvon `true` eli totta tai arvon `false` eli epätotta. |


## Erityyppisten muuttujien lukeminen käyttäjältä

Ohjelmiemme käyttämissä tekstipohjaisissa käyttöliittymissä syötteen lukeminen käyttäjältä tapahtuu aina merkkijonona, sillä käyttäjä kirjoittaa syötteen tekstinä. Merkkijonon lukeminen käyttäjältä on jo tuttua -- siihen käytetään Scanner-apuvälineen tarjoamaa `nextLine`-komentoa.

```java
import java.util.Scanner;

public class Ohjelma {

    public static void main(String[] args) {
        Scanner lukija = new Scanner(System.in);

        System.out.println("Kirjoita tekstiä ja paina enter ");
        String teksti = lukija.nextLine();
        System.out.println("Kirjoitit " + teksti);
    }
}
```

<sample-output>

Kirjoita tekstiä ja paina enter
**teksti**
Kirjoitit teksti

</sample-output>


Muunlaiset syötteet kuten kokonaisluvut, liukuluvut ja totuusarvot luetaan myös tekstinä, mutta ne muunnetaan Javan tarjoamilla apuvälineillä annetun muuttujan tyyppiseksi.

## Kokonaisluvun lukeminen

Merkkijonon muuntaminen kokonaisluvuksi tapahtuu komennolla `Integer.valueOf`, jolle annetaan parametrina muunnettavan luvun sisältämä merkkijono.

```java
String lukuMerkkijonona = "42";
int luku = Integer.valueOf(lukuMerkkijonona);

System.out.println(luku);
```

<sample-output>

42

</sample-output>

Scanneria käytettäessä lukeminen ja muuntaminen asetetaan yleensä sisäkkäin. Tämä tapahtuu seuraavasti.

```java
import java.util.Scanner;

public class Ohjelma {

    public static void main(String[] args) {
        Scanner lukija = new Scanner(System.in);

        System.out.println("Kirjoita luku ");
        int luku = Integer.valueOf(lukija.nextLine());
        System.out.println("Kirjoitit " + luku);
    }
}
```

<sample-output>

Kirjoita luku
**42**
Kirjoitit 42

</sample-output>


<programming-exercise name="Kokonaisluvun lukeminen" tmcname='osa01-Osa01_12.KokonaisluvunLukeminen'>

Kirjoita ohjelma, joka kysyy käyttäjältä lukua. Tämän jälkeen ohjelma tulostaa käyttäjän syöttämän luvun.

Alla on annettuna ohjelman esimerkkitulostuksia:

<sample-output>

Syötä luku!
**3**
Syötit luvun 3

</sample-output>

<sample-output>

Syötä luku!
**42**
Syötit luvun 42

</sample-output>

</programming-exercise>

Kokeile toteuttamasi ohjelman toimintaa myös syötteillä, jotka eivät ole lukuja. Ohjelman pitäisi hajota, sillä se ei tiedä miten sellaiset syötteet, jotka eivät ole lukuja, pitäisi muuttaa luvuiksi. Opimme Ohjelmoinnin jatkokurssilla menetelmiä muunmuassa tällaisten poikkeustilanteiden käsittelyyn.

### Liukuluvun lukeminen

Merkkijonon muuntaminen liukuluvuksi tapahtuu komennolla `Double.valueOf`, jolle annetaan parametrina muunnettavan luvun sisältämä merkkijono.

```java
String lukuMerkkijonona = "42.42";
double luku = Double.valueOf(lukuMerkkijonona);
System.out.println(luku);
```

<sample-output>

42.42

</sample-output>

Kuten kokonaislukujen tapauksessa, Scanneria käytettäessä lukeminen ja muuntaminen asetetaan yleensä sisäkkäin. Tämä tapahtuu seuraavasti.

```java
import java.util.Scanner;

public class Ohjelma {
    public static void main(String[] args) {
        Scanner lukija = new Scanner(System.in);
        System.out.println("Kirjoita luku ");
        double luku = Double.valueOf(lukija.nextLine());
        System.out.println("Kirjoitit " + luku);
    }
}
```

<sample-output>

Kirjoita luku
**1234.2**
Kirjoitit 1234.2

</sample-output>

Liukulukutyyppiseen muuttujaan voi lukea myös kokonaisluvun. Tällöin luku muunnetaan liukulukutyyppiseksi automaattisesti. Alla oleva esimerkki näyttää edellisen ohjelman toiminnan kun käyttäjä syöttää kokonaisluvun.

<sample-output>

Kirjoita luku
**18**
Kirjoitit 18.0

</sample-output>

<programming-exercise name="Liukuluvun lukeminen" tmcname='osa01-Osa01_13.LiukuluvunLukeminen'>

Kirjoita ohjelma, joka kysyy käyttäjältä liukulukua. Tämän jälkeen ohjelma tulostaa käyttäjän syöttämän luvun.

Alla on annettuna ohjelman esimerkkitulostuksia:

<sample-output>

Syötä luku!
**3.14**
Syötit luvun 3.14

</sample-output>

<sample-output>

Syötä luku!
**2.718**
Syötit luvun 2.718

</sample-output>

</programming-exercise>


### Totuusarvon lukeminen

Merkkijonon muuntaminen kokonaisluvuksi tapahtui komennolla `Integer.valueOf` ja merkkijonon muuntaminen liukuluvuksi tapahtui komennolla `Double.valueOf`. Komento `valueOf` esiintyy myös merkkijonon muuntamisessa totuusarvoksi -- tämä tehdään komennolla `Boolean.valueOf`.

Totuusarvotyyppiset muuttujat voivat saada arvokseen vain `true` eli totta tai `false` eli epätotta. Kun merkkijonoa muunnetaan totuusarvotyyppiseksi, merkkijonon tulee olla "true" mikäli totuusarvon arvoksi halutaan `true`. Kirjoitusasulla ei ole väliä, eli myös "TRue" muuttuu totuusarvoksi `true`. Muut merkkijonot muuntuvat totuusarvoksi `false`.

```java
import java.util.Scanner;

public class Ohjelma {
    public static void main(String[] args) {
        Scanner lukija = new Scanner(System.in);
        System.out.println("Kirjoita totuusarvo ");
        boolean arvo = Boolean.valueOf(lukija.nextLine());
        System.out.println("Kirjoitit " + arvo);
    }
}
```

<sample-output>

Kirjoita totuusarvo
**enpäs!**
Kirjoitit false

</sample-output>

<sample-output>

Kirjoita totuusarvo
**TRUE**
Kirjoitit true

</sample-output>

<sample-output>

Kirjoita totuusarvo
**true**
Kirjoitit true

</sample-output>


<programming-exercise name="Totuusarvon lukeminen" tmcname='osa01-Osa01_14.TotuusarvonLukeminen'>

Kirjoita ohjelma, joka kysyy käyttäjältä totuusarvoa. Tämän jälkeen ohjelma tulostaa käyttäjän syöttämän totuusarvon.

Alla on annettuna ohjelman esimerkkitulostuksia:

<sample-output>

Syötä jotain!
**joulupukkia ei ole olemassa**
Totta vaiko ei? false

</sample-output>

<sample-output>

Syötä jotain!
**TRUE**
Totta vaiko ei? true

</sample-output>

</programming-exercise>


### Yhteenveto

Alla vielä yhteenveto:

```java
import java.util.Scanner;

public class Ohjelma {
    public static void main(String[] args) {
        Scanner lukija = new Scanner(System.in);
        String teksti = lukija.nextLine();
        int kokonaisluku = Integer.valueOf(lukija.nextLine());
        double liukuluku = Double.valueOf(lukija.nextLine());
        boolean totuusarvo = Boolean.valueOf(lukija.nextLine());

        // jne
    }
}
```

<programming-exercise name="Muuttujien lukeminen yhdessä"  tmcname='osa01-Osa01_15.MuuttujienLukeminenYhdessa'>

Kirjoita ohjelma, joka kysyy käyttäjältä merkkijonoa, kokonaislukua, liukulukua ja totuusarvoa. Tämän jälkeen ohjelma tulostaa käyttäjän syöttämät arvot.

Alla on annettuna ohjelman esimerkkitulostuksia:

<sample-output>

Syötä merkkijono!
**heippa**
Syötä kokonaisluku!
**11**
Syötä liukuluku!
**4.2**
Syötä totuusarvo!
**true**
Syötit merkkijonon heippa
Syötit kokonaisluvun 11
Syötit liukuluvun 4.2
Syötit totuusarvon true

</sample-output>

<sample-output>

Syötä merkkijono!
**oho!**
Syötä kokonaisluku!
**-4**
Syötä liukuluku!
**3200.1**
Syötä totuusarvo!
**false**
Syötit merkkijonon oho!
Syötit kokonaisluvun -4
Syötit liukuluvun 3200.1
Syötit totuusarvon false

</sample-output>

</programming-exercise>
