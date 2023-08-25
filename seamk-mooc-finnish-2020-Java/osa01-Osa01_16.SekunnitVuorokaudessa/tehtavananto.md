

Toteuta tehtäväpohjaan ohjelma, joka kysyy käyttäjältä vuorokausien lukumäärää. Tämän jälkeen ohjelma tulostaa sekuntien määrän annetuissa vuorokausissa.

Opimme aiemmin, että luvun lukeminen onnistuu seuraavasti:

```java
Scanner lukija = new Scanner(System.in);

System.out.println("Kirjoita luku ");
int luku = Integer.valueOf(lukija.nextLine());
System.out.println("Kirjoitit " + luku);
```

Esimerkkitulostuksia:

<sample-output>

Kuinka monen vuorokauden sekunnit tulostetaan?
**1**
86400

</sample-output>

<sample-output>

Kuinka monen vuorokauden sekunnit tulostetaan?
**3**
259200

</sample-output>

<sample-output>

Kuinka monen vuorokauden sekunnit tulostetaan?
**7**
604800

</sample-output>

