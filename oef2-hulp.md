# Mobile & Internet 2 - Opgave 2
  * bekijk het filmpje
  * bekijk de startcode in een browser
  * gebruik de browser inspector om snel een idee te krijgen van de structuur van de onderdelen

Er zijn meerdere manieren om deze opgave uit te werken. Hieronder staat uitleg voor 1 manier.

## Login venster verbergen/tonen
  * bij de start moet de ```#loginmodal``` verborgen zijn. Werk hiervoor met de CSS ```translateY()``` functie in de css definitie ```#loginmodal```.
  * bij klik op de ```#btnLogin``` moet deze loginmodal getoond worden
  * plaats een transitie in de ```#loginmodal```
  * werk met een eventlistener die je op de ```#btnLogin``` hangt om de modal te tonen (voeg een class toe aan de classList van ```#loginmodal```).
  * wanneer je op ANNULEER klikt, moet ```#loginmodal``` verbergen. 

## Formchecking login modal
  * zorg voor aangepaste boodschappen wanneer 1 of beide velden leeg zijn.
  * zorg voor aangepaste tekst indien het email adres de algemene vorm van een email adres niet volgt.
  * je kan je hiervoor baseren op het voorbeeld op https://rogiervdl.github.io/JS-course/02_dom.html#/example-2-formchecking
    * onderschep het submit event (https://rogiervdl.github.io/JS-course/02_dom.html#/intercepting-the-form)
    * kijk na of de input correct is, indien niet, zorg voor een aangepaste boodschap
    * als beide velden ingevuld zijn, en het email adres is qua vorm correct (bevat een ```@``` , gevolgd door toegelaten tekens, gevolgd door een ```.``` gevolgd door een aantal tekens), haal je de class weg die je hebt toegepast op ```#loginform``` om deze te tonen, zodat het terug verdwijnt.
    * als je zoekt naar 'javascript regex email' kom je verschillende mogelijke zoekpatronen en voorbeelden tegen om email adressen na te kijken. Voor deze oefening moet het geen uitgebreide controle zijn.
  
## Interactie foto's
### Klikken op de kleine foto's
Je kan kijken naar het voorbeeld op https://rogiervdl.github.io/JS-course/02_dom.html#/example-1-slideshow als je bij dit onderdeel vast zit.
Bestudeer eerst het filmpje en de structuur van de html code.

  * Vervang de grote foto door de grote versie van de kleine foto waar je net op klikte. Bestudeer de html om te zien hoe je met javascript tot het juiste element met de afbeelding geraakt.
  HINT: het is de eerste (enige) img binnen ```large__figure``` 
  * vervang de tekst in ```.large__title``` door de alt van de kleine foto waar je net op klikte
  * 