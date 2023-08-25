

Tehtäväpohjassa on valmiina luokka `Viesti`, jonka avulla voidaan luoda viestejä kuvaavia olioita. Jokaisella viestillä on lähettäjä ja sisältö.

Toteuta luokka `Viestipalvelu`. Luokalla tulee olla parametriton konstruktori ja sen tulee sisältää lista `Viesti`-olioita. Lisää luokalle tämän jälkeen seuraavat kaksi metodia:

- `public void lisaa(Viesti viesti)` - lisää viestipalveluun parametrina annetun viestin mikäli viestin sisällön pituus on korkeintaan 280 merkkiä.

- `public ArrayList<Viesti> getViestit()` - palauttaa viestipaveluun lisätyt viestit.

Vinkki! Saat merkkijonon pituuden merkkijonoon liittyvällä `length()`-metodilla.

