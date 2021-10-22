---
layout: info
title:  "Aiheita"
nav-title: "Aiheita"
categories: jekyll update
tag: info
permalink: /fi/aiheet/
---

Aiheen voi keksiä itse, tai voit valita alla olevasta listasta itsellesi mielenkiintoisen aiheen. Listalla olevat aiheet ovat vain ehdotuksia, niitä voi muokata ja kehittää - lopullinen aihe sovitaan yhdessä ohjaajan kanssa.

## Verkot ja polunetsintä

* Aihe sopii lähes millä tahansa ohjelmointikielellä toteutettavaksi, kunhan osaat tuottaa kartan / labyrintin visualisoinnin niin, ettei se vaadi liikaa työtä. Visualisointi on välttämätön, mutta sen tekeminen ei saisi viedä suurta osaa työajasta. Selkeä ASCII-grafiikka riittää. 

1. Miten löydetään tehokkaasti nopein/lyhin reitti labyrintistä ulos. Labyrintteja voi tuottaa itse tai ladata jostain valmiita. [Wikipedia, Maze solving algorithm](https://en.wikipedia.org/wiki/Maze_solving_algorithm) 

2. Miten löydetään tehokkaasti nopein/lyhin reitti verkossa kahden pisteen välillä. Verkon pisteet voivat olla esimerkiksi katuosoitteita, joukkoliikenteen pysäkkejä tai koordinaatteja. Hyvä artikkeli aiheesta: [Reitinhakualgoritmien vertailu](http://theory.stanford.edu/~amitp/GameProgramming/AStarComparison.html)

* Kummassakin tapauksessa vaaditaan vähintään kahden eri reitinhakualgoritmin vertailu, joista ainakin toinen poikkeaa riittävästi esitietoihin kuuluvista Tira-kurssilla opituista. Esim. JPS (Jump Point Search), IDA\* tai fringe search (varsin vaativa) vs Dijkstra. A\* vs Dijkstra ei kelpaa, koska A\* on liian lähellä esitietona olevaa Dijkstran algoritmia. JPS:ää ei voi käyttää verkossa, jossa kaaret voivat kulkea mielivaltaiseen suuntaan. Labyrinteissa tulee käyttää niihin sopivia algoritmeja. Jos aiheena on JPS (kulku 8 suuntaan) vs Dijkstra, voit käyttää valmiita tietorakenteita. Mikäli aihe on IDA\* vs Dijkstra, tulee Dijkstran algoritmin prioriteettijono toteuttaa itse tehokkaasti keolla, mutta IDA\*:n pinona voi käyttää valmista tietorakennetta. Katso [JPS](http://users.cecs.anu.edu.au/~dharabor/data/papers/harabor-grastien-aaai11.pdf), [IDA\*](https://en.wikipedia.org/wiki/Iterative_deepening_A*), [fringe search](https://webdocs.cs.ualberta.ca/~holte/Publications/fringe.pdf).

* Reitinhakualgoritmien vertailussa on syytä heti alkuun toteuttaa löydetyn reitin ja läpikäytyjen solmujen / hyppypisteiden visualisointi. Ilman sitä on vaikea selvittää toimiiko algoritmi oikein. Kartan mukana tulevia etäisyystietoja voi käyttää testeissä, mutta oikea etäisyys ei vielä takaa, että algoritmi toimii niin tehokkaasti kuin sen kuuluu toimia. Visualisointi paitsi auttaa valmiin työn oikeellisuuden toteamisessa, nopeuttaa myös virheiden löytämistä ohjelman laatimisen aikana. 

* Karttoja reitinhakutöihin löytyy esimerkiksi [Moving AI Lab](http://www.movingai.com/benchmarks/):in sivuilta tai maanminttauslaitoksen karttojen [lataus](http://kartat.kapsi.fi/) sivustolta. Huomaa, että Moving AI:n kartoissa ilmoitetut etäisyydet on laskettu niin, että reitti kiertää esteen kulmapikselin, sen sijaan että kulkisi viistosti tavallaan puoliksi estepikselin yli. 

* Myös joukkoliikenteen reitti/aikataulut [https://developers.google.com/transit/gtfs/](https://developers.google.com/transit/gtfs/) tai [https://digitransit.fi/en/developers/](https://digitransit.fi/en/developers/) ja avoin karttadata [https://www.openstreetmap.org](https://www.openstreetmap.org) ovat olleet suosittuja. 

## Tiedon tiivistys

* Tiedosto tulisi saada mahtumaan pienempään tilaan, miten tämä onnistuu? Toivottava lopullinen koko tekstiä pakattaessa on 40-60% alkuperäisestä koosta. Tiedosto pitää myös pystyä palauttamaan alkuperäiseen muotoon. Tekstiä on mielekästä pakata vain häviöttömillä pakkausmenetelmillä, kuvaa ja ääntä voi pakata myös häviöllisillä menetelmillä. Sopiva laajuus on kahden pakkausalgoritmin vertailu, esim. Huffman vs Lempel Ziv. Jotkin pakkausmenetelmät ovat niin vaativia, että yhdenkin toteuttaminen riittää. Voit käyttää kielen valmiita tietorakenteita. Katso [Tiedonpakkaus](https://fi.wikipedia.org/wiki/Tiedonpakkaus)


## Pelit

* Vuoropohjaisia kahden pelaajan pelejä pelataan usein [minimax-algoritmilla](https://en.wikipedia.org/wiki/Minimax), jota on tehostettu [alpha-beta-karsinnalla](https://en.wikipedia.org/wiki/Alpha%E2%80%93beta_pruning). Yleensä ei ole mahdollista tutkia kaikkia siirtovaihtoehtoja siihen asti, että jompi kumpi pelaaja voittaa. Silloin täytyy erilaisia pelitilanteita laittaa arvojärjestykseen myös muilla perusteilla. Tällainen on sopiva laajuus peliprojektille. Kaikkiin alla mainittuihin peleihin ei tämä lähestymistapa kuitenkaan toimi.

* Shakki, go, risti-nolla (laajalla ruudukolla, 5:n rivi) jne. ovat hauskoja ja haastavia pelejä. Niitä olisi kiva pelata tietokonetta vastaan, tehtävänäsi on kehittää valitsemallesi pelille tekoäly. Tekoälyn pitää pystyä pelaamaan ihmistä vastaan, ehkä myös itseään vastaan. Voit käyttää valmista Java-pohjaa, mutta huomaa, että siihen perehtyminen voi vaatia paljon aikaa.

* [xboard](https://www.gnu.org/software/xboard/) ja [lichess](https://lichess.org/blog/WvDNticAAMu_mHKP/welcome-lichess-bots) alustoja hyödyntävä java-projektipohja shakkitekoälylle on tehty ohtu-projektina, ja se löytyy täältä: [https://github.com/TiraLabra/chess](https://github.com/TiraLabra/chess) Jos käytät valmista pohjaa, kerro koodin kommenteissa selvästi mikä on omaa koodiasi, ja mikä on pohjaa. Älä muokkaa pohjaa, vaan kirjoita oma koodisi omaan luokkaansa / metodiinsa.

* Kivi-sakset-paperi on kaikille tuttu peli. Onnistutko toteuttamaan tekoälyn, joka päihittää ohjaajan? Kun tekoälysi on hyvä, voit jatkaa kehitystä ottamalla mukaan vielä kaksi vaihtoehtoa: [Lisko ja Spock](http://www.youtube.com/watch?v=x5Q6-wMx-K8). Yksi tapa oppia toisen pelityyli on käyttää useamman eri asteen Markovin ketjuja: [https://arxiv.org/pdf/2003.06769](https://arxiv.org/pdf/2003.06769). Kannattaa jutella ohjaajan kanssa jos tämä aihe kiinnostaa.
![Lisko Spock](http://upload.wikimedia.org/wikipedia/commons/a/ad/Pierre_ciseaux_feuille_l%C3%A9zard_spock_aligned.svg)

* [15-pelin](http://en.m.wikipedia.org/wiki/15_puzzle) ratkaisija. Kaikille tuttu 15-peli on haastava ratkaistava, jopa 3 x 3 ruudukon pelin ratkaisu vie paljon aikaa pahimmassa tapauksessa heikolla heuristiikalla. IDA* sopii algoritmiksi, heuristiikaksi on useita vaihtoehtoja. Niitä voi vertailla tehokkuustesteissä. 

* [Miinaharava](https://en.wikipedia.org/wiki/Minesweeper_(video_game)) on toinen suosittu pulmapeli. Voit toteuttaa ratkaisijan/auttajan miinaharavaan projektipohjalla joka läytyy täältä: [https://github.com/TiraLabra/minesweeper](https://github.com/TiraLabra/minesweeper) Tämän kurssin kannalta kiinnostavista ratkaisutavoista kerrotaan esim. täällä: [https://dash.harvard.edu/handle/1/14398552](https://dash.harvard.edu/handle/1/14398552)  Jos käytät valmista pohjaa, kerro koodin kommenteissa selvästi mikä on omaa koodiasi, ja mikä on pohjaa. Älä muokkaa pohjaa, vaan kirjoita oma koodisi omaan luokkaansa / metodiinsa.

* [halite](https://halite.io/) tekoäly. Tai muu internetistä löytyvä tekoälyhaaste.

## Koneoppiminen

* Laskennallinen luovuus. Markovin ketjujen avulla voidaan tuottaa esimerkiksi musiikkia tai luonnollisen kielen kaltaisia sanoja tai lauseita. Markovin ketju on prosessi, jossa kukin tila riippuu vain edellisestä tilasta, tai tässä tapauksessa jostain kiinteästä määrästä edellisiä tiloja. Esimerkiksi toisen asteen Markovin ketjun toteuttaminen vaatii kaikkien opetusdatassa esiintyvien kolmikoiden tallettamista. Kokeile generointia alkaen 1. asteesta, ja vertaa tuloksia eri asteilla. Seuraava kirjain, sana tai sävel arvotaan opetusdatasta opittujen todennäköisyyksien mukaan. Toteuta itse trie-tietorakenne sanojen / lauseiden / sävel- / sointusekvenssien tallettamiseen, ja kokeile mitä syntyy Markovin ketjun avulla. Voit käyttää sekä valmiita kirjastoja että ulkoisia ohjelmia opetusdatan esikäsittelyyn, melodian soittamiseen / nuotintamiseen jne. Aiemmissa projekteissa on musiikkidataa syötetty ohjelmalle MIDI-tiedostoina, [Lilypond](http://lilypond.org/)-nuotteina, koskettimilla soittamalla ja muuntamalla nuotteja käsin numeeriseen muotoon. Järkevien tai edes hauskojen lauseiden tuottamiseen tarvitaan minimissään toisen asteen Markovin ketju. Jotta ei päädytä toistamaan opetusdataa sellaisenaan, pitää silloin olla niin paljon opittuja mahdollisia kolmen sanan jonoja, että kahden edellisen perusteella voi kolmannen usein valita useammalla tavalla. Eri sanoja on paljon, joten dataa tarvitaan runsaasti, jotta tähän päästään, jos data on tekstiä. Myös geneettisillä algoritmeilla voi tuottaa taidetta. 

* Eigenface kasvontunnistus. Katso [Eigenface](https://en.wikipedia.org/wiki/Eigenface) Esitiedot: vähintään Lineaarialgebra ja matriisilaskenta 1+2. Perusmenetelmää voidaan laajentaa, jolloin voit käyttää matriisilaskentaan valmiita kirjastoja, sovi tarkemmasta aiheesta ohjaajan kanssa. Kaikille ohjelmointikielille ei valmiita matriisilaskennan välineitä kuitenkaan ole olemassa.


* Käsin kirjoitettujen numeroiden tunnistus. [MNIST](http://yann.lecun.com/exdb/mnist/) on tietokanta, jota käytetään paljon hahmontunnistusmenetelmien testaamiseen. Tällä kurssilla on numeroita luokiteltu esimerkiksi neuroverkoilla. Sovi ohjaajan kanssa mitä valmiita välineitä voit käyttää, jotta työmäärä on kohtuullinen. Hieman neuroverkkoja helpompi ratkaisu on muuntaa MNIST:in harmaasävykuvat mustavalkoisiksi ja käyttää [k:n lähimmän naapurin menetelmää](https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm) pistejoukkojen etäisyysmitoilla. Joidenkin etäisyysmittojen laskukaavoja löytyy täältä: [A Modified Hausdorff Distance for Object Matching](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.1.8155&rank=5&q=hausdorff&osm=&ossid=) Parhaaksi mainitun mitan D22 lisäksi kannattaa kokeilla ainakin mittaa D23 sellaisenaan ja ilman kerrointa 1/N osakaavassa d6. 

## Luolastojen / labyrinttien generointi
* Suosituksi noussut aihe on esimerkiksi rogue-peleissä käytettävien luolien generointi. Tähän on tarjolla valmiita algoritmeja, mutta oma toteutus on myös täysin mahdollinen. Luolaston generointi voi olla joko etukäteen tapahtuva tai dynaamisesti pelin aikana pelaajan liikkumisen mukaan kehittyvä. Algoritmeja on kahdenlaisia. Toiset tuottavat pelkistä käytävistä koostuvia labyrintteja, jotka yleensä täyttävät suorakaiteen muotoisen tilan kokonaan niin, että joka kohtaan on mahdollista päästä lähtöpisteestä. Jotkin algoritmit taas tuottavat huoneita ja niiden välisiä käytäviä. Labyrintteja generoivat algoritmit ovat yleensä aika yksinkertaisia, jolloin sopiva laajuus on kahden tai useamman menetelmän vertailu. Muita luolastoja saatetaan tuottaa monivaiheisen prosessin kautta, jolloin vertailua ei ehkä tarvita. Tällöin esim. yksi algoritmi voi tuottaa huoneita, toinen niiden väliset käytävät ja kolmas halutun kaltaisen ulkoasun. Katso [https://en.wikipedia.org/wiki/Maze_generation_algorithm](https://en.wikipedia.org/wiki/Maze_generation_algorithm)


## Tietorakennevertailut
Tietorakenteita on monenlaisia, mikä olisi paras kuhunkin ongelmaan? Vertaile neljää eri tietorakennetta (esimerkiksi puita tai kekoja), joita ei ole käsitelty Tietorakenteet ja algoritmit -kurssilla. Tutki missä tilanteessa kukin on paras, eli missä tilanteessa käyttäisit kutakin rakennetta. Tämä aihe ei sovellu ohjelmointikieliin, joissa ei ole tehokasta taulukkoa.


## Salaus ja Tietoturva
* Tietoturva on tänä päivänä tärkeämpää kuin koskaan monien toimintojemme siirryttyä verkkoon. Salausta voi tehdä monilla eri tavoin ja moniin käyttötarkoituksiin. Esim. [RSA-salaus](https://fi.wikipedia.org/wiki/RSA) on sopiva aihe. Sellaiset salausmenetelmät eivät vastaa tämän kurssin tavoitteita, jotka perustuvat yksittäisten sanojen tai koko tekstin merkkien paikan vaihtamiseen tai yksittäisten merkkien korvaamiseen aina jollain tietyllä merkillä. Sovi ohjaajan kanssa mitä valmiita välineitä voit käyttää, jotta saavutetaan sopiva laajuus työlle.

* Salauksia voi myös murtaa. Esimerkiksi vaihtosalaukseen perustuvan salakirjoituksen saa murrettua sanaston avulla merkkien frekvenssejä analysoimalla, jos teksti on riittävän pitkä, ja tiedetään mitä kieltä se on. Ratkaisuksi käy peruuttava haku, joka kokeilee korvata salattuja merkkejä siinä järjestyksessä, mitkä frekvenssien perusteella ovat luultavimpia. Sanaston talletukseen sopii trie-tietorakenne.

## Signaalinkäsittely (kuva, ääni)
Toteuta yksi (tai useampi, riippuen vaativuudesta) signaalinkäsittelyalgoritmi ja raportoi tuloksista. Useat signaalinkäsittelyn algoritmit hyödyntävät matriisilaskentaa ja lineaarialgebraa, joten niiden tunteminen on hyödyksi.

### Muuta kivaa
* Rahtifirma NopsaToimitus haluaa optimoida konttikuljetuksissa käytettävän tilan. Suunnittele miten voidaan täyttää yksi tai useampi kontti mahdollisimman tehokkaasti, jos tiedetään pakettien määrä ja koot. Ideaa voi hakea kuutiopalapelin ratkaisijasta.

* Säännöllisten lausekkeiden tulkki tai kääntäjä. Tulkki sovittaa lauseketta merkkijonoon ja kertoo, kuuluuko se lausekkeen määräämään kieleen. Kääntäjä tuottaa DFA:n, jolle merkkijono annetaan, ja saadaan sama tulos kuin edellä. [Säännölliset lausekkeet](https://blog.stevenlevithan.com/archives/10-reasons-to-learn-and-use-regular-expressions) 

* Kirjoitusvirheiden korjaaja. Merkkijonojen etäisyysmittojen avulla voi selvittää mikä oikea sana todennäköisimmin on, kun tiedetään millaisia virheitä ihmiset tyypillisesti tekevät kirjoittaessaan. Yksi tähän soveltuva mitta on [Damerau–Levenshtein -etäisyys.](https://en.wikipedia.org/wiki/Damerau%E2%80%93Levenshtein_distance) Sanaston talletukseen sopii trie-tietorakenne.
