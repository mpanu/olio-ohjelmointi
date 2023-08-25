

**Huom!** Esimerkkitulosteet saattavat rivittyä väärin kapeilla ruuduilla. Mikäli käytät selainikkunan koosta vain rajattua osaa, tai käytössäsi on muuten kapea ruutu, kokeile venyttää ruutua leveyssuunnassa ja tarkasta muuttuuko tekstin rivitys. Tehtävässä oletetaan "leveällä ruudulla" havaittava rivitys.

Lisäksi jos sinulla tulee ongelmia tässä tehtävässä 'ä'-kirjaimen kanssa, kokeile palauttaa tehtävä suoraan palvelimelle painamalla nuolta ylöspäin Netbeanssissa.

Kirjoita ohjelma, joka kysyy käyttäjältä hahmon nimeä sekä hahmon ammattia. Tämän jälkeen ohjelma tulostaa pienen tarinan.

Ohjelman tulostuksen tulee olla kuten esimerkissä -- huomaa, että nimi ja ammatti muuttuu syötteen perusteella.

<sample-output>

Kerron kohta tarinan, mutta tarvitsen siihen hieman tietoja.
Minkä niminen tarinassa esiintyvä hahmo on?
**Nauriskala**
Mikä hahmon ammatti on?
**kalastaja**
Tässä tarina:
Olipa kerran Nauriskala, joka oli ammatiltaan kalastaja.
Matkatessaan töihin, Nauriskala mietti arkeaan.
Ehkäpä Nauriskala ei olekaan koko elämäänsä kalastaja.

</sample-output>

Tehtäväpohjan mukana tulee runko, joka sisältää Scanner-apuvälineen luomisen.

```java
import java.util.Scanner;

public class Tarina {

    public static void main(String[] args) {
        Scanner lukija = new Scanner(System.in);

        // toteuta ohjelma tänne
    }
}
```

Alla vielä toinen esimerkki.

<sample-output>

Kerron kohta tarinan, mutta tarvitsen siihen hieman tietoja.
Minkä niminen tarinassa esiintyvä hahmo on?
**Ada**
Mikä hahmon ammatti on?
**matemaatikko**
Tässä tarina:
Olipa kerran Ada, joka oli ammatiltaan matemaatikko.
Matkatessaan töihin, Ada mietti arkeaan.
Ehkäpä Ada ei olekaan koko elämäänsä matemaatikko.

</sample-output>

