

Helsingin Yliopiston opiskelijaruokaloissa eli Unicafeissa opiskelijat maksavat lounaansa käyttäen maksukorttia. Lopullinen Maksukortti tulee näyttämään luokkakaaviona seuraavalta:

<img src="../img/diagrams/luokkakaavio-teht-maksukortti.png" alt="[Maksukortti|-saldo:double|+Maksukortti(double);+syoEdullisesti():void;+syoMaukkaasti():void;+lataaRahaa(double):void;+toString():String]">

Tässä tehtäväsäsarjassa tehdään luokka `Maksukortti`, jonka tarkoituksena on jäljitellä Unicafeissa tapahtuvaa maksutoimintaa.


<h2>Luokan runko</h2>

Projektiin tulee kuulumaan kaksi kooditiedostoa:

Tehtäväpohjan mukana tulee kooditiedosto `Paaohjelma` jonka sisällä on `main`-metodi.

Lisää projektiin uusi luokka nimeltä `Maksukortti`. Uuden luokan saa lisättyä seuraavasti: Ruudun vasemmalla reunalla on projektilistaus. Paina projektin nimen kohdalla hiiren oikeaa nappia. Valitse avautuvasta valikosta *New* ja *Java Class*. Anna luokan nimeksi (Class Name) `Maksukortti`.

Tee ensin `Maksukortti`-olion konstruktori, jolle annetaan kortin alkusaldo ja joka tallentaa sen olion sisäiseen muuttujaan. Tee sitten `toString`-metodi, joka palauttaa kortin saldon muodossa "Kortilla on rahaa X euroa".

Seuraavassa on luokan `Maksukortti` runko:

```java
public class Maksukortti {
    private double saldo;

    public Maksukortti(double alkusaldo) {
        // kirjoita koodia tähän
    }

    public String toString() {
        // kirjoita koodia tähän
    }
}
```

Seuraava pääohjelma testaa luokkaa:

```java
public class Paaohjelma {
    public static void main(String[] args) {
        Maksukortti kortti = new Maksukortti(50);
        System.out.println(kortti);
    }
}
```

Ohjelman tulisi tuottaa seuraava tulostus:

<sample-output>

Kortilla on rahaa 50.0 euroa

</sample-output>


<h2>Kortilla maksaminen</h2>


Täydennä `Maksukortti`-luokkaa seuraavilla metodeilla:

```java
public void syoEdullisesti() {
    // kirjoita koodia tähän
}

public void syoMaukkaasti() {
    // kirjoita koodia tähän
}
```

Metodin `syoEdullisesti` tulisi vähentää kortin saldoa 2.60 eurolla ja metodin `syoMaukkaasti` tulisi vähentää kortin saldoa 4.60 eurolla.

Seuraava pääohjelma testaa luokkaa:

```java
public class Paaohjelma {
    public static void main(String[] args) {
        Maksukortti kortti = new Maksukortti(50);
        System.out.println(kortti);

        kortti.syoEdullisesti();
        System.out.println(kortti);

        kortti.syoMaukkaasti();
        kortti.syoEdullisesti();
        System.out.println(kortti);
    }
}
```

Ohjelman tulisi tuottaa kutakuinkin seuraava tulostus:

<sample-output>

Kortilla on rahaa 50.0 euroa
Kortilla on rahaa 47.4 euroa
Kortilla on rahaa 40.199999999999996 euroa

</sample-output>


<h2>Ei-negatiivinen saldo</h2>


Mitä tapahtuu, jos kortilta loppuu raha kesken? Ei ole järkevää, että saldo muuttuu negatiiviseksi. Muuta metodeita `syoEdullisesti` ja `syoMaukkaasti` niin, että ne eivät vähennä saldoa, jos saldo menisi negatiiviseksi.

Seuraava pääohjelma testaa luokkaa:

```java
public class Paaohjelma {
    public static void main(String[] args) {
        Maksukortti kortti = new Maksukortti(5);
        System.out.println(kortti);

        kortti.syoMaukkaasti();
        System.out.println(kortti);

        kortti.syoMaukkaasti();
        System.out.println(kortti);
    }
}
```

