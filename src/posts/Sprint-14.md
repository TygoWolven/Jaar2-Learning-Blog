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
Voor het inladen van gegevens zijn de `+page.server.js` en de `+page.js` van toepassing. 

Hierbij heeft de server.js altijd async

```js
export async function load() {
  return {
    foo: 'bar'
  }
}
```

### Binding

`script`
  `let name = 'world'`
  `$: shout = name + 'rocks!'`
`script`

input bind:value={name}

`h1Hello {name}!/h1`
`p{shout}/p`


### Library & Components
De meeste framework projecten hebben een bibliotheekfunctie. De library.

In de library kun je alles hergebruiken. Denk aan de `Header.svelte`. De naam van het bestand moet altijd met een hoofdletter beginnen.

Vervolgens is dit bestand her te gebruiken door gebruik te maken van de volgende code:

`import {Header} from '$lib'`

"index.js"...
`export { default as Header } from './Header.svelte`

Ook heb ik de voorbeeldrepo van Justus gedownload na het college.


## Design Critique
Dieter Rams
10 Principles of good design

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
Een sprint-review is kijken naar wat je gemaakt hebt en hoe ver je bent met de opdrachtgever

Hierbij ga je:
-Specifieke vragen bedenken om feedback te krijgen
-Specifieke vragen stellen om feedback te krijgen
-Een demo geven aan de opdrachtgever om de applicatie te laten zien
  - Langs userstories gaan
  - Website laten zien naast het design
  - Werk van deze sprint laten zien
  - Laten zien waar je nog niet aan toe bent gekomen (adhv het design)
-Een voorstel geven om het product mogelijk te kunnen verbeteren
-Uitkomst van testen bespreken om zo verbeteringen te laten zien
-Planning voor de volgende review geven
-Werk opleveren / vragen hoe ze het opgeleverd willen hebben

Rollen tijdens Sprint Review:
Feedback verwerker (Github Issues)
Presentator
Timekeeper
Cheerleader

## Voorbereiding Sprint Review

Ik heb een vraag over wat de opdrachtgever vind van mijn design voor het lijstje sprints.
Zelf ben ik er niet heel enthousiast over dus misschien dat de opdrachtgever hier leuke ideeën voor heeft.
