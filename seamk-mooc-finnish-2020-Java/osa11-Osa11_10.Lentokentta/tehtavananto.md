

Tässä tehtävässä toteutat edellä kuvatun sovelluksen. Saat suunnitella rakenteen vapaasti, tai voit noudattaa edellä kuvattua rakennetta. Käyttöliittymän ulkomuoto sekä vaaditut komennot on määritelty ennalta. Tehtävä on kahden yksittäisen tehtäväpisteen arvoinen.

**Huom: jotta testit toimisivat, saat luoda ohjelmassasi vain yhden Scanner-olion käyttäjän syötteen lukemiseen.**

Lentokenttä-tehtävässä toteutetaan lentokentän hallintasovellus. Lentokentän hallintasovelluksessa hallinnoidaan lentokoneita ja lentoja. Lentokoneista tiedetään aina tunnus ja kapasiteetti. Lennoista tiedetään lennon lentokone, lähtöpaikan tunnus (esim. <a href="http://en.wikipedia.org/wiki/Helsinki_Airport" target="_blank" rel="noopener">HEL</a>) ja kohdepaikan tunnus (esim. <a href="http://en.wikipedia.org/wiki/Batman_Airport" target="_blank" rel="noopener">BAL</a>).

<br/>

Sekä lentokoneita että lentoja voi olla useita. Samalla lentokoneella voidaan myös lentää useita eri lentoja.

Sovelluksen tulee toimia kahdessa vaiheessa: ensin syötetään lentokoneiden ja lentojen tietoja hallintakäyttöliittymässä, jonka jälkeen siirrytään lentopalvelun käyttöön. Lentopalvelussa on kolme toimintoa; lentokoneiden tulostaminen, lentojen tulostaminen, ja lentokoneen tietojen tulostaminen. Tämän lisäksi käyttäjä voi poistua ohjelmasta valitsemalla vaihtoehdon `x`. Jos käyttäjä syöttää epäkelvon komennon, kysytään komentoa uudestaan.


**Ohjelman tulee käynnistyä kun pakkauksessa `lentokentta` olevan luokan Main metodi main suoritetaan.**

Ohjelman esimerkkitulostus alla:

<sample-output>

Lentokentän hallinta
--------------------

Valitse toiminto:
[1] Lisää lentokone
[2] Lisää lento
[x] Poistu hallintamoodista
&gt; **1**
Anna lentokoneen tunnus: **HA-LOL**
Anna lentokoneen kapasiteetti: **42**
Valitse toiminto:
[1] Lisää lentokone
[2] Lisää lento
[x] Poistu hallintamoodista
&gt; **1**
Anna lentokoneen tunnus: **G-OWAC**
Anna lentokoneen kapasiteetti: **101**
Valitse toiminto:
[1] Lisää lentokone
[2] Lisää lento
[x] Poistu hallintamoodista
&gt; **2**
Anna lentokoneen tunnus: **HA-LOL**
Anna lähtöpaikan tunnus: **HEL**
Anna kohdepaikan tunnus: **BAL**
Valitse toiminto:
[1] Lisää lentokone
[2] Lisää lento
[x] Poistu hallintamoodista
&gt; **2**
Anna lentokoneen tunnus: **G-OWAC**
Anna lähtöpaikan tunnus: **JFK**
Anna kohdepaikan tunnus: **BAL**
Valitse toiminto:
[1] Lisää lentokone
[2] Lisää lento
[x] Poistu hallintamoodista
&gt; **2**
Anna lentokoneen tunnus: **HA-LOL**
Anna lähtöpaikan tunnus: **BAL**
Anna kohdepaikan tunnus: **HEL**
Valitse toiminto:
[1] Lisää lentokone
[2] Lisää lento
[x] Poistu hallintamoodista
&gt; **x**

Lentopalvelu
------------

Valitse toiminto:
[1] Tulosta lentokoneet
[2] Tulosta lennot
[3] Tulosta lentokoneen tiedot
[x] Lopeta
&gt; **1**
G-OWAC (101 henkilöä)
HA-LOL (42 henkilöä)
Valitse toiminto:
[1] Tulosta lentokoneet
[2] Tulosta lennot
[3] Tulosta lentokoneen tiedot
[x] Lopeta
&gt; **2**
HA-LOL (42 henkilöä) (HEL-BAL)
HA-LOL (42 henkilöä) (BAL-HEL)
G-OWAC (101 henkilöä) (JFK-BAL)

Valitse toiminto:
[1] Tulosta lentokoneet
[2] Tulosta lennot
[3] Tulosta lentokoneen tiedot
[x] Lopeta
&gt; **3**
Mikä kone: **G-OWAC**
G-OWAC (101 henkilöä)

Valitse toiminto:
[1] Tulosta lentokoneet
[2] Tulosta lennot
[3] Tulosta lentokoneen tiedot
[x] Lopeta
&gt; **x**

</sample-output>


**Huom1:** Testien kannalta on oleellista että *käyttöliittymä* toimii **täsmälleen** kuten yllä kuvattu. Ohjelman tulostamat vaihtoehdot kannattanee copypasteta tästä ohjelmakoodiin. Testit eivät oleta, että ohjelmasi on varautunut epäkelpoihin syötteisiin.

**Huom2:** älä käytä luokkien nimissä skandeja, ne saattavat aiheuttaa ongelmia testeihin!



