---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home
title: Tiralabra
---

<script src="assets/fuu.js"></script>

## Link to English materials

[Link to English materials](en/)

<noscript><h2 style="color:red;font-weight:bold;">Sivuston sisältö ei näy oikein ilman javascript tukea</h2>
Salli scriptit ainakin lähteestä <code>tiralabra.github.io</code>.
</noscript>

## Ohjaaja

<ul>
<script>
var script = document.scripts[document.scripts.length - 1];
tas.forEach(ta => {
  var elem = document.createElement("li");
  s = ta.name;
  if (ta.fiEmail) {
    s = s + ", " + ta.fiEmail;
  } else if (ta.email) {
    s = s + ", " + ta.email;
  } else {
    s = s + ", (etunumi.sukunimi@helsinki.fi)"
  }
  if (ta.fiSocial) {
    s = s + ", " + ta.fiSocial;
  } else if (ta.social) {
    s = s + ", " + ta.social;
  }
  elem.innerHTML = s;
  script.parentElement.insertBefore(elem, script);
});
</script>
</ul>

## 📅 Aikataulu

Tarkempi aikataulu [täällä](fi/aikataulu/).

<script>
    script = document.scripts[document.scripts.length - 1];
    script.parentElement.insertBefore(makeCalendarFi(), script);
</script>

## 📣 Ajankohtaista

* Kurssin ohjeistusta on muutettu siksi, että yhä useampi suorittaa projektin jollain muulla kielellä kuin Javalla, joka on vielä keväällä 2021 ollut useimpien käyttämä ohjelmointikieli. Ohjeisiin voi tulla pieniä tarkennuksia kurssin alkamiseen asti. 

* <script>
   if (doodleSent) {
    if (timing["demo"]) {
      document.write("Demotilaisuuden ajankohdat on lyöty lukkoon. Ottakaa yhteyttä jos ette pääse paikalle.")
    } else {
      document.write("Doodle linkki demotilaisuuden aikatauluttamiseksi on lähetetty kurssille ilmoittautuneille opiskelijoille. Sähköposti on lähtenyt siihen osoitteseen mikä on labtooliin rekisteröity.")
    }
   } else {
    document.write("Kysely demotilaisuuden aikatauluttamiseksi lähetetään pari viikkoa ennen kurssin päättymistä.")
   }
  </script>
* Lopullinen palautus <script>document.write(fiString(timing["end"].date));</script>.
* Jos löydät kurssisivuilta jotain parannettavaa. Voit seurata [täältä](fi/bug_bounty) löytyviä ohjeita virheen korjaamisesksi. Hyvistä korjauksista on mahdollista saada yhden kurssipisteen "bug bounty" (max 1 per oppilas)

## Linkkejä materiaaliin

* [Aloitusluennon kalvot](kalvot/aloitusluento.pdf)

* [Tarkka aikataulu](fi/aikataulu)

* [Usein kysytyt kysymykset](fi/faq)

* [Aiheideoita](fi/aiheet)

* [Tietoja dokumentaatiosta](fi/dokumentaatio)

* [Ohjeita gitin käyttöön](fi/git-ohje)

