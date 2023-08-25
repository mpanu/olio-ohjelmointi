

Tässä tehtävässä toteutetaan ohjelma kurssipistetilastojen tulostamiseen. Ohjelmalle syötetään pisteitä (kokonaislukuja nollasta sataan), ja ohjelma tulostaa niiden perusteella arvosanoihin liittyviä tilastoja. Syötteiden lukeminen lopetetaan kun käyttäjä syöttää luvun -1. Lukuja, jotka eivät ole välillä [0-100] ei tule ottaa huomioon tilastojen laskemisessa.

Muistathan, että käyttäjältä luetun merkkijonon saa muunnettua kokonaisluvuksi `Integer`-luokan metodilla `valueOf`. Tämä toimii seuraavasti:

```java
String lukuMerkkijonona = "3";
int luku = Integer.valueOf(lukuMerkkijonona);

System.out.println(lukuMerkkijonona + 7);
System.out.println(luku + 7);
```

<sample-output>

37
10

</sample-output>


<h2>Pisteiden keskiarvot</h2>


Kirjoita ohjelma, joka lukee käyttäjältä kurssin yhteispisteitä kuvaavia kokonaislukuja. Luvut väliltä [0-100] ovat hyväksyttäviä ja luku -1 lopettaa syötteen. Muut luvut ovat virhesyötteitä, jotka tulee jättää huomiotta. Kun käyttäjä syöttää luvun -1, tulostetaan syötettyjen yhteispisteiden keskiarvo.

<sample-output>

Syötä yhteispisteet, -1 lopettaa:
**-42**
**24**
**42**
**72**
**80**
**52**
**-1**
Pisteiden keskiarvo (kaikki): 54.0

</sample-output>

<sample-output>

Syötä yhteispisteet, -1 lopettaa:
**50**
**51**
**52**
**-1**
Pisteiden keskiarvo (kaikki): 51.0

</sample-output>


<h2>Hyväksyttyyn arvosanaan liittyvien pisteiden keskiarvot</h2>

Täydennä ohjelmaa siten, että se laskee kaikkien pisteiden keskiarvon lisäksi myös hyväksyttyyn arvosanaan liittyvien pisteiden keskiarvot.

Hyväksytyn arvosanan saa vähintään 50 kurssipisteellä. Voit olettaa, että käyttäjä kirjoittaa aina vähintään yhden välillä [0-100] olevan kokonaisluvun. Jos hyväksyttyyn arvosanaan osuvia lukuja ei ole lainkaan, tulostetaan viiva hyväksyttyjen keskiarvon kohdalle "-".

<sample-output>

Syötä yhteispisteet, -1 lopettaa:
**-42**
**24**
**42**
**72**
**80**
**52**
**-1**
Pisteiden keskiarvo (kaikki): 54.0
Pisteiden keskiarvo (hyväksytyt): 68.0

</sample-output>

<sample-output>

Syötä yhteispisteet, -1 lopettaa:
**49**
**48**
**47**
**-1**
Pisteiden keskiarvo (kaikki): 48.0
Pisteiden keskiarvo (hyväksytyt): -

</sample-output>


<h2>Hyväksyttyjen prosenttiosuus</h2>

Täydennä edellisessä osassa toteuttamaasi ohjelmaa siten, että ohjelma tulostaa myös hyväksymisprosentin. Hyväksymisprosentti lasketaan kaavalla <em>100 * hyväksytyt / osallistujat</em>.

<sample-output>

Syötä yhteispisteet, -1 lopettaa:
**49**
**48**
**47**
**-1**
Pisteiden keskiarvo (kaikki): 48.0
Pisteiden keskiarvo (hyväksytyt): -
Hyväksymisprosentti: 0.0

</sample-output>

<sample-output>

Syötä yhteispisteet, -1 lopettaa:
**102**
**-4**
**33**
**77**
**99**
**1**
**-1**
Pisteiden keskiarvo (kaikki): 52.5
Pisteiden keskiarvo (hyväksytyt): 88.0
Hyväksymisprosentti: 50.0

</sample-output>


<h2>Arvosanajakauma</h2>

Täydennä ohjelmaa siten, että ohjelma tulostaa myös arvosanajakauman. Arvosananajakauma muodostetaan seuraavasti.

<table class="table">
  <tr>
    <th>pistemäärä</th>
    <th>arvosana</th>
  </tr>
  <tr>
    <td>< 50</td>
    <td>hylätty eli 0</td>
  </tr>
  <tr>
    <td>< 60</td>
    <td>1</td>
  </tr>
  <tr>
    <td>< 70</td>
    <td>2</td>
  </tr>
  <tr>
    <td>< 80</td>
    <td>3</td>
  </tr>
  <tr>
    <td>< 90</td>
    <td>4</td>
  </tr>
  <tr>
    <td>>= 90</td>
    <td>5</td>
  </tr>
</table>


Jokainen koepistemäärä muutetaan arvosanaksi yllä olevan taulukon perusteella. Jos syötetty pistemäärä ei ole välillä [0-100], jätetään se huomiotta.

Arvosanajakauma tulostetaan tähtinä. Esim jos arvosanaan 5 oikeuttavia koepistemääriä on 1 kappale, tulostuu rivi <em>5: *</em>. Jos johonkin arvosanaan oikeuttavia pistemääriä ei ole, ei yhtään tähteä tulostu, alla olevassa esimerkissä näin on mm. nelosten kohdalla.</em>

<br/>

<sample-output>

Syötä yhteispisteet, -1 lopettaa:
**102**
**-2**
**1**
**33**
**77**
**99**
**-1**
Pisteiden keskiarvo (kaikki): 52.5
Pisteiden keskiarvo (hyväksytyt): 88.0
Hyväksymisprosentti: 50.0
Arvosanajakauma:
5: *
4:
3: *
2:
1:
0: **

</sample-output>

