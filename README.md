# CCLuokkaharjoituksia
Esimerkkejä ja harjoituksia C# luokista ja olioista

## Luokkien periytyminen
Luokka voi periä toiselta luokalta kenttiä ja metodeja. Luokkaa, jonka ominaisuuksia peritään (inheritance) kutsutaan yliluokaksi (superclass, parent class) ja perivää luokkaa aliluokaksi (subclass, child class). Perimisen keskeinen idea on se, että yliluokassa määriteltyjä ominaisuuksi (kenttä) ja metodeja ei tarvitse enää määritellä aliluokassa, riittää että kerrotaan niiden periytyvän yliluokasta. Yliluokalla ja aliluokalla voi olla saman nimisiä metodeja, jotka toimiviat eri tavalla. Tätä kutsuttaa metodien ylikirjoittamiseksi (method overload). Alemmissa versioissa aliluokassa määritelty metodi, joka on kirjoitettu eri tavalla kuin yliluokassa, syrjäytti aliluokan saman nimisen metodin. Uusimmat kääntäjät eivät kuitenkaan toimi näin. Aliluokan metodi voi myös syrjäyttää yliluokan metodin silloin, kun yliluokan metodi on määritelty virtuaaliseksi (virtual) ja aliluokasssa metodi on määritelty syrjäyttäväksi (overload). Toinen vaihtoehto on käyttää aliluokan metodin määrityksessä "new" -komentoa yliluokan metodin syrjäyttämiseksi. Jos "new" jätetään pois aliluokka syrjäyttää edelleen yliluokan (toisin kuin dokumentaatiossa lukee). Seuraavassa esimerkissä on kolme luokkaa: yliluokka, lemmikinomistaja sekä kaksi aliluokkaa kissanomistajalle ja koiranomistajalle.

      '''csharp
    
      // Super/Base/properties of Hooman ie. fields
      class Hooman
      (
      public string name - "Essi Esimerkki";
      public int age -30;
      public string - "Emäntä";
    
      // Default constructor w/o arguments
      // No need to define, will be created automatically
      public Hooman()
      (
    
      )
  )

  // Sub/Deriver/Child class inherits Hooman class
  class CatOwner : Hooman
  (
      // Define the method differently in subclass
      public new voi SayOpinion()
      ( Console.WriteLine("Kissat ovat itsenäisiä ja pitävät hiiret loitolla");
      )
  )
  '''
Tehtävä1
Rakenna koiranomistajalle perivä luokka ja sille ylikirjoittava SayOpinion-metodi

// Create a new dog owner and call SayOpinion method
DogOwner dogOwner = new DogOwner();
dogOwner.SayOpinion();
Perinteisesti metodin ylikirjoittaminen aliluokassa on määritelty käyttämällä komentoja virtualja override:

Tehtävä 2
Tee yliluokka Pet ja sille aliluokka Hare. Määrittele metodi Eats, joka tulostaa ruudulle eläimen ruokavalion. Pet-luokassa tyyliin "Syö ruokaa" ja aliluokassa "Syö porkkanoita". Käytä perinteistä määrittelyä virtuaaliseksi metodiksi ja ylikirjoitettavaksi metodiksi.

Tehtävä 3
Luo uusi sovellus (solution) ja projekti. Asetukset C#, Windows-alustalle ja Console-sovellustyypiksi. Sovelluksen avulla kerätään tietoa tietoteknisistä laitteista. Kaikille laitteille yhteisiä ominaisuuksia ovat:

Hankintapäivä (string)
Hankintahinta (double)
Takuuaika kuukausina (int)
Kiinostuksen kohteena ovat tietokoneet, puhelimet ja tabletit. Rakenna näille luokkamääritykset ja periytä yhteiset ominaisuudet yliluokasta. Muista kommentoida koodia. Mieti mitä metodeja tarvittaisiin esim. jäljellä olevan takuuajan selvittämiseksi. Mieti mitä eroja tietokoneilla ja muilla laitetyypeillä on. Tee tietokoneille, puhelimille ja tableteille omat luokat ja mieti, mitä kenttiä aliluokissa pitäisi olla.

Tee tätä tehtävää varten oma Github-repositorio Laiterekisteri. Ota se käyttöön Visual Studiossa, jotta voit versioida kirjoittamaasi koodia.