* [Ohjeita ja esimerkkejä testauksen tekemiseen Javalla](https://github.com/TiraLabra/Testing-and-rmq)

* [Yksinkertaiset ohjeet Maven- tai Gradle-projektin luontiin](fi/maven-gradle)

* [Ohjeet palautuksien ja viikkoraportin tekemiseen](fi/palautukset)

* [Ohjeet vertaisarviointiin](fi/vertaisarvioinnit)

## 🗒️ Labtool

* [https://study.cs.helsinki.fi/labtool/](https://study.cs.helsinki.fi/labtool/)
* Kirjaudu Yliopiston tunnuksilla.

## Kurssiin [telegram-kanava](https://t.me/tkttiralabra)

## Ohjaus

<ul>
<script>
var script = document.scripts[document.scripts.length - 1];
if (timing["paja1"]) {
  var elem = document.createElement("li");
  elem.innerHTML = "Pajaohjausta järjestetään kalenterissa näkyviin aikoihin.";
  script.parentElement.insertBefore(elem, script);
  elem = document.createElement("li");
  elem.innerHTML = "Pajasta voi myös muihin aikoihin pyytää apua aloritmeihin liittyen.";
  script.parentElement.insertBefore(elem, script);
} else {
  var elem = document.createElement("li");
  elem.innerHTML = "Intensiivikursseilla ei järjestetä viikottaista pajaa. Jos haluat henkilökohtaista ohjausta kumpulassa niin ota yhteyttä ohjaajaan";
  script.parentElement.insertBefore(elem, script);
}
</script>
<li>Voit myös ottaa yhteyttä <a href="https://t.me/tkttiralabra">Telegramissa</a>.</li>
<li>Tai tarvittaessa sähköpostilla.</li>
</ul>

## Demotilaisuus

<ul>
  <li id="demo" />
  <li><b>PAKOLLINEN!</b> Ota yhteyttä jos et pääse demotilaisuuteen, se on läpipääsyyn pakollinen!</li> 
  <li>Lähtökohtaisesti kaikki demoavat omalta koneeltaan. Voi olla hyvä saapua demoon hyvissä ajoin ja varmistaa että projektori/ruudun jako toimii. Jos omaa kannettavaa ei ole kannattaa demoamisesta sopia kaverin tai ohjaajan kanssa erikseen.</li>
  <li>Korkeintaan 5min per projekti.</li>
  <li>Ei tarvitse dioja, mutta halutessaan niitä voi käyttää, tosin ne vie aikaa, joten ei suositeltu, etenkään ellei tuo omaa konetta esitykseen.</li>
</ul>

<script>
  var elem = document.getElementById("demo");
  if (timing["demo2"]) {
    elem.innerHTML = "Paikat ja ajat:";
    var ulelem = document.createElement("ul");
    Object.keys(timing).filter(name => name.startsWith("demo")).map(name => fiEvent(timing[name])).forEach(ev => {
      var lielem = document.createElement("li");
      lielem.innerHTML = ev;
      ulelem.appendChild(lielem);
    })
    elem.appendChild(ulelem);
  } else if (timing["demo"]) {
    elem.innerHTML = "Paikka ja aika: " + fiEvent(timing["demo"]) + ".";
  } else {
    elem.innerHTML = "Aika ja paikka vahvistuvat myöhemmin.";
  }
</script>

## Esimerkkiprojektit

* [Saskelin projekti](https://github.com/saskeli/NonogramSolver_TiRa) **Huom:** että etenkin tämän jälkeen kurssi on jonkin verran muuttunut.
* Ja Jussi sanoi että [oma projektinsa](https://github.com/yussiv/Compress) oli kiireessä tehty mahdollisimman helpolla suoritettu.
* Molemmat kuitenkin (kuulemma) projektirakenteiltaan hyviä, jos haluaa esimerkkejä.

## 🏆 Kurssin suorittaminen
Kurssin työmäärä on opintopisteiden (4) perusteella n. 107 tuntia. Varaudu siis käyttämään työhön 15-20 tuntia viikossa jokaisella viikolla.

Kurssilla opiskelija toteuttaa ohjelman, joka ratkaisee jonkin ohjelmointiongelman. Ongelmanratkaisuun käytetään sopivia algoritmeja ja tietorakenteita. Aihe on vapaa, kunhan siinä on tarpeeksi algoritmista vaativuutta. Aihe-ehdotuksissa on aiheita, jotka ovat riittävän laajoja, mutta eivät liian laajoja. Työhön kuluva aika riippuu kuitenkin hyvin paljon aiemmasta osaamisesta. Jos valitset täysin oman aiheen, tai aihe-ehdotus ei ole täsmällinen, sovi mieluiten jo ensimmäisellä viikolla ohjaajan kanssa siitä, miten aihe kannattaa rajata, ja mitä sinun tulee toteuttaa itse, jotta saavutetaan sopiva laajuus. Suoritus ei edellytä oman algoritmin kehittämistä. Tämäkin on mahdollista, mikäli opiskelija haluaa haastavamman aiheen. Keskeistä työssä on, että ohjelma on tehokas ja toimii oikein. Työn aiheesta riippuu, miten suuria tapauksia ohjelman tulee pystyä käsittelemään. Mahdollisia aiheita voi katsoa [täältä](fi/aiheet).

Kurssi pidetään osittain verkkokurssina, kaikki viikoittaiset palautukset tapahtuvat verkon kautta. Toistaiseksi myös aloitusluento ja loppudemot pidetään etänä. Lisätietoa palautuksista [täällä](fi/palautukset).

Ohjelma toteutetaan **ohjaajan hyväksymällä** kielellä. Java on monikäyttöinen kieli, ja se soveltuu mihin tahansa aiheeseen. Python on joissakin asioissa hyvin hidas, mutta sillä voi tehdä lähes mitä vain, kunhan käytetään sen valmiita tietorakenteita, ja määritellään toteutus niin, että vaadittu laajuus tulee muusta kuin tietorakenteiden toteuttamisesta itse. Muilla kielillä on kullakin omat vahvuutensa, eikä ohjaaja tunne kaikkia kieliä lainkaan. Jos valitset muun kielen kuin Javan tai Pythonin, joudut itsenäisemmin arvioimaan kielen sopivuutta valitsemaasi aiheeseen, etkä ehkä saa ohjaajalta yhtä hyvin neuvoja siihen, kuinka jokin asia kannattaa toteuttaa käyttämälläsi kielellä, tai kuinka esimerkiksi yksikkötestaus tapahtuu. Jos tunnet jonkin kielen riittävän hyvin, voi olla hyvinkin perusteltua käyttää johonkin projektiin juuri sitä eikä Javaa tai Pythonia. 

Kurssin ensisijainen tavoite on oppia toteuttamaan itse tietorakenteita ja algoritmeja. Työn laajuutta arvioidaan siis niiden perusteella, ja oleellista on, että työssä on käytetty myös sellaisia algoritmeja tai tietorakenteita, joita ei ole käsitelty kurssilla Tietorakenteen ja algoritmit. Hyväksi koettu tapa tehdä työ vaiheittain on laittaa ensin kuntoon algoritmin ydin käyttäen kielen standardikirjastojen valmista kalustoa (tietorakenteet, järjestämisalgoritmit jne.). Kannattaa siis pyrkiä toteuttamaan algoritmin ydin nopeasti ja korvaamaan sen jälkeen valmis kalusto omilla toteutuksilla. Riippuu kuitenkin ohjelmointikielestä, voiko sillä toteuttaa itse jotain tietorakennetta niin tehokkaasti, että ohjelma toimii järkevässä ajassa, tai että kahden algoritmin vertailun tulos vastaa algoritmien tehokkuutta eikä riipu hitaasta tietorakenteesta, joka ei yleisesti ole niin hidas. Jos tietorakenteita ei ole mielekästä toteuttaa itse, pitää projektiin saada riittävä laajuus algoritmeista, ja toisaalta jos algoritmit ovat riittävän vaativia, voi käyttää valmiita tietorakenteita ja mahdollisesti myös kielen ulkopuolisia kirjastoja. 

Käyttöliittymä ei ole keskeinen asia kurssilla, mutta toimiva käyttöliittymä on tärkeä. Joissakin tapauksessa jopa komentoriviparametrit ovat riittävä tapa kommunikoida ohjelman kanssa. Yleensä kuitenkin tarvitaan ainakin valikko-ohjaus komentoriviltä. Usein myös selkeä visualisointi on välttämätön jo ohjelman kehitysvaiheessa, jotta näkee toimiiko ohjelma oikein. Graafisenkin käyttöliittymän koodaamiseen kuluva aika voi säästyä kehitys- / testausvaiheessa, jos siitä on ennestään kokemusta, ja jos joutuu paljon kokeilemaan ohjelmaa erilaisilla parametrien arvoilla yms. Valikko + ASCII-grafiikka on silti yleensä riittävä käyttöliittymä, kunhan se on hyvin tehty, eikä graafinen käyttöliittymä sinänsä ole tavoite tai arvosanaa nostava tekijä. Esim. reitinhakuohjelmissa ASCII-grafiikka kyllä rajoittaa käytetyn kartan kokoa ja sitä mitä asioita voidaan samassa kuvassa visualisoida.

## 📈 Arvosteluperusteet
* Ohjelma: 30 p
    * Toimivuus ja ominaisuudet 10 p
    * Testaus 10 p
    * Dokumentoiva koodi (JavaDoc sekä itsedokumentoiva) 5 p
    * Ohjelmakoodin selkeys 5 p

* Dokumentaatio 10 p
    * Aiheen määrittely 2p
    * Ongelman toteutus 3p
    * Testaus 3p (myös suorituskykytestaus!)
    * Käyttöohje 2p

* Arvostelu kurssin aikana 20p
    * Vertaisarvioinnit 2 * 4p = 8p
    * Viikkopalautukset 6 x 2p = 12 p

(Yhteensä 60 p)

Kurssin hyväksytysti suorittaminen vaatii ohjelmalta itsetoteutettuja tietorakenteita sekä toiminnallisuutta. Kukin työ arvioidaan omana kokonaisuutenaan, alla viitteelliset pisterajat. Arvosanaan 5 edellytetään riittävän pistemäärän lisäksi, että projektin laajuus on riittävä, testaus on vakuuttava, dokumentaatio on moitteeton ja molemmat vertaisarviot on tehty ohjeiden mukaisesti.

* 5: 50 p
* 4: 45 p
* 3: 40 p
* 2: 35 p
* 1: 30 p
