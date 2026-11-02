---
id: QAwebinars/rol-per-link-zonder-server
naam: 'Eén statische pagina voor meerdere rollen, gekozen via de link, met gedeelde realtime staat'
soort: werkingsprincipe
bestanden: [index.html]
afgeleid_van: klaswerkplaats/agenda-firebase-statisch
---
## Wat ze doet
Een klein samenwerkingshulpmiddel voor een paar vaste rollen bouw je als één HTML-bestand zonder eigen server: de rol staat in de link (`?role=moderator` of `?role=presenter`), zodat elke deelnemer een eigen bladwijzer krijgt en na herladen in dezelfde rol terugkomt; zonder rol in de link verschijnt een keuzescherm dat de gekozen rol in de adresbalk zet. Beide rollen luisteren naar hetzelfde stuk van een realtime database en tekenen bij elke wijziging de hele lijst opnieuw; alleen de knoppen verschillen per rol. Volgorde houd je bij met een getal per item, en "naar boven" zet dat getal op één minder dan het kleinste, zodat je nooit andere items hoeft te herschrijven. Bij het opstarten controleert de pagina of de configuratie nog een invulwaarde (`JOUW_...`) bevat en toont dan een duidelijke melding in plaats van stil te falen. Dit is geen beveiliging: de rol in de link bepaalt alleen wat je ziet, niet wat je mag; echte afscherming vraagt databaseregels of inloggen.
## Varianten
## Inbouwen
Kijk in `index.html` naar `init`, `selectRole` (rol uit en naar de link), `moveToTop` (volgorde met één getal), `isConfigured` (controle op invulwaarde) en `renderQuestions` (alles opnieuw tekenen bij elke wijziging). Neem het patroon over in je eigen pagina met je eigen rollen en gegevens; de Firebase-koppeling kan vervangen worden door een andere dienst die wijzigingen live doorstuurt. Toon gebruikerstekst altijd via een ontsnappingsfunctie zoals `escHtml` wanneer je met `innerHTML` tekent.
