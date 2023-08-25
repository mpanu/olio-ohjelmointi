

Tehtävänäsi on toteuttaa luokka `UseanKaannoksenSanakirja`, johon voidaan lisätä yksi tai useampi käännös jokaiselle sanalle. Luokan tulee toteuttaa seuraavat metodit:

- `public void lisaa(String sana, String kaannos)` lisää käännöksen sanalle säilyttäen vanhat käännökset

- `public ArrayList<String> kaanna(String sana)` palauttaa listan, joka sisältää sanojen käännökset. Jos sanalle ei ole yhtäkään käännöstä, metodin tulee palauttaa tyhjä lista.

- `public void poista(String sana)` poistaa sanan ja sen kaikki käännökset sanakirjasta.


Käännökset kannattanee lisätä `HashMap<String, ArrayList<String>>`-tyyppiseen oliomuuttujaan.

Esimerkki:

```java
UseanKaannoksenSanakirja sanakirja = new UseanKaannoksenSanakirja();
sanakirja.lisaa("kuusi", "six");
sanakirja.lisaa("kuusi", "spruce");

sanakirja.lisaa("pii", "silicon");
sanakirja.lisaa("pii", "pi");

System.out.println(sanakirja.kaanna("kuusi"));
sanakirja.poista("pii");
System.out.println(sanakirja.kaanna("pii"));
```

<sample-output>

[six, spruce]
[]

</sample-output>

