

Tässä tehtävässä teemme eliöita ja eliöistä koostuvia laumoja jotka liikkuvat ympäriinsä. Eliöiden sijaintien ilmoittamiseen käytetään *kaksiulotteista koordinaatistoa*. Jokaiseen sijaintiin liittyy kaksi lukua, `x`- ja `y`-koordinaatti. Koordinaatti `x` kertoo, kuinka pitkällä "nollapisteestä" mitattuna sijainti on vaakasuunnassa, ja koordinaatti `y` vastaavasti kuinka pitkällä sijainti on pystysuunnassa. Jos koordinaatiston käsite ei ole tuttu, voit lukea siitä lisää esimerkiksi <a href="http://fi.wikipedia.org/wiki/Koordinaatisto">wikipediasta</a>.

<br/>

Tehtävän mukana tulee rajapinta `Siirrettava`, joka kuvaa asiaa jota voidaan siirtää paikasta toiseen. Rajapinta sisältää metodin `void siirra(int dx, int dy)`. Parametri `dx` kertoo, paljonko asia siirtyy x-akselilla ja `dy` y-akselilla.


Tehtävässä toteutat luokat `Elio` ja `Lauma`, jotka molemmat ovat siirrettäviä.


<h2>Elio-luokan toteuttaminen</h2>


Luo luokka `Elio`, joka toteuttaa rajapinnan `Siirrettava`. Eliön tulee tietää oma sijaintinsa (x, y -koordinaatteina). Luokan `Elio` APIn tulee olla seuraava:

- **public Elio(int x, int y)**<br/>Luokan konstruktori, joka saa olion aloitussijainnin x- ja y-koordinaatit parametrina
- **public String toString()**<br/> Luo ja palauttaa oliosta merkkijonoesityksen. Eliön merkkijonoesityksen tulee olla seuraavanlainen `"x: 3; y: 6"`. Huomaa että koordinaatit on erotettu puolipisteellä (`;`)
- **public void siirra(int dx, int dy)**<br/> Siirtää oliota parametrina saatujen arvojen verran. Muuttuja `dx` sisältää muutoksen koordinaattiin `x`, muuttuja `dy` sisältää muutoksen koordinaattiin `y`. Esimerkiksi jos muuttujan `dx` arvo on 5, tulee oliomuuttujan `x` arvoa kasvattaa viidellä

Kokeile luokan `Elio` toimintaa seuraavalla esimerkkikoodilla.

```java
Elio elio = new Elio(20, 30);
System.out.println(elio);
elio.siirra(-10, 5);
System.out.println(elio);
elio.siirra(50, 20);
System.out.println(elio);
```

<sample-output>

x: 20; y: 30
x: 10; y: 35
x: 60; y: 55

</sample-output>


<h2>Lauman toteutus</h2>

Luo luokka `Lauma`, joka toteuttaa rajapinnan `Siirrettava`. Lauma koostuu useasta `Siirrettava`-rajapinnan toteutavasta oliosta, jotka tulee tallettaa esimerkiksi listarakenteeseen.

Luokalla `Lauma` tulee olla seuraavanlainen API.

- **public String toString()**<br/> Palauttaa merkkijonoesityksen lauman jäsenten sijainnista rivin vaihdolla erotettuna.
- **public void lisaaLaumaan(Siirrettava siirrettava)**<br/> Lisää laumaan uuden `Siirrettava`-rajapinnan toteuttavan olion
- **public void siirra(int dx, int dy)**<br/> Siirtää laumaa parametrina saatujen arvojen verran. Huomaa että tässä sinun tulee siirtää jokaista lauman jäsentä.

Kokeile ohjelmasi toimintaa alla olevalla esimerkkikoodilla.

```java
Lauma lauma = new Lauma();
lauma.lisaaLaumaan(new Elio(73, 56));
lauma.lisaaLaumaan(new Elio(57, 66));
lauma.lisaaLaumaan(new Elio(46, 52));
lauma.lisaaLaumaan(new Elio(19, 107));
System.out.println(lauma);
```

<sample-output>

x: 73; y: 56
x: 57; y: 66
x: 46; y: 52
x: 19; y: 107

</sample-output>


