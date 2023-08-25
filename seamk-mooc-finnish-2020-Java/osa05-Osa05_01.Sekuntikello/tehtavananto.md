


Tehtäväpohjassa tulee edellä kuvattu luokka `Viisari`. Toteuta materiaalin `Kello`-luokkaa mukaillen luokka `Sekuntikello`.


Sekuntikellossa on kaksi viisaria. Yksi sadasosasekunneille ja yksi sekunneille. Sekuntikellon edetessä sadasosasekuntien määrä kasvaa yhdellä. Kun sadasosasekunteja vastaava viisari saavuttaa arvon sata, viisarin arvo nollaantuu ja sekuntien määrä kasvaa yhdellä. Vastaavasti, kun sekunteja vastaava viisari saavuttaa arvon kuusikymmentä, viisarin arvo nollaantuu.


- `public Sekuntikello()` luo uuden sekuntikellon.
- `public String toString()` palauttaa sekuntikellon merkkijonoesityksen. Merkkijonoesityksen tulee olla muotoa "sekunnit:sadasosasekunnit", missä sekä sekunnit että sadasosasekunnit esitetään kahdella numerolla. Esimerkiksi merkkijono "19:83" kuvastaisi aikaa 19 sekuntia, 83 sadasosasekuntia.
- `public void etene()` siirtää kelloa yhden sadasosasekunnin eteenpäin.


Kun olet saanut tehtävän tehtyä, palauta se palvelimelle.


Voit halutessasi kokeilla kellon toimintaa pääohjelmassa. Alla olevalla esimerkkikoodilla saat aikaan ohjelman, missä kello tulostetaan ja kello etenee kerran sadasosasekunnissa.


```java
Sekuntikello sekuntikello = new Sekuntikello();

while (true) {
    System.out.println(sekuntikello);
    sekuntikello.etene();

    try {
        Thread.sleep(10);
    } catch (Exception e) {

    }
}
```

Huom! Yllä kuvatun ohjelman suoritus ei lopu itsestään ikinä. Saat sammutettua ohjelman tulostusikkunan vasemmassa laidassa olevaa punaista neliötä painamalla.


