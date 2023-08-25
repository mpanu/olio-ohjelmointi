

Tehtäväpohjassa on valmiiksi annettuna luokka `Sanakirja`, joka tarjoaa toiminnallisuuden sanojen ja niiden käännösten tallentamiseen. Vaikka luokan sisäisessä totetuksessa on asioita, joita kurssilla ei ole käsitelty, on sen käyttö suoraviivaista:

```java
Sanakirja kirja = new Sanakirja();
kirja.lisaa("yksi", "one");
kirja.lisaa("kaksi", "two");

System.out.println(kirja.kaanna("yksi"));
System.out.println(kirja.kaanna("kaksi"));
System.out.println(kirja.kaanna("kolme"));
```

<sample-output>

one
two
null

</sample-output>

Tässä tehtävässä toteutat luokkaa `Sanakirja` hyödyntävän tekstikäyttöliittymän.


<h2>Tekstikäyttöliittymän käynnistys ja lopetus</h2>

Toteuta luokka `Tekstikayttoliittyma`, joka saa konstruktorin parametrina `Scanner`-olion sekä `Sanakirja`-olion. Lisää tämän jälkeen luokalle metodi `public void kaynnista()`. Metodin tulee toimia seuraavalla tavalla:

1. Metodi kysyy käyttäjältä komentoa.
2. Mikäli komento on `lopeta`, tekstikäyttöliittymä tulostaa merkkijonon "Hei hei!" ja metodin `kaynnista` suoritus päättyy.
3. Muulloin, tekstikäyttöliittymä tulostaa viestin "Tuntematon komento", jonka jälkeen metodi jatkaa kysymällä käyttäjältä komentoa eli kohdasta 1.


```java
Scanner lukija = new Scanner(System.in);
Sanakirja kirja = new Sanakirja();

Tekstikayttoliittyma kayttoliittyma = new Tekstikayttoliittyma(lukija, kirja);
kayttoliittyma.kaynnista();
```

<sample-output>

Komento: **jotain**
Tuntematon komento
Komento: **lisaa**
Tuntematon komento
Komento: **lopeta**
Hei hei!

</sample-output>


<h2>Käännösten lisääminen</h2>

Muokkaa metodia `public void kaynnista()` siten, että se toimii seuraavalla tavalla:

1. Metodi kysyy käyttäjältä komentoa.
2. Mikäli komento on `lopeta`, tekstikäyttöliittymä tulostaa merkkijonon "Hei hei!" ja metodin `kaynnista` suoritus päättyy.
3. Mikäli komento on `lisaa`, tekstikäyttöliittymä kysyy käyttäjältä sanaa ja käännöstä, kumpaakin omalla rivillään. Tämän jälkeen sanat lisätään sanakirjaan ja metodi jatkaa kysymällä käyttäjältä komentoa eli kohdasta 1.
4. Muulloin, tekstikäyttöliittymä tulostaa viestin "Tuntematon komento", jonka jälkeen metodi jatkaa kysymällä käyttäjältä komentoa eli kohdasta 1.


<sample-output>

Komento: **jotain**
Tuntematon komento
Komento: **lisaa**
Sana: **hauki**
Käännös: **pike**
Komento: **muuta**
Tuntematon komento
Komento: **lopeta**
Hei hei!

</sample-output>

Yllä kuvatussa esimerkissä sanakirja-olioon lisätään sana "hauki" sekä sen käännös "pike". Sanakirjaa voisi tällöin käyttöliittymästä poistumisen jälkeen käyttää seuraavasti:

```java
Scanner lukija = new Scanner(System.in);
Sanakirja kirja = new Sanakirja();

Tekstikayttoliittyma kayttoliittyma = new Tekstikayttoliittyma(lukija, kirja);
kayttoliittyma.kaynnista();
System.out.println(kirja.kaanna("hauki")); // tulostaa merkkijonon "pike"
```


<h2>Sanan kääntäminen</h2>


Muokkaa metodia `public void kaynnista()` siten, että se toimii seuraavalla tavalla:

1. Metodi kysyy käyttäjältä komentoa.
2. Mikäli komento on `lopeta`, tekstikäyttöliittymä tulostaa merkkijonon "Hei hei!" ja metodin `kaynnista` suoritus päättyy.
3. Mikäli komento on `lisaa`, tekstikäyttöliittymä kysyy käyttäjältä sanaa ja käännöstä, kumpaakin omalla rivillään. Tämän jälkeen sanat lisätään sanakirjaan ja metodi jatkaa kysymällä käyttäjältä komentoa eli kohdasta 1.
4. Mikäli komento on `hae`, tekstikäyttöliittymä kysyy käyttäjältä käännettävää sanaa. Tämän jälkeen tekstikäyttöliittymä tulostaa sanan käännöksen ja metodi jatkaa kysymällä käyttäjältä komentoa eli kohdasta 1.
5. Muulloin, tekstikäyttöliittymä tulostaa viestin "Tuntematon komento", jonka jälkeen metodi jatkaa kysymällä käyttäjältä komentoa eli kohdasta 1.


<sample-output>

Komento: **jotain**
Tuntematon komento
Komento: **lisaa**
Sana: **hauki**
Käännös: **pike**
Komento: **muuta**
Tuntematon komento
Komento: **hae**
Haettava: **hauki**
Käännös: pike
Komento: **hae**
Haettava: **nauris**
Käännös: null
Komento: **lopeta**
Hei hei!

</sample-output>


<h2>Käännöksen siistiminen</h2>

Muokkaa tekstikäyttöliittymän hakutoiminnallisuutta siten, että mikäli sanaa ei löydy (eli sanakirja palauttaa `null`-viitteen), tekstikäyttöliittymä tulostaa viestin "Sanaa (haettava) ei löydy".

<sample-output>

Komento: **jotain**
Tuntematon komento
Komento: **lisaa**
Sana: **hauki**
Käännös: **pike**
Komento: **muuta**
Tuntematon komento
Komento: **hae**
Haettava: **hauki**
Käännös: pike
Komento: **hae**
Haettava: **nauris**
Sanaa nauris ei löydy
Komento: **lopeta**
Hei hei!

</sample-output>


