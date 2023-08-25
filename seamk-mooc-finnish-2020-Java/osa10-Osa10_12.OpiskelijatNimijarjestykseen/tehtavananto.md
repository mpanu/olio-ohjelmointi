

Saat valmiin luokan Opiskelija. Opiskelijalla on nimi. Toteuta Opiskelija-luokassa `Comparable`-rajapinta siten, että `compareTo`-metodi lajittelee opiskelijat nimen mukaan aakkosjärjestykseen.

**Vinkki:** Opiskelijan nimi on String, ja String-luokka on itsessään `Comparable`. Voit hyödyntää String-luokan `compareTo`-metodia Opiskelija-luokan metodia toteuttaessasi. `String.compareTo` kohtelee kirjaimia eriarvoisesti kirjainkoon mukaan, ja tätä varten String-luokalla on myös metodi `compareToIgnoreCase` joka nimensä mukaisesti jättää kirjainkoon huomioimatta. Voit käyttää opiskelijoiden järjestämiseen kumpaa näistä haluat.

