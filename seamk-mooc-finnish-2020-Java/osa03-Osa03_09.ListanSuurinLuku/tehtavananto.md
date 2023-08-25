

Ohjelmaan on toteutettu valmiina pohja, joka lukee käyttäjältä lukuja listalle. Syötteiden lukeminen päätetään kun käyttäjä syöttää luvun -1.

Lisää ohjelmaan toiminnallisuus, joka lukujen lukemisen jälkeen etsii listalta listan suurimman luvun ja tulostaa sen arvon. Ohjelman pitäisi toimia seuraavasti.

<sample-output>

**72**
**2**
**8**
**93**
**11**
**-1**

Listan suurin luku: 93

</sample-output>

Ota mallia allaolevasta pienintä lukua etsivästä lähdekoodista.

```java
// oletetaan, että käytössämme on lista, jossa on kokonaislukuja

int pienin = lista.get(0);

for(int i = 0; i < lista.size(); i++) {
    int luku = lista.get(i);
    if (pienin > luku) {
        pienin = luku;
    }
}

System.out.println("Listan pienin luku: " + pienin);
```

