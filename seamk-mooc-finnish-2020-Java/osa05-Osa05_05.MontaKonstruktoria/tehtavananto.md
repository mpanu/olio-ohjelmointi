

Tehtäväpohjassa on luokka `Esine`, joka kuvaa kaupassa olevaa esinettä. Jokaisella esineellä on nimi, sijainti sekä paino.


Lisää luokkaan `Esine` seuraavat kolme konstruktoria:

- `public Esine(String nimi)` luo esineen annetulla nimellä. Esineen sijainniksi tulee "pientavarahylly" ja painoksi 1.

- `public Esine(String nimi, String sijainti)` luo esineen annetulla nimellä ja sijainnilla. Esineen painoksi tulee 1.

- `public Esine(String nimi, int paino)` luo esineen annetulla nimellä ja painolla. Esineen sijainniksi tulee "varasto".


Voit kokeilla ohjelmasi toimintaa seuraavalla koodilla:


```java
Esine mitta = new Esine("Mitta");
Esine laasti = new Esine("Laasti", "remonttitavarat");
Esine rengas = new Esine("Rengas", 5);

System.out.println(mitta);
System.out.println(laasti);
System.out.println(rengas);
```


<sample-output>

Mitta (1 kg) löytyy sijainnista pientavarahylly
Laasti (1 kg) löytyy sijainnista remonttitavarat
Rengas (5 kg) löytyy sijainnista varasto

</sample-output>

