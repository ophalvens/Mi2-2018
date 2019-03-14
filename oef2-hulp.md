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

## Active/hover effect op de kleine afbeeldingen
Dit effect is een uitbreiding op wat we tijdens de eerste oefening hebben gedaan
  * Maak in css een effect op voor :hover en .active
  * In de eventlistener op de thumbnails zorg je er voor dat de class ```active wordt``` toegevoegd aan de aangeklikte thumbnail.
  * Als je dit effect niet wilt laten staan bij het aanklikken van een volgende thumbnails, moet je eerst dit effect verwijderen. Hier zijn meerdere strategieën moglijk. Hieronder enkele :
    * Verwijder de class ```active``` van alle thumbnails voor je die toepast op de aangeklikte tumbnail. Doe dit voordat je de ```active``` toepast op de net aangeklikte thumbnail.
    * Hou bij het klikken op een thumbnail in een (globale) variabele bij welke de net aangeklikte thumbnail is, zodat je specifiek van dat element de class ```active``` kan verwijderen voor je de active toepast op de aangeklikte thumbnail.
    * Zoek voor het verwijderen van de ```active``` alle img op met een ```active``` class en verwijder daarvan de ```active``` van de ```classList```

## Filters
### Met de album
Kijk naar de structuur van de foto's in html. Waaraan kan je zien in welke album een foto zit?
Kijk naar de waarden van de verschillende options van de select.
  * Werk met een 'change' eventlistener op de select
  * Hou een lijst bij van alle elementen die je wilt tonen/verbergen. Omwille van perfmantie hou je die best bij in een variabele buiten je eventlistener.
  * Loop door de lijst van elementen. Toon de elementen van de gewenste album, verberg de andere.
  * Let op : het eerste element van de select heeft geen bestaande albumId, maar het is net bij deze waarde dat je alle foto's wilt tonen.

### Filteren op het jaar
Kijk naar de structuur van de html. Merk op dat dit gelijkaardig is aan die van de album, maar op basis van een ander attribuut.
Dit betekent dus dat je op een gelijkaardige manier zal kunnen filteren, met een aantal belangrijke aanpassingen.
  * Je moet met een eventlistener werken op de 3 checkboxen.
  * Er kunnen 0, 1, 2 of 3 jaartallen geselecteerd worden. Wat wil je dat er getoond wordt in deze gevallen?
  * De makkelijkste manier om gestructureerd met deze jaartallen te werken, is om deze in een object te stoppen als eigenschappen en deze standaard op true te zetten. Wanneer de checked waarde van een checkbox wijzigt, wijzig je ook deze waarde. Bij het uitvoeren van je filter maak je dan gebruik van dat opbject.
  * Het is makkelijker als je er van uit gaat dat je er van uit gaat dat standaard alle jaartallen aangevinkt zijn. Het meest eenvoudige is dat met html te doen (```checked```).
  * Aangezien we nu met meer filters willen werken, plaats je die array 
  * Maak van het filteren een aparte functie