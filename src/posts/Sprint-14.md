---
title: Sprint 14 - Lose your Head
description: Hier heb ik gedocumenteerd wat ik heb geleerd in Sprint 14.
date: '2024-9-23'
categories:
  - Semester 3
  - Sprint 14
published: true
---

## Sveltekit Principles

### Structure
````ts
// Hier zie je een standaard sveltekit-structuur
my-project/
- src/
  - lib/
    - server/
  - routes/
    - +page.svelte
  - app.html
  - error.html
- static/
  - assets/
- .env
- .env.example
- package.json
- svelte.config.js
- tsconfig.json
- vite.config.js
````

Binnen sveltekit zijn de `src`, `routes` en de `app.html` noodzakelijk. Zonder deze files kan je project niet draaien. In de `package.json` staat een lijst met depencies die de developer zal moeten hebben om het project te runnen.

Dan heb je nog de `.env` bestanden. In het normale bestand staan dingen zoals je API-key die niet gepubliceerd mogen worden. Echter zijn deze wel nodig om het project te kunnen runnen. Daarnaast heb je nog het `.env.example` bestand. Hierin laat je een soort layout zien zodat de andere developer wel weet welke geheime informatie er in moet komen te staan.

### Routing
Bij het aanmaken van routes binnen je sveltekit-project kun je er altijd maar beter voor zorgen dat alles vanaf het begin al goed is opgebouwd. Als je hier in het begin al fouten in maakt is de kans groot dat je verder in het project verdwaald gaat raken.

### Error Handling
Sveltekit heeft standaard zijn eigen error page, maar deze kun je ook heel gemakkelijk zelf overnemen om hiervan een leuke error-page te maken. Hierbij zorgt de `routes/+error.svelte` voor een custom error-page. Deze zal getoond worden bij elke error die mogelijk kan opspelen binnen de website.

Om de error-status en bericht te laten zien kun je de volgende code neerzetten binnen het `+error.svelte` bestand. <br>

````
import { page } from '$app//stores'

{$page.status} - {page.error.message}
````

### Loading Data
Voor het inladen van gegevens zijn de `+page.server.js` en de `+page.js` van toepassing. Hierbij moet je ervoor zorgen dat de de `server.js` altijd een async heeft.

```js
export async function load() {
  return {
    foo: 'bar'
  }
}
```

### Binding
Binnen sveltekit is het mogelijk om elementen met elkaar te verbinden. Zo kun je bijvoorbeeld een `input` verbinden met een `p`. Zo komen op beide plekken dezelfde content te staan. Dit doe je door en het `script` veld de volgende code neer te zetten:
````
let name = 'world'
$: shout = name + 'rocks!'
````
Daarnaast zet je in de `HTML` het volgende:
````
<input bind:value={name}>

<h1>Hello {name}!</h1>
<p>{shout}</p>
````

### Library & Components
De meeste framework projecten hebben een bibliotheekfunctie, de library. In de library kun je alles hergebruiken (componenten). Denk hierbij bijvoorbeeld aan de `Header.svelte`. De naam van het bestand moet altijd met een hoofdletter beginnen, maar dit zorgt ervoor dat je de `header` automatisch op elke pagina kan laten zien, zonder dat je deze elke keer opnieuw hoeft te schrijven.

Om zo een component te gebruiken moet je de volgende code toepassen:
````
// In de +layout.svelte of de +page.svelte
import {Header} from '$lib'
{Header}

// In de index.js 
export { default as Header } from './Header.svelte
````

## Design Critique
Een Design Critique is een sessie waarbij teamleden gaan kijken naar elkaars designs, en hier volop kritiek op gaan geven. Dit kan zowel goede, als slechte kritiek zijn. Het doel hiervan is om nieuwe inzichten te krijgen over het design.

Om te kijken wat goede designprincipes zijn kun je kijken naar het artikel van Dieter Rams waarin hij 10 principes geeft voor goed design.

Bron:
https://tenprinciples.design/

## FDND Agile Woordenlijst
Agile Development

Backlog

Business Owner:
Eigenaar van een bedrijf.

Continuous Integration:
Een automatische integratie van de live-website zodra er updates zijn.

Daily Scrum

Definition of Done

Epic

Feature

Iteration

Minimal viable product:
Het minimale werk dat je kunt opleveren voor een project.

MoSCoW

Optimum viable product:
Het maximale werk dat je kunt opleveren voor een project.

Planning poker

Product owner:
De persoon die meestal een opdracht aanbied, en hierbij stories aanmaakt.

Refactoring

Retrospective

Release

Scrum

Scrum Master

Scrum Team

Sprint

Sprint Goal

Sprint planning

Sprint review

Stand-up:
Snelle meeting waarin je bespreekt wat je gaat doen, waar je tegen aan loopt en of je hulp nodig hebt.

Stakeholders:
Mensen die op een of andere manier te maken hebben met het project.

Task

Task board

Task points

Velocity:
Hoeveelheid planning-punten die je per sprint kunt verbranden.`

## Sprint Review: over hoe je deze kan voorbereiden
Een sprint-review is kijken naar wat je gemaakt hebt en hoe ver je bent met de opdrachtgever.

### Wat ga je doen?
-Specifieke vragen bedenken om feedback te krijgen <br>
-Specifieke vragen stellen om feedback te krijgen 

-Een demo geven aan de opdrachtgever om de applicatie te laten zien
  - Langs userstories gaan
  - Website laten zien naast het design
  - Werk van deze sprint laten zien
  - Laten zien waar je nog niet aan toe bent gekomen (adhv het design) 

-Een voorstel geven om het product te verbeteren <br>
-Uitkomst van testen bespreken om zo verbeteringen te laten zien <br>
-Planning voor de volgende review geven <br>
-Werk opleveren / vragen hoe ze het opgeleverd willen hebben

### Welke rollen zijn er?
Feedback verwerker (Github Issues)

Presentator

Timekeeper

Cheerleader

## Vragen ter voorbereiding op de Sprint Review
Voor de sprint review heb ik een aantal vragen voorbereid die ik wil gaan stellen:
- Wat vind je van het design van het lijstje met sprints?
  - *Dit wil ik vragen omdat ik zelf niet erg enthousiast ben over het design, dus mogelijk krijg ik wat inzichten van de opdrachtgever.*
- Zijn er bepaalde functies die je graag zou willen zien binnen het project?