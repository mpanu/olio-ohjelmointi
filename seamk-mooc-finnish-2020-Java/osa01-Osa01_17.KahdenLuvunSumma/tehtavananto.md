

Kirjoita ohjelma, joka kysyy käyttäjältä kahta lukua. Tämän jälkeen ohjelma tulostaa käyttäjän syöttämien lukujen summan.

Kun kysyt useampaa lukua, tee kullekin luvulle oma muuttuja:

```java
Scanner lukija = new Scanner(System.in);

System.out.println("Syötä ensimmäinen luku!");
int eka = Integer.valueOf(lukija.nextLine());
System.out.println("Syötä toinen luku!");
int toka = Integer.valueOf(lukija.nextLine());

// tee jotain luvuilla
```

Alla on annettuna ohjelman toivottuja esimerkkitulostuksia:

<sample-output>

Syötä ensimmäinen luku!
**8**
Syötä toinen luku!
**3**
Lukujen summa on 11

</sample-output>

<sample-output>

Syötä ensimmäinen luku!
**3**
Syötä toinen luku!
**-1**
Lukujen summa on 2

</sample-output>

