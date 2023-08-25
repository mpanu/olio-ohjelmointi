

Tehtäväpohjassa on valmiina luokka `Kirja`, joka kuvaa numeerisen tunnuksen `id` ja nimen `nimi` sisältäviä olioita.

Tässä tehtävässä toteutetaan peräkkäishaku- ja binäärihakualgoritmi kirjojen hakemiseen niiden numeerisen tunnuksen perusteella. Tehtäväpohjassa on valmiina toteutettavien metodien nimet -- tällä hetkellä kumpikin metodeista palauttaa arvon `-1` -- sekä pääohjelma, jota voi käyttää metodien testaamiseen.

<h2>Peräkkäishaku</h2>

Peräkkäishakualgoritmi toimii siten, että se tarkastelee kutakin listassa tai taulukossa olevaa arvoa yksi kerrallaan, nollannesta indeksistä lähtien.

Toteuta luokkaan `Paaohjelma` metodi `public static int perakkaishaku(ArrayList<Kirja> kirjat, int haettavaId)`, joka hakee parametrina annetusta listasta kirjaa, jonka `id`-muuttujan arvo on sama kuin metodille parametrina annetun `haettavaId`-muuttujan arvo. Mikäli kirja löytyy, tulee metodin palauttaa kyseisen kirjan indeksi parametrina annetussa listassa. Mikäli kirjaa ei löydy, tulee metodin palauttaa arvo `-1`.


<h2>Binäärihaku</h2>

Toteuta luokkaan `Paaohjelma` metodi `public static int binaarihaku(ArrayList<Kirja> kirjat, int haettavaId)`, joka hakee parametrina annetusta listasta kirjaa, jonka `id`-muuttujan arvo on sama kuin metodille parametrina annetun `haettavaId`-muuttujan arvo. Mikäli kirja löytyy, tulee metodin palauttaa kyseisen kirjan indeksi parametrina annetussa listassa. Mikäli kirjaa ei löydy, tulee metodin palauttaa arvo `-1`.

Metodi tulee toteuttaa binäärihakuna, jolloin alkuoletuksena on se, että lista on järjestyksessä. Oleta lisäksi, että listan alkupäässä olevat `id`t ovat aina pienempiä kuin listan loppupäässä olevat `id`t.

Saat apuusi myös edellisessä esityksessä käytetyn binäärihaun idean sekä *pseudokoodin*, eli ohjelmointikielen kaltaisella kielellä kuvatun ohjelman kuvauksen.

Edellisessä esityksessä binäärihaun idea kuvattiin seuraavasti:

- Tietoa etsitään järjestyksessä olevasta taulukosta tai listasta.
- Hakeminen aloitetaan keskikohdasta.
- Mikäli tarkasteltavan keskikohdan arvo ei ole haettu arvo, rajataan haettavasta alueesta puolet pois ja siirrytään tarkastelemaan jäljelle jäävän alueen keskikohtaa.
- Mikäli tarkasteltavan keskikohdan arvo on haettu arvo, palautetaan tarkasteltavan keskikohdan indeksi.
- Mikäli tarkasteltavaa aluetta ei ole enää jäljellä (koko alue rajattu pois), palautetaan arvo -1, joka kuvaa ettei haettavaa arvoa löydy

Binäärihaun pseudokoodi on seuraavanlainen.

```code
// oletetaan, että käytössä on muuttuja haettava
// oletetaan, että käytössä on muuttuja lista
alku = 0 // listan nollas indeksi
loppu = koko(lista) - 1 // listan viimeinen indeksi

toista kunnes alku on suurempi kuin loppu:
    keski = (loppu + alku) / 2

    jos arvo kohdassa lista[keski] on haettava
        palauta muuttujan keski arvo

    jos arvo kohdassa lista[keski] on pienempi kuin haettava
        alku = keski + 1

    jos arvo kohdassa lista[keski] on suurempi kuin haettava
        loppu = keski - 1

palauta arvo -1
```

Huomaa, että kirjojen tapauksessa tarkastelet kirjojen `id`-muuttujien arvoja. Tämä tarkoittaa sitä, että sen sijaan, että käsittelet vain listan tietyssä indeksissä olevaa arvoa, tulee tehtävässä käsitellä tietyssä indeksissä olevan arvon `id`-muuttujaa.

