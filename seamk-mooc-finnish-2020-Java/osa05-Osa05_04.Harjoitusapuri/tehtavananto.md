

[Karvosen kaavan](https://fi.wikipedia.org/wiki/Karvosen_kaava) avulla voidaan laskea tavoitesyke fyysistä harjoittelua varten. Tavoitesykkeen laskeminen perustuu kaavaan `(maksimisyke - leposyke) * (tavoitesykeprosentti) + leposyke`, missä tavoitesyke annetaan prosenttina maksimisykkeestä.


Esimerkiksi, jos henkilön maksimisyke on `200`, leposyke `50`, ja tavoitesyke `75%` maksimisykkeestä, on tavoiteltava sydämen syke noin `((200-50) * (0.75) + 50)` eli `162.5` lyöntiä minuutissa.


Luo luokka `Harjoitusapuri`, jolle annetaan konstruktorin parametrina ikä ja leposyke. Harjoitusapurin tulee tarjota metodi tavoitesyke, jolle annetaan parametrina prosentuaalista maksimisykkeen osuutta kuvaava double-tyyppinen luku. Osuus annetaan lukuna nollan ja yhden välillä. Luokalla tulee olla:


- Konstruktori `public Harjoitusapuri(int ika, int leposyke)`
- Metodi `public double tavoitesyke(double prosenttiaMaksimista)`, joka laskee ja palauttaa tavoiteltavan sykkeen.


Käytä maksimisykkeen laskemiseen kaavaa `206.3 - (0.711 * ikä)`.


Käyttöesimerkki:


```java
Harjoitusapuri apuri = new Harjoitusapuri(30, 60);

double prosenttiosuus = 0.5;

while (prosenttiosuus < 1.0) {
    double tavoite = apuri.tavoitesyke(prosenttiosuus);
    System.out.println("Tavoite " + (prosenttiosuus * 100) + "% maksimista: " + tavoite);
    prosenttiosuus = prosenttiosuus + 0.1;
}
```

<sample-output>

Tavoite 50.0% maksimista: 122.48500000000001
Tavoite 60.0% maksimista: 134.98200000000003
Tavoite 70.0% maksimista: 147.479
Tavoite 80.0% maksimista: 159.976
Tavoite 89.99999999999999% maksimista: 172.473
Tavoite 99.99999999999999% maksimista: 184.97000000000003

</sample-output>