Ohjelman tulisi tuottaa seuraava tulostus:

<sample-output>

Kortilla on rahaa 5.0 euroa
Kortilla on rahaa 0.40000000000000036
Kortilla on rahaa 0.40000000000000036

</sample-output>

Yllä toinen metodin `syoMaukkaasti` kutsu ei vaikuttanut saldoon, koska saldo olisi mennyt negatiiviseksi.


<h2>Kortin lataaminen</h2>


Lisää `Maksukortti`-luokkaan seuraava metodi:

```java
public void lataaRahaa(double rahamaara) {
    // kirjoita koodia tähän
}
```

Metodin tarkoituksena on kasvattaa kortin saldoa parametrina annetulla rahamäärällä. Kuitenkin kortin saldo saa olla korkeintaan 150 euroa, joten jos ladattava rahamäärä ylittäisi sen, saldoksi tulisi tulla silti tasan 150 euroa.

Seuraava pääohjelma testaa luokkaa:

```java
public class Paaohjelma {
    public static void main(String[] args) {
        Maksukortti kortti = new Maksukortti(10);
        System.out.println(kortti);

        kortti.lataaRahaa(15);
        System.out.println(kortti);

        kortti.lataaRahaa(10);
        System.out.println(kortti);

        kortti.lataaRahaa(200);
        System.out.println(kortti);
    }
}
```

Ohjelman tulisi tuottaa seuraava tulostus:

<sample-output>

Kortilla on rahaa 10.0 euroa
Kortilla on rahaa 25.0 euroa
Kortilla on rahaa 35.0 euroa
Kortilla on rahaa 150.0 euroa

</sample-output>


<h2>Kortin lataus negatiivisella arvolla</h2>

Muuta metodia `lataaRahaa` vielä siten, että jos yritetään ladata negatiivinen rahamäärä, ei kortilla oleva arvo muutu.

Seuraava pääohjelma testaa luokkaa:

```java
public class Paaohjelma {
    public static void main(String[] args) {
        Maksukortti kortti = new Maksukortti(10);
        System.out.println("Pekka: " + kortti);
        kortti.lataaRahaa(-15);
        System.out.println("Pekka: " + kortti);
    }
}
```

Ohjelman tulisi tuottaa seuraava tulostus:

<sample-output>

Pekka: Kortilla on rahaa 10.0 euroa
Pekka: Kortilla on rahaa 10.0 euroa

</sample-output>


<h2>Monta korttia</h2>


Tee luokan `Paaohjelma` `main`-metodiin koodi, joka sisältää seuraavan tapahtumasarjan:

- Luo Pekan kortti. Kortin alkusaldo on 20 euroa
- Luo Matin kortti. Kortin alkusaldo on 30 euroa
- Pekka syö maukkaasti
- Matti syö edullisesti
- Korttien arvot tulostetaan (molemmat omalle rivilleen, rivin alkuun kortin omistajan nimi)
- Pekka lataa rahaa 20 euroa
- Matti syö maukkaasti
- Korttien arvot tulostetaan (molemmat omalle rivilleen, rivin alkuun kortin omistajan nimi)
- Pekka syö edullisesti
- Pekka syö edullisesti
- Matti lataa rahaa 50 euroa
- Korttien arvot tulostetaan (molemmat omalle rivilleen, rivin alkuun kortin omistajan nimi)


Pääohjelman runko on seuraava:

```java
public class Main {
    public static void main(String[] args) {
        Maksukortti pekanKortti = new Maksukortti(20);
        Maksukortti matinKortti = new Maksukortti(30);

        // kirjoita koodia tähän
    }
}
```

Ohjelman tulisi tuottaa seuraava tulostus:

<sample-output>

Pekka: Kortilla on rahaa 15.4 euroa
Matti: Kortilla on rahaa 27.4 euroa
Pekka: Kortilla on rahaa 35.4 euroa
Matti: Kortilla on rahaa 22.799999999999997 euroa
Pekka: Kortilla on rahaa 30.199999999999996 euroa
Matti: Kortilla on rahaa 72.8 euroa

</sample-output>

