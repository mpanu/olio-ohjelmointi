

Luo lyhenteiden ylläpitoon käytettävä luokka `Lyhenteet`. Luokalla tulee olla parametriton konstruktori, ja sen tulee tarjota seuraavat metodit:

- `public void lisaaLyhenne(String lyhenne, String selite)` lisää lyhenteen sekä siihen liittyvän selitteen.
- `public boolean onkoLyhennetta(String lyhenne)` tarkastaa onko lyhennettä lisätty; palauttaa `true` mikäli kyllä, `false` mikäli ei.
- `public String haeLyhenne(String lyhenne)` hakee lyhenteeseen liittyvän selitteen; palauttaa `null` mikäli lyhennettä ei ole lisätty.

Käyttöesimerkki:

```java
Lyhenteet lyhenteet = new Lyhenteet();
lyhenteet.lisaaLyhenne("esim.", "esimerkiksi");
lyhenteet.lisaaLyhenne("jne.", "ja niin edelleen");
lyhenteet.lisaaLyhenne("yms.", "ynnä muuta sellaista");

String teksti = "esim. jne. yms. lol.";

for (String osa: teksti.split(" ")) {
    if(lyhenteet.onkoLyhennetta(osa)) {
        osa = lyhenteet.haeLyhenne(osa);
    }

    System.out.print(osa);
    System.out.print(" ");
}

System.out.println();
```

<sample-output>

esimerkiksi ja niin edelleen ynnä muuta sellaista lol.

</sample-output>

