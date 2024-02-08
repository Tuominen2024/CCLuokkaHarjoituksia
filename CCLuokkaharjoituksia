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
