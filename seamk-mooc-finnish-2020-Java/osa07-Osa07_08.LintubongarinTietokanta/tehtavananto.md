

**Tehtävä vastaa kolmea yksiosaista tehtävää.**

Tässä tehtävässä suunnittelet ja toteutat tietokannan lintubongareille. Tietokanta sisältää lintuja, joista jokaisella on nimi (merkkijono) ja latinankielinen nimi (merkkijono). Tämän lisäksi tietokanta laskee kunkin linnun havaintokertoja.

Ohjelmasi täytyy toteuttaa seuraavat komennot:

- `Lisaa` - lisää linnun (**huom:** komennon nimessä ei ä-kirjainta!)

- `Havainto` - lisää havainnon

- `Tilasto` - tulostaa kaikki linnut

- `Nayta` - tulostaa yhden linnun (**huom:** komennon nimessä ei ä-kirjainta!)

- `Lopeta` - lopettaa ohjelman

Lisäksi virheelliset syötteet pitää käsitellä. (Ks. `Simo` alla). Tässä vielä esimerkki ohjelman toiminnasta:

<sample-output>

? **Lisaa**
Nimi: **Korppi**
Latinankielinen nimi: **Corvus Corvus**
? **Lisaa**
Nimi: **Haukka**
Latinankielinen nimi: **Dorkus Dorkus**
? **Havainto**
Mikä havaittu? **Haukka**
? **Havainto**
Mikä havaittu? **Simo**
Ei ole lintu!
? **Havainto**
Mikä havaittu? **Haukka**
? **Tilasto**
Haukka (Dorkus Dorkus): 2 havaintoa
Korppi (Corvus Corvus): 0 havaintoa
? **Nayta**
Mikä? **Haukka**
Haukka (Dorkus Dorkus): 2 havaintoa
? **Lopeta**

</sample-output>

**Huom!** Ohjelmasi rakenne on täysin vapaa. Testaamme vain että `Paaohjelma` luokan `main`-metodi toimii kuten tässä on kuvailtu. Hyödyt tehtävässä todennäköisesti ongelma-aluetta sopivasti kuvaavista luokista.

