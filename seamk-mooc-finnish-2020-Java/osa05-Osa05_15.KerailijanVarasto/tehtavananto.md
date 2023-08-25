

Tässä tehtävässä toteutat ohjelman, jota käytetään keräilijän varaston käsittelyyn. Varastoon voi lisätä esineitä. Kun esineiden lisääminen lopetetaan, varastossa olevat esineet tulostetaan.

<h2>Esineiden lisääminen ja listaaminen</h2>

Ohjelman tulee lukea käyttäjältä esineitä. Kun kaikki käyttäjän esineet on luettu, ohjelma tulostaa esineiden tiedot.

Kustakin esineestä tulee lukea tunnus ja nimi. Mikäli syötetty tunnus tai nimi on tyhjä, ohjelma lopettaa syötteen pyytämisen ja tulostaa esineiden tiedot.

Esimerkkitulostus:

<sample-output>

Syötä esineen tunnus, tyhjä lopettaa.
**B07H8ND8HH**
Syötä esineen nimi, tyhjä lopettaa.
**He-Man hahmo**
Syötä esineen tunnus, tyhjä lopettaa.
**B07H8ND8HH**
Syötä esineen nimi, tyhjä lopettaa.
**He-Man**
Syötä esineen tunnus, tyhjä lopettaa.
**B07NQFMZYG**
Syötä esineen nimi, tyhjä lopettaa.
**He-Man hahmo**
Syötä esineen tunnus, tyhjä lopettaa.
**B07NQFMZYG**
Syötä esineen nimi, tyhjä lopettaa.
**He-Man hahmo**
Syötä esineen tunnus, tyhjä lopettaa.

==Esineet==
B07H8ND8HH: He-Man hahmo
B07H8ND8HH: He-Man
B07NQFMZYG: He-Man hahmo
B07NQFMZYG: He-Man hahmo

</sample-output>

Esineiden tulostusmuodon tulee olla `tunnus: nimi`.

Huom! Älä käytä kaksoispistettä ohjelman muussa tulostuksessa.


<h2>Kukin esine tulostetaan vain kerran</h2>

Muokkaa ohjelmaa siten, että esineiden syöttämisen jälkeen kukin esine tulostetaan korkeintaan kerran. Kaksi esinettä tulee käsittää samoina mikäli niiden tunnukset ovat samat (nimet voivat vaihdella esimerkiksi maittain).

Mikäli käyttäjä syöttää saman esineen useaan otteeseen, tulostuksessa käytetään ensimmäisenä syötettyä esinettä.

<sample-output>

Syötä esineen tunnus, tyhjä lopettaa.
**B07H8ND8HH**
Syötä esineen nimi, tyhjä lopettaa.
**He-Man hahmo**
Syötä esineen tunnus, tyhjä lopettaa.
**B07H8ND8HH**
Syötä esineen nimi, tyhjä lopettaa.
**He-Man**
Syötä esineen tunnus, tyhjä lopettaa.
**B07NQFMZYG**
Syötä esineen nimi, tyhjä lopettaa.
**He-Man hahmo**
Syötä esineen tunnus, tyhjä lopettaa.
**B07NQFMZYG**
Syötä esineen nimi, tyhjä lopettaa.
**He-Man hahmo**
Syötä esineen tunnus, tyhjä lopettaa.

==Esineet==
B07H8ND8HH: He-Man hahmo
B07NQFMZYG: He-Man hahmo

</sample-output>


Vinkki! Tämä kannattaa toteuttaa siten, että kukin esine lisätään listalle korkeintaan kerran -- vertaile esineiden samuutta niiden tunnuksien perusteella.

