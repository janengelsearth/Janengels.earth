# janengels.earth

Persoonlijke website van Jan Engels. Statische site: `index.html` is de hele site.
Na elke wijziging op `main` bouwt statichost.eu de site automatisch opnieuw (webhook).

## Onderhoud van bronnen (link-rot)

Twee automatische controles in `.github/workflows/`:

- **Linkcontrole** (`linkcontrole.yml`): elke 1e van de maand en na elke wijziging van `index.html` worden alle links nagelopen. Werkt er een niet meer, dan verschijnt onder *Issues* een melding "Kapotte links" met de lijst. LinkedIn wordt overgeslagen: die site blokkeert controles.
- **Bronnen archiveren** (`archiveren.yml`): na elke wijziging van `index.html` en elk kwartaal wordt elke externe bron bewaard in het Internet Archive (web.archive.org). Is een bron later verdwenen, dan staat de kopie daar. Het overzicht staat bij *Actions* → *Bronnen archiveren* → de laatste run.

Handmatig starten kan via *Actions* → kies de workflow → *Run workflow*.

Afspraken bij nieuwe bronnen: altijd titel, uitgever en datum vermelden (dan blijft de bron vindbaar zonder link), en bij voorkeur vaste adressen gebruiken (wetten.overheid.nl, officielebekendmakingen.nl, CBS).
