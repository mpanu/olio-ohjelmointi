

Tehtäväpohjassa tulee sovellus, johon on lisätty riippuvuus H2-nimiseen tietokantaan. Sovelluksessa on seuraavat neljä luokkaa:

- `Todo`: tehtävää tehtävää kuvaava luokka. Jokaisella tehtävällä on numeerinen tunnus (id), nimi, kuvaus sekä tieto siitä onko tehtävä tehty.

- `TodoDao`: tehtävien tietokantaan tallentamiseen käytettävä luokka, sana "dao" on lyhenne sanasta "data access object". Luokka tarjoaa metodit tehtävien listaamiseen, lisäämiseen, tehdyksi asettamiseen sekä poistamiseen. Tehdyksi asettaminen ja poistaminen tapahtuu numeerisen tunnuksen perusteella. Luokan konstruktori saa parametrinaan käytettävän tietokannan osoitteen.

- `Kayttoliittyma`: tehtävien tietokantaan tallentamiseen käytettävä luokka. Luokka tarjoaa metodit tehtävien listaamiseen, lisäämiseen, tehdyksi asettamiseen sekä poistamiseen. Tehdyksi asettaminen ja poistaminen tapahtuu numeerisen tunnuksen perusteella. Luokan konstruktori saa parametrina käytettävän tietokannan osoitteen.

- `Ohjelma`: sovelluksen käynnistämiseen tarkoitettu luokka.


Tässä tehtävässä tarkoituksenasi on muokata käyttöliittymää siten, että sovelluksen käyttäjällä on mahdollisuus tehtävien lisäämiseen, listaamiseen, tehdyksi asettamiseen sekä poistamiseen. Älä muokkaa luokkia `Todo`, `TodoDao` tai `Ohjelma`.

Odotettu sovelluksen toiminta on seuraava:


```

Syötä komento:
1) listaa
2) lisää
3) aseta tehdyksi
4) poista
x) lopeta
> 1
Listataan tietokannan tiedot

Syötä komento:
1) listaa
2) lisää
3) aseta tehdyksi
4) poista
x) lopeta
> 2
Lisätään tehtävää
Syötä nimi
koodaa
Syötä kuvaus
koodaa paljon

Syötä komento:
1) listaa
2) lisää
3) aseta tehdyksi
4) poista
x) lopeta
> 2
Lisätään tehtävää
Syötä nimi
tee ruokaa
Syötä kuvaus
riisipuuroa

Syötä komento:
1) listaa
2) lisää
3) aseta tehdyksi
4) poista
x) lopeta
> 1
Listataan tietokannan tiedot
Todo{id=1, nimi=koodaa, kuvaus=koodaa paljon, valmis=false}
Todo{id=2, nimi=tee ruokaa, kuvaus=riisipuuroa, valmis=false}

Syötä komento:
1) listaa
2) lisää
3) aseta tehdyksi
4) poista
x) lopeta
> 3

Mikä asetetaan tehdyksi (syötä id)?
2

Syötä komento:
1) listaa
2) lisää
3) aseta tehdyksi
4) poista
x) lopeta
> 1
Listataan tietokannan tiedot
Todo{id=1, nimi=koodaa, kuvaus=koodaa paljon, valmis=false}
Todo{id=2, nimi=tee ruokaa, kuvaus=riisipuuroa, valmis=true}

Syötä komento:
1) listaa
2) lisää
3) aseta tehdyksi
4) poista
x) lopeta
> 4

Mikä poistetaan (syötä id)?
2

Syötä komento:
1) listaa
2) lisää
3) aseta tehdyksi
4) poista
x) lopeta
> 1
Listataan tietokannan tiedot
Todo{id=1, nimi=koodaa, kuvaus=koodaa paljon, valmis=false}

Syötä komento:
1) listaa
2) lisää
3) aseta tehdyksi
4) poista
x) lopeta
> 3

Mikä asetetaan tehdyksi (syötä id)?
1

Syötä komento:
1) listaa
2) lisää
3) aseta tehdyksi
4) poista
x) lopeta
> 1
Listataan tietokannan tiedot
Todo{id=1, nimi=koodaa, kuvaus=koodaa paljon, valmis=true}

Syötä komento:
1) listaa
2) lisää
3) aseta tehdyksi
4) poista
x) lopeta
> x
Kiitos!

```

Tehtävässä toteuttamasi tekstikäyttöliittymä ei oikeastaan poikkea millään tavalla aiemmin toteuttamistamme tekstikäyttöliittymistä. Toisin kuin ennen, nyt tieto vain tallennetaan tietokantaan: *tallennetut tiedot ovat sovelluksen käytössä myös seuraavan käynnistyksen yhteydessä.*

