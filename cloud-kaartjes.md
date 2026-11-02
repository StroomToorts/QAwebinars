bevindingen 2

Nagekeken: README.md (leeg), index.html (de hele app, één bestand). Er is geen CLAUDE.md of STATUS.md in deze repo.

## Kaartjes

- `software-index/live-vragenlijst.md`: herbruikbaar omdat het een volledig werkend, losstaand Q&A-hulpmiddel is voor elk live webinar of elke presentatie; alleen de Firebase-configuratie, het databasepad en een paar namen moeten aangepast.
  - ernst: n.v.t. (bouwsteen, geen fout)
  - bestand en regel: index.html, regel 489 en verder (script), configuratie regel 492-500, databasepad regel 538
  - scenario: een ander project wil een gedeelde lijst tussen twee schermen tijdens een live sessie
  - voorstel: kopieer index.html, vul eigen Firebase-configuratie en databasepad in, vervang de KC26-teksten
- `software-index/rol-per-link-zonder-server.md`: herbruikbaar als ontwerppatroon voor elk klein samenwerkingshulpmiddel met vaste rollen, ook zonder de code over te nemen (rol in de link, één statisch bestand, gedeelde live staat, volgorde met één getal, controle op invulwaarden in de configuratie).
  - ernst: n.v.t. (bouwsteen, geen fout)
  - bestand en regel: index.html, `isConfigured` regel 513, `selectRole` regel 553, `moveToTop` regel 642, `renderQuestions` regel 692
  - scenario: een ander project bouwt een scorebord, wachtrij of regietool voor meerdere mensen tegelijk
  - voorstel: neem het patroon over, eventueel met een andere realtime dienst dan Firebase

## Overwogen maar niet gekozen

- `escHtml` (regel 777): nuttig maar te klein en te algemeen voor een eigen kaartje; vermeld in het werkingsprincipe.
- Lettergrootte-knoppen voor de spreker (`adjustFont`): te klein, hoort bij de vragenlijst.
- Donkere kleurenset en kaartopmaak (CSS-variabelen): projectgebonden huisstijl, geen echte bouwsteen.
- Inhoud (KC26, namen van moderator en spreker, Firebase-project): projectgegevens, niet herbruikbaar en bewust niet in de kaartjes gezet.

## Terloops opgemerkt (niet gewijzigd)

- De Firebase-webconfiguratie staat leesbaar in index.html (regel 492-500). Dat is bij Firebase-websleutels normaal, maar dan hangt de afscherming volledig af van de databaseregels; wie de pagina kent, kan vragen toevoegen of wissen als die regels open staan. Voorstel: databaseregels nakijken.
