# BrusselsExplorer — Dynamic Web (Herexamen)

Deze webapp toont gegevens uit de dataset **"Recycleries - Ressourceries - Repair Cafés"** van [opendata.brussels](https://opendata.brussels.be), met een tabel en kaartweergave.

## Functionaliteiten
- Ophalen van minstens 20 records uit de API (met paginatie en infinite scroll).
- Tabel met 6 vaste kolommen: **titel – naam – datum – adres – gemeente – type**.
- Kaartweergave met markers en popups (Leaflet).
- Zoekfunctie op tekst.
- Sorteren op elk veld en op afstand (na geolocatie).
- Filteren via facetten.
- Favorieten (⭐) met mogelijkheid tot notities.
- Donker/licht thema.
- Responsive design.

## Gebruikte API's
- **Opendata.brussels** (Opendatasoft Explore v2.1)
  - Records endpoint: `https://opendata.brussels.be/api/explore/v2.1/catalog/datasets/{dataset_id}/records`
  - Facetten endpoint: `https://opendata.brussels.be/api/explore/v2.1/catalog/datasets/{dataset_id}/facets`
- Dataset: `recycleries-ressourceries-repaircafes-vbx`

## Technische vereisten — waar in code?
- **DOM manipulatie**: `renderRows`, `buildHeader`, `bindEvents`
- **Events**: `bindEvents()` voor click en submit
- **Modern JavaScript**: gebruik van `const`/`let`, template literals, `map`, `filter`, `for...of`, arrow functions, ternary operator, callbacks, Promises, async/await
- **Observer API**: `IntersectionObserver` in `setupInfiniteScroll`
- **Data & API**: `fetchJSON`, `buildUrl`, `normalizeRecord`, `formatField`
- **Opslag & validatie**: `saveJSON`, `loadJSON`, formulier-validatie in notitie-formulier
- **Styling & layout**: CSS Grid/Flex, toegankelijke knoppen en toggles

## Installatiehandleiding
1. Download `index.html`.
2. Open het bestand in je browser (internet vereist voor API en Leaflet-kaart).
3. Of publiceer via GitHub Pages:
   - Maak een publieke repo aan, upload `index.html` in de root.
   - Ga naar **Settings → Pages** en zet branch op `main` en root `/`.
   - Wacht tot de link actief wordt.

## Screenshots
![donker thema](<Screenshot 2025-08-11 at 23.21.34-1.png>)
![zoekbalkje](<Screenshot 2025-08-11 at 23.22.08.png>)
![pagina](<Screenshot 2025-08-11 at 23.21.28.png>)

## Bronnen
- Opendatasoft Explore API v2.1 — officiële documentatie
- Dataset `recycleries-ressourceries-repaircafes-vbx` op opendata.brussels
- LeafletJS documentatie