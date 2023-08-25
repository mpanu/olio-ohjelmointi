

<h2>Rekisterinumeron equals ja hashCode</h2>

Eurooppalaiset rekisteritunnukset koostuvat kahdesta osasta: yksi tai kaksikirjaimisesta maatunnuksesta ja maakohtaisesti määrittyvästä rekisterinumerosta, joka taas koostuu numeroista ja merkeistä. Rekisterinumeroita esitetään seuraavanlaisen luokan avulla:

```java
public class Rekisterinumero {
    // tässä määre final tarkoittaa sitä, että arvoa ei voi muuttaa asetuksen jälkeen
    private final String rekNro;
    private final String maa;

    public Rekisterinumero(String maa, String rekNro) {
       this.rekNro = rekNro;
       this.maa = maa;
    }

    public String toString(){
        return maa+ " "+rekNro;
    }
}
```

Rekisterinumeroja halutaan tallettaa esim. ArrayList:eille ja käyttää HashMap:in avaimina, eli kuten yllä mainittu, tulee niille toteuttaa metodit `equals` ja `hashCode`, muuten ne eivät toimi halutulla tavalla. Toteuta luokalle rekisterinumero metodit `equals` ja `hashCode`.

Esimerkkiohjelma:

```java
public static void main(String[] args) {
    Rekisterinumero rek1 = new Rekisterinumero("FI", "ABC-123");
    Rekisterinumero rek2 = new Rekisterinumero("FI", "UXE-465");
    Rekisterinumero rek3 = new Rekisterinumero("D", "B WQ-431");

    ArrayList<Rekisterinumero> suomalaiset = new ArrayList<>();
    suomalaiset.add(rek1);
    suomalaiset.add(rek2);

    Rekisterinumero uusi = new Rekisterinumero("FI", "ABC-123");
    if (!suomalaiset.contains(uusi)) {
        suomalaiset.add(uusi);
    }
    System.out.println("suomalaiset: " + suomalaiset);
    // jos equals-metodia ei ole ylikirjoitettu, menee sama rekisterinumero toistamiseen listalle

    HashMap<Rekisterinumero, String> omistajat = new HashMap<>();
    omistajat.put(rek1, "Arto");
    omistajat.put(rek3, "Jürgen");

    System.out.println("omistajat:");
    System.out.println(omistajat.get(new Rekisterinumero("FI", "ABC-123")));
    System.out.println(omistajat.get(new Rekisterinumero("D", "B WQ-431")));
    // jos hashCode ei ole ylikirjoitettu, eivät omistajat löydy
}
```

Toteuta metodit equals ja hashCode. Kun metodit equals ja hashCode on toteutettu oikein, ylläolevan esimerkin tulostus on seuraavanlainen.


<sample-output>

suomalaiset: [FI ABC-123, FI UXE-465]
omistajat:
Arto
Jürgen

</sample-output>


<h2>Omistaja rekisterinumeron perusteella</h2>

Toteuta luokka `Ajoneuvorekisteri` jolla on seuraavat metodit:

- `public boolean lisaa(Rekisterinumero rekkari, String omistaja)` lisää parametrina olevaa rekisterinumeroa vastaavalle autolle parametrina olevan omistajan. Metodi palauttaa true jos omistajaa ei ollut ennestään; jos rekisterinumeroa vastaavalla autolla taas oli jo omistaja, metodi palauttaa false ja ei tee mitään

- `public String hae(Rekisterinumero rekkari)` palauttaa parametrina olevaa rekisterinumeroa vastaavan auton omistajan. Jos auto ei ole rekisterissä, palautetaan `null`

- `public boolean poista(Rekisterinumero rekkari)` poistaa parametrina olevaa rekisterinumeroa vastaavat tiedot, metodi palauttaa true jos tiedot poistetiin, ja false jos parametria vastaavia tietoja ei ollut rekisterissä


**Huom:** Ajoneuvorekisterin täytyy tallettaa omistajatiedot `HashMap<Rekisterinumero, String> omistajat` -tyyppiseen oliomuuttujaan!

<h2>Ajoneuvorekisteri laajenee</h2>

Lisää Ajoneuvorekisteriin vielä seuraavat metodit:

- `public void tulostaRekisterinumerot()` tulostaa rekisterissä olevat rekisterinumerot.

- `public void tulostaOmistajat()` tulostaa rekisterissä olevien autojen omistajat. Kukin nimi tulee tulostaa vain kertaalleen vaikka omistajalla olisikin useampi auto.

Vinkki! Voit luoda metodiin `tulostaOmistajat` listan, jota käytät jo tulostettujen omistajien muistamiseen. Mikäli omistaja ei ole listalla, hänet voi tulostaa ja lisätä listalle-- mikäli omistajaa taas on listalla, häntä ei tule tulostaa.


