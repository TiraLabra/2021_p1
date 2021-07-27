---
layout: info
title:  "FAQ"
categories: jekyll update
tag: info
permalink: /fi/faq/
---

## Saako testeissä käyttää valmista kirjastoa "X"?

Kyllä.

## Saako käyttöliittymässä käyttää valmista kirjastoa "Y"?

Kyllä.

Kannattaa varmistaa että erottelu käyttöliittymän ja varsinaisen projektin välillä on selkeä ja jättää käyttöliittymä pois testikaattavuudesta.

## Saako tiedostojen lukemiseen / kirjoittamiseen käyttää valmista kirjastoa "Z"?

Kyllä.

Kannattaa "piilottaa" kirjaston käyttö omaan "I/O" luokkaan joka on ainoa jossa on kirjaston "Z" importti.

## Saako javan rajapintoja käyttää?

Kyllä. Tosin monissa tapauksissa tämä ei ole erityisen käytännöllistä.

Esimerkiksi javan `List` sisältää paljon ominaisuuksia, mitä ei itse toteutetulla listalla tarvita. Lisäksi `List` on geneerinen tietorakenne, mikä javassa tarkoittaa että `List` rajapintaan perustuva oma toteutus ei voi ikinä olla yhtä nopea kuin kokonaisluvuille kovakoodattu rakenne. (Ellei kokonaislukujen käsittelyä ole erikseen koodattu toteutukseen.)

## Pitääkö tietorakenteiden olla geneerisiä?

Ei.

## Saako ohjelmointikielen funktionaalisia ominaisuuksia (esim. Javan stream) käyttää?

Ehkä, riippuu kielestä. Näiden käyttäminen tiralabran tyyppisessä projektissa on monesti epäkäytännöllistä näiden rakenteiden hitaudesta johtuen.

Nämä toki ovat sallittuja ainakin testeissä ja käyttöliittymäkoodissa.

## Saako Javan tai muun kielen `String` luokan funktioita / metodeita käyttää?

Saa.


## Saako Javan `Arrays` luokan funktioita / metodeita käyttää?

Lähtökohtaisesti ei.

## Saako käyttää javan `Random` luokkaa?

Saa, ellei satunnaislukujen generoiminen ole osa itse projektia.

## Saako käyttää valmiita matemaattisia funktioita?

Alkeistyyppien matemaattisia funktioita saa käyttää, kokonaiseen tietorakenteeseen kohdistuvia ei.

## Mikä on helpoin aihe jolla kurssista pääsee läpi / saa vitosen?

Tämä on todella henkilökohtaista, eri henkilöille erilaiset projektit ovat erilailla haastavia.

Tyypillisesti reittialgoritmivertailut, pakkausalgoritmit ja luolastogeneraattorit ovat olleet yksinkertaisemmasta päästä.

* Reitinhaku [Movin ai labs](https://movingai.com/benchmarks/grids.html) 2d kartoilla on melko nopea toteuttaa, jos visualisointi on tekstigrafiikkana. Dijkstra vs JPS tai IDA* riittää hyvällä toteutuksella viitoseen. Dijkstra vs A* ei riitä läpäisyyn, koska Dijkstra kuuluu esitietoihin ja A* on lähes sama koodi.
* Huffman pakkauksen toteuttamalla pääsee hyvin läpi. Toteuttamalla sen lisäksi jonkin muun pakkauksen on hyvät saumat vitoseen.
* Luolastojen tai karttojen generointi parilla erilaisella algoritmilla riittää aika helposti läpipääsyn ja on suhteellisen yksinkertaisesti laajennettavissa vitosen arvoiseen suoritukseen.

Kannattaa keskustella ohjaajan kanssa.

## Voiko kieleksi valita C/C++/Rust/Fortran...?

Matalan tason kielissä testaaminen ja testikattavuuden seuraaminen voi olla hankalaa. Ei suositella ellei ole hyvin perehtynyt kyseiseen kieleen ja valmis selvittämään miten kattavuudet saa esim. Codecoviin.

Koodikatselmointien kanssa voi tulla ongelmia. Voit joutua arvioimaan jollain itsellesi tuntemattomalla kielellä kirjoitettua koodia, vastaavasti saamasi palaute voi olla vähemmän hyödyllistä, jos sen laatija ei osaa käyttämääsi kieltä.

Puhu joka tapauksessa ohjaajan kanssa *ennen ekaa palautusta*!

## Voiko kieleksi valita JavasCriptin?

Jäsä tuntuu jostain syystä soveltuvan yllättävän hyvin tiralabrakieleksi. Kuitenkin jäsän kirjoittamisen, testaamisen ja testikattavuuden seuraamisen olisi syytä olla entuudestaan tuttua.

Koodikatselmoinnista voi kielivalinnan takia jäädä pisteitä saamatta.

Puhu joka tapauksessa ohjaajan kanssa *ennen ekaa palautusta*!

## Voiko kieleksi valita Pascal/APL/ADA/Piet/PHP/...?

Ei suositella. Voit kysyä ohjaajalta *ennen ekaa palautusta*!

## Mitä pitää testata?

Yksikkötesteillä tulee testata kaikki paitsi käyttöliittymä, suorituskykytestit ja mahdollisesti tiedostojen luku ja kirjoittaminen riippuen projektista. Mieti mitä oman sovelluksesi toiminnan oikeellisuus tarkoittaa. Reitinhakualgoritmin tulee löytää lyhin reitti, jos se kuuluu algoritmin määritelmään, ja reitin ja sen etsinnän etenemisen pitää olla sen kaltainen kuin on tarkoitus. Labyrintin tai luolaston tulee olla yhtenäinen. Miinaharavabotti ei saa koskaan osua miinaan silloin, kun ruutua pidetään turvallisena. Pakatun tiedoston koon täytyy olla odotusten mukainen, ja sen tulee purkautua alkuperäiseksi. Shakkibotti ei saa tehdä laittomia siirtoja, ja sen on osattava tehdä matti, mikäli mahdollista sillä laskentasyvyydellä, johon päästään. Jos kattava oikeellisuustesti vie liikaa aikaa, kannattaa laittaa yksikkötesteihin vain pari edustavaa testitapausta ja tehdä lisäksi erillinen testipaketti. 

## Mikä kattavuus pitää olla prosentteina että on riittävästi?

Mitään prosenttimääräisiä tavoitteita ei ole asetettu syystä. On hyvin mahdollista tuottaa 100% kattavuus huonosti testatulle koodille, ja vastaavasti voi olla että 50% kattavuus on täysin riittävä. Yleisesti, mitä korkeampi - sitä parempi.

Kannattaa kirjoittaa mahdollisimman pieniä yksikkötestejä mahdollisimman paljon. Ideana olisi että jos koodissa on virhe, tulisi vähintään yhden testin havaita se, ja virheen kohta koodissa tulisi olla mahdollisimman selkeä.

## Mihin suorituskykytestit pitää laittaa?

Suorituskykytestejä ei kannata tehdä yksikkötesteiksi. Jos yksikkötestien suorittamiseen menee useita minuutteja, ei testejä usein jakseta ajaa tarpeeksi usein. Vastaavasti jos suorituskykytestien ajamiseen menee alle minuutti, on aika todennäköistä että testit eivät ole riittäviä.

Kannattaa siis tehdä oma paketti suorituskykytesteille. Ks. esim. [esimerkkiprojekti](https://github.com/TiraLabra/Testing-and-rmq/tree/master/src/main/java/rmq/util).
