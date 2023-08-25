

Tehtäväpohjan mukana tulee luokka `Paivays`, joka määrittelee päivästä, kuukaudesta ja vuodesta koostuvan olion. Tässä tehtävässä täydennät Paivays-luokkaa siten, että sen equals-metodi osaa kertoa ovatko päivämäärät täsmälleen samat.

Lisää `Paivays`-luokkaan metodi `public boolean equals(Object object)`, joka kertoo onko metodille parametrina annetun olion päiväys sama kuin käytetyn olion päiväys.

Metodin tulee toimia seuraavasti:

```java
Paivays p = new Paivays(1, 2, 2000);
System.out.println(p.equals("heh"));
System.out.println(p.equals(new Paivays(5, 2, 2012)));
System.out.println(p.equals(new Paivays(1, 2, 2000)));
```

<sample-output>

false
false
true

</sample-output>

