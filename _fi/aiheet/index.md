---
layout: info
title:  "Aiheita"
nav-title: "Aiheita"
categories: jekyll update
tag: info
permalink: /fi/aiheet/
---

Aiheen voi keksiä itse, tai valita alla olevasta listasta itselleen mielenkiintoinen aihe. Listalla olevat aiheet ovat vain ehdotuksia, niitä voi muokata ja kehittää - lopullinen aihe sovitaan yhdessä ohjaajan kanssa.

## Verkot ja polunetsintä

* Aihe sopii lähes millä tahansa ohjelmointikielellä toteutettavaksi, kunhan osaat toteuttaa kartan / labyrintin visualisoinnin niin, ettei se vaadi kovin paljon työtä. Visualisointi vaaditaan, mutta se ei ole keskeinen osa tätä projektia. Selkeä ASCII-grafiikka riittää. 

* Miten löydetään tehokkaasti nopein/lyhin reitti labyrintistä ulos. Labyrintti voi olla tehty esimerksi ascii-merkeistä tai piirretty kuva. [Wikipedia, Maze solving algorithm](https://en.wikipedia.org/wiki/Maze_solving_algorithm) 

* Miten löydetään tehokkaasti nopein/lyhin reitti verkossa kahden pisteen välillä. Verkon pisteet voivat olla esimerkiksi katuosoitteita, joukkoliikenteen pysäkkejä tai koordinaatteja. Hyvä artikkeli aiheesta: [Reitinhakualgoritmien vertailu](http://theory.stanford.edu/~amitp/GameProgramming/AStarComparison.html)

* Vähintään kahden eri reitinhakualgoritmin vertailu, joista toinen poikkeaa riittävästi esitietoihin kuuluvista Tira-kurssilla opituista. Esim. JPS, IDA\*, fringe search (varsin vaativa). A* ei kelpaa, ellei projektissa ole muuta algoritmista vaativuutta riittävästi. Labyrinteissa on syytä käyttää niihin tarkoitettuja algoritmeja.

* Reitinhakualgoritmien vertailussa on syytä heti alkuun toteuttaa löydetyn reitin ja läpikäytyjen solmujen / hyppypisteiden visualisointi. Ilman sitä on aika työlästä selvittää toimiiko algoritmi oikein. Vaikka kartan mukana olisi etäisyystietoja, joihin voi verrata lasketun reitin pituutta, ei oikean pituinen reitti takaa, että algoritmi toimii niin kuin sen pitäisi ja niin tehokkaasti kuin sen kuuluu toimia. Visualisointi paitsi auttaa valmiin työn oikeellisuuden toteamisessa, nopeuttaa myös virheiden löytämistä ohjelman laatimisen aikana.

* Karttoja reitinhakutöihin löytyy esimerkiksi [Moving AI Lab](http://www.movingai.com/benchmarks/):in sivuilta tai maanminttauslaitoksen karttojen [lataus](http://kartat.kapsi.fi/) sivustolta.

* Myös joukkoliikenteen reitti/aikataulut [https://developers.google.com/transit/gtfs/](https://developers.google.com/transit/gtfs/) tai [https://digitransit.fi/en/developers/](https://digitransit.fi/en/developers/) ja avoin karttadata [https://www.openstreetmap.org](https://www.openstreetmap.org) ovat olleet suosittuja.

## Tiedon tiivistys

* Tiedosto tulisi saada mahtumaan pienempään tilaan, miten tämä onnistuu? Toivottava lopullinen koko on 40-60% alkuperäisestä koosta. Tiedosto pitää myös pystyä avaamaan alkuperäiseen muotoon myöhemmin. Kuinka hyvin ohjelma suoriutuu suhteessa olemassa oleviin ohjelmiin.
* Sopiva laajuus on kahden pakkausalgoritmin vertailu, esim. Huffman vs Lempel Ziv.


## Pelit

* Aihe sopii lähes millä tahansa ohjelmointikielellä toteutettavaksi.

* Vuoropohjaisia kahden pelaajan pelejä pelataan usein [minimax-algoritmilla](https://en.wikipedia.org/wiki/Minimax), jota on tehostettu [alpha-beta-karsinnalla](https://en.wikipedia.org/wiki/Alpha%E2%80%93beta_pruning). Yleensä ei ole mahdollista tutkia kaikkia siirtovaihtoehtoja siihen asti, että jompi kumpi voittaa. Silloin täytyy erilaisia pelitilanteita laittaa arvojärjestykseen myös muilla perusteilla. Tällainen on sopiva laajuus peliprojektille. Kaikkiin alla mainittuihin peleihin ei tämä lähestymistapa kuitenkaan toimi.

* Shakki, go, risti-nolla (laajalla ruudukolla, 5:n rivi) jne. ovat hauskoja ja haastavia pelejä. Niitä olisi kiva pelata tietokonetta vastaan, tehtävänäsi on kehittää valitsemallesi pelille tekoäly. Tekoälyn pitää pystyä pelaamaan ihmistä vastaan, ehkä myös itseään vastaan. 

* [xboard](https://www.gnu.org/software/xboard/) ja [lichess](https://lichess.org/blog/WvDNticAAMu_mHKP/welcome-lichess-bots) alustoja hyödyntävä java-projektipohja shakkitekoälylle on tehty ohtu-projektina, ja se löytyy täältä: [https://github.com/TiraLabra/chess](https://github.com/TiraLabra/chess) Jos käytät valmista pohjaa, kerro koodin kommenteissa selvästi mikä on omaa koodiasi, ja mikä on pohjaa. Älä muokkaa pohjaa, vaan kirjoita oma koodisi omaan luokkaansa / metodiinsa.

* Kivi-sakset-paperi on kaikille tuttu peli. Onnistutko toteuttamaan tekoälyn, joka päihittää ohjaajan? Kun tekoälysi on hyvä voit jatkaa kehitystä ottamalla mukaan vielä kaksi vaihtoehtoa: [Lisko ja Spock](http://www.youtube.com/watch?v=x5Q6-wMx-K8). Huomaa että tämä aihe on tämä kurssin esitiedoilla aika hankala. Kannattaa ehdottomasti jutella ohjaajan kanssa jos tämä aihe kiinnostaa. ![Lisko Spock](http://upload.wikimedia.org/wikipedia/commons/a/ad/Pierre_ciseaux_feuille_l%C3%A9zard_spock_aligned.svg)

* [15-pelin](http://en.m.wikipedia.org/wiki/15_puzzle) ratkaisija. Kaikille tuttu 15-peli voi olla haastava ratkaistava. Saatko kehitettyä ohjelman joka ratkaisee pelin kuin pelin? 

* [Miinaharava](https://en.wikipedia.org/wiki/Minesweeper_(video_game)) on toinen suosittu pulmapeli. Voit toteuttaa ratkaisijan/auttajan miinaharavaan projektipohjalla joka läytyy täältä: [https://github.com/TiraLabra/minesweeper](https://github.com/TiraLabra/minesweeper) Tämän kurssin kannalta kiinnostavista ratkaisutavoista kerrotaan esim. täällä: https://dash.harvard.edu/handle/1/14398552  Jos käytät valmista pohjaa, kerro koodin kommenteissa selvästi mikä on omaa koodiasi, ja mikä on pohjaa. Älä muokkaa pohjaa, vaan kirjoita oma koodisi omaan luokkaansa / metodiinsa.

* [halite](https://halite.io/) tekoäly. Tai muu internetistä löytyvä tekoälyhaaste.

## Koneoppiminen

* Aihe sopii lähes millä tahansa ohjelmointikielellä toteutettavaksi. Esim. matriisilaskentaan ei kaikille ohjelmointikielille kuitenkaan löydy valmiita kirjastoja.

* Laskennallinen luovuus. Luovuutta voi toteuttaa esimerkiksi geneettisten algoritmien tai Markovin ketjujen avulla. Markovin ketju on prosessi, jossa kukin tila riippuu vain edellisestä tilasta, tai tässä tapauksessa yleensä jostain kiinteästä määrästä edellisiä tiloja. Näin voidaan tuottaa vaikka luonnollisen kaltaisia sanoja tai lauseita. Näin tuotettuja sanoja voi hyödyntää myös salasanan murtajassa valmiin sanaston lisäksi. Tällä kurssilla on tehty myös sävellyksiä käyttäen Markovin ketjuja. Toteuta itse Trie-tietorakenne sanojen / lauseiden / sävelkulkujen / sointusekvenssien tallettamiseen.

* Eigenface kasvontunnistus. Katso [Eigenface](https://en.wikipedia.org/wiki/Eigenface) Esitiedot: vähintään Lineaarialgebra ja matriisilaskenta 1+2. Perusmenetelmää voidaan laajentaa, jolloin voit käyttää matriisilaskentaan valmiita kirjastoja, sovi tarkemmasta aiheesta ohjaajan kanssa.

## Luolastogeneraattori
* Suosituksi noussut aihe on esimerkiksi rogue-peleissä käytettävien luolien generointi. Tähän on tarjolla valmiita algoritmejä joita voi toteuttaa, mutta oma toteutus on myös täysin mahdollinen. Luolaston generointi voi joko olla etukäteen tapahtuva tai dynaamisesti pelin aikana kehittyvä pelaajan liikkumisen mukaan.


## Tietorakennevertailut
Tietorakenteita on monenlaisia, mikä olisi paras kuhunkin ongelmaan? Vertaile neljää eri tietorakennetta (esimerkiksi puita tai kekoja), joita ei ole käsitelty Tietorakenteet ja algoritmit -kurssilla. Tutki missä tilanteessa kukin on paras, eli missä tilanteessa käyttäisit kutakin rakennetta. Tämä aihe ei sovellu ohjelmointikieliin, joissa ei ole tehokasta taulukkoa.


## Salaus ja Tietoturva
* Tietoturva on tänä päivänä tärkeämpää kuin koskaan monien toimintojemme siirryttyä verkkoon. Salausta voi tehdä monilla eri tavoin ja moniin käyttötarkoituksiin, oheinen sivusta tarjoaa paljon kokeiltavaa aiheesta: http://rumkin.com/tools/cipher/index.php

* Salauksia ja tiivistyksiä voi myös purkaa. Ylläolevan linkin kautta löydät paljon ideoita - voit myös ryhtyä tutkimaan esimerkiksi merkkien frekvenssejä ja analysoida sitä kautta salattua tiedostoa. Vaihtosalaukseen perustuvan salakirjoituksen saa murrettua sanaston avulla, jos teksti on riittävän pitkä, ja tiedetään mitä kieltä se on. Tämä liittyy läheisesti myös Huffmann-tiivistettyyn dataan: (http://rumkin.com/tools/cipher/frequency.php)


## Signaalinkäsittely (kuva, ääni)
Toteuta yksi (tai useampi, riippuen vaativuudesta) signaalinkäsittelyalgoritmi ja raportoi tuloksista. Useat signaalinkäsittelyn algoritmit hyödyntävät matriisilaskentaa ja lineaarialgebraa, joten niiden tunteminen on hyödyksi.

### Muuta kivaa
* Rahtifirma NopsaToimitus haluaa optimoida konttikuljetuksissa käytettävän tilan. Suunnittele miten voidaan täyttää yksi tai useampi kontti mahdollisimman tehokkaasti, jos tiedetään pakettien määrä ja koot. Ideaa voi hakea kuutiopalapelin ratkaisijasta.

* Suunnittele säännöllisten lauseiden tulkki. Miksi? Loistava vastaus: (https://web.archive.org/web/20181227172507/https://blog.stevenlevithan.com/archives/10-reasons-to-learn-and-use-regular-expressions)

* Kirjoitusvirheiden korjaaja. Merkkijonojen etäisyysmittojen avulla voi selvittää mikä oikea sana todennäköisimmin on, kun tiedetään millaisia virheitä ihmiset tyypillisesti tekevät kirjoittaessaan. Tällä pääsee alkuun: (https://en.wikipedia.org/wiki/Damerau%E2%80%93Levenshtein_distance)
