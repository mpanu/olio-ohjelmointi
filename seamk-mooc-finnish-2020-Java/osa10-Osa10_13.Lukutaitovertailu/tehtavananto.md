

Käytetään tässä tehtävässä UNESCOn avointa dataa lukutaidosta. Data sisältää tilastot eri maiden arvioiduista tai raportoiduista lukutaidoista viimeisen kahden vuoden ajalta. Tehtäväpohjassa mukana oleva tiedosto `lukutaito.csv` sisältää arviot sekä yli 15-vuotiaiden naisten että yli 15-vuotiaiden miesten lukutaidosta. Tiedoston lukutaito.csv yksittäisen rivin muoto on seuraava: teema, ikäryhmä, sukupuoli, maa, vuosi, lukutaitoprosentti. Alla on esimerkkinä tiedoston viisi ensimmäistä riviä.


<pre>
Adult literacy rate, population 15+ years, female (%),United Republic of Tanzania,2015,76.08978
Adult literacy rate, population 15+ years, female (%),Zimbabwe,2015,85.28513
Adult literacy rate, population 15+ years, male (%),Honduras,2014,87.39595
Adult literacy rate, population 15+ years, male (%),Honduras,2015,88.32135
Adult literacy rate, population 15+ years, male (%),Angola,2014,82.15105
</pre>


Kirjoita ohjelma, joka lukee tiedoston `lukutaito.csv` ja tulostaa tiedoston sisällön pienimmästä lukutaidosta suurimpaan. Tulostus tulee muotoilla seuraavan esimerkin näyttämään muotoon. Esimerkki näyttää tulostuksen ensimmäiset 5 odotettua riviä.


<sample-output>

Niger (2015), female, 11.01572
Mali (2015), female, 22.19578
Guinea (2015), female, 22.87104
Afghanistan (2015), female, 23.87385
Central African Republic (2015), female, 24.35549

</sample-output>

Tehtävä on kahden pisteen arvoinen.

Vinkki! Merkkijonon saa pilkottua taulukoksi pilkun kohdalta seuraavalla tavalla.


```java
String mjono = "Adult literacy rate, population 15+ years, female (%),Zimbabwe,2015,85.28513";
String[] palat = mjono.split(",");
// nyt palat[0] sisältää "Adult literacy rate"
// palat[1] sisältää " population 15+ years"
// jne.

// saat välilyönnit pois alusta ja lopusta trim-metodilla:
palat[1] = palat[1].trim();
```

