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

## Saako käyttää valmiita matemaattisia funktioita?

Alkeistyyppien matemaattisia funktioita saa käyttää, kokonaiseen tietorakenteeseen kohdistuvia ei.

## Mitä pitää testata?

Yksikkötesteillä tulee testata kaikki paitsi käyttöliittymä, suorituskykytestit ja mahdollisesti tiedostojen luku ja kirjoittaminen riippuen projektista. Mieti mitä oman sovelluksesi toiminnan oikeellisuus tarkoittaa. Reitinhakualgoritmin tulee löytää lyhin reitti, jos se kuuluu algoritmin määritelmään, ja reitin ja sen etsinnän etenemisen pitää olla sen kaltainen kuin on tarkoitus. Labyrintin tai luolaston tulee olla yhtenäinen. Miinaharavabotti ei saa koskaan osua miinaan silloin, kun ruutua pidetään turvallisena. Pakatun tiedoston koon täytyy olla odotusten mukainen, ja sen tulee purkautua alkuperäiseksi. Shakkibotti ei saa tehdä laittomia siirtoja, ja sen on osattava tehdä matti, mikäli mahdollista sillä laskentasyvyydellä, johon päästään. Jos kattava oikeellisuustesti vie liikaa aikaa, kannattaa laittaa yksikkötesteihin vain pari edustavaa testitapausta ja tehdä lisäksi erillinen testipaketti. 

## Mikä kattavuus pitää olla prosentteina että on riittävästi?

Mitään prosenttimääräisiä tavoitteita ei ole asetettu syystä. On hyvin mahdollista tuottaa 100% kattavuus huonosti testatulle koodille, ja vastaavasti voi olla että 50% kattavuus on täysin riittävä. Yleisesti, mitä korkeampi - sitä parempi.

Kannattaa kirjoittaa mahdollisimman pieniä yksikkötestejä mahdollisimman paljon. Ideana olisi että jos koodissa on virhe, tulisi vähintään yhden testin havaita se, ja virheen kohta koodissa tulisi olla mahdollisimman selkeä.

## Mihin suorituskykytestit pitää laittaa?

Suorituskykytestejä ei kannata tehdä yksikkötesteiksi. Jos yksikkötestien suorittamiseen menee useita minuutteja, ei testejä usein jakseta ajaa tarpeeksi usein. Vastaavasti jos suorituskykytestien ajamiseen menee alle minuutti, on aika todennäköistä että testit eivät ole riittäviä.

Kannattaa siis tehdä oma paketti suorituskykytesteille. Ks. esim. [esimerkkiprojekti](https://github.com/TiraLabra/Testing-and-rmq/tree/master/src/main/java/rmq/util).
