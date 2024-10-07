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
AFBEELDING VAN SVELTE-STRUCTUUR TOEVOEGEN

Binnen sveltekit zijn de `src`, `routes` en de `app.html` noodzakelijk. Zonder deze files kan je project niet draaien.

In de `package.json` staat een lijst met depencies die nodig zijn om het project te runnen.

In je `.env` staat geheime informatie die niet op straat mogen.

In je `.env.example` staat een layout waarin je kan zien welke geheime informatie je nodig hebt om het project te runnen.


### Routing
Zorg dat je routes vanaf het begin altijd goed opgebouwd zijn, als je hier in het begin een fout in maakt ben je de rest van je project verdwaald.

### Error Handling
routes/+error.svelte zorgt voor een custom error-pagina. Deze werkt als er ook nog maar iets werkend is van svelte.

`script`
`import { page } from '$app//stores'`
`script`

`{$page.status} - {page.error.message}`


### Loading Data
Voor het inladen van gegevens zijn de `+page.server.js` en de `+page.js` van toepassing. 

Hierbij heeft de server.js altijd async

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
Hoeveelheid planning-punten die je per sprint kunt verbranden.