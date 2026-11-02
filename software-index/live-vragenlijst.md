---
id: QAwebinars/live-vragenlijst
naam: Live vragenlijst voor een webinar met een moderator die vragen invoert en een spreker die ze afvinkt
soort: software
bestanden: [index.html]
afgeleid_van:
---
## Wat ze doet
Eén losse webpagina waarmee twee mensen tijdens een live sessie samen een vragenlijst bijhouden: de moderator typt binnengekomen vragen in (naam, vraag, aantal stemmen), de spreker ziet ze meteen op zijn eigen scherm in grote letters. Elke vraag gaat van "te beantwoorden" naar "bezig" naar "beantwoord"; de spreker kan een vraag bovenaan zetten en de letters groter of kleiner maken, de moderator kan bewerken, verwijderen en een per ongeluk gestarte vraag terughalen. Alles wordt meteen gelijkgezet tussen beide schermen via Firebase Realtime Database; er is geen eigen server nodig, de pagina kan als statisch bestand online staan (bv. GitHub Pages). Nodig: een eigen Firebase-project met een Realtime Database en de webconfiguratie daarvan. Het doet geen inloggen of afscherming (wie de link en de database kent, kan schrijven), haalt geen vragen automatisch uit een webinarplatform en bewaart geen geschiedenis buiten de database.
## Varianten
## Inbouwen
Kopieer `index.html`. Vervang bovenaan het script het blok `firebaseConfig` door de configuratie van je eigen Firebase-project (en zet in Firebase databaseregels die passen bij je gebruik). Pas het databasepad `kc26-qa/questions` aan naar een eigen naam, en vervang de projectgebonden teksten: de titel "KC26", de evenementnaam en de namen van moderator en spreker op het keuzescherm. De rest (statussen, volgorde, lettergrootte, opmaak) werkt zonder aanpassing; teksten in de interface zijn in het Nederlands.
