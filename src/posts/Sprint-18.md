---
title: User Needs
description: Hier documenteer ik wat ik heb geleerd in sprint 18.
date: '2025-01-06'
categories:
  - Semester 3
  - Sprint 18
published: true
status: false
value: 1
---

## Static Site Generation
### Client-side rendering (CSR)
De webbrowser laadt een leeg HTML bestand in. Met JS en CSS wordt de connectie gemaakt met een backend en de pagina gerendered.

### Server-side rendering (SSR)
Bij elke aanvraag wordt er op de server connectie gemaakt, en de pagina gerendered. De webbrowser ontvangt de complete HTML voor de pagina.

### Static site generation (SSG)
Tijdens de build worden alle mogelijke pagina's al gerendered. Het resultaat hiervan is een statische website die eenvoudig gehost kan worden.

Als je dit wilt gebruiken kun je binnen sveltekit een `adapter-static` installeren en aanpassingen maken in de `svelte.config.js`. 

### Incremental static regeneration (ISR)
Bij elke build worden alleen de pagina's gerendered die zijn veranderd. 

### Content delivery network (CDN)
Een CDN is een netwerk van servers die statische bestanden opslaan. Wanneer iemand een aanvraag doet naar je website, gaat deze naar de hosting omgeving in de buurt van de gebruiker, ipv naar de andere kant van de wereld, naar jouw server.

Voordelen
- veiligheid
- performance
- schaalbaarheid
- gratis hosting

Nadelen
- build time
- minder dynamische content

### Continuous integration (CI)
Het automatiseren van de integratie van codeaanpassingen binnen een softwareproject. Een voorbeeld van een hosting die dit doet is Vercel.

### Wat zou voor mijn huidige project de juiste deployment strategie zijn?
Wij denken dat SSR het beste aansluit bij ons project. Mede doordat wij gebruik maken van dynamische content en dat de pagina makkelijk gevonden moet kunnen worden voor potentiële klanten van WoGo.

## GSAP
GSAP werkt volgens tijdlijnen waarmee je alles kunt animeren. Het is een grote library die door alle grote bedrijven wordt gebruikt.

### Tween
Een tween is hetgene dat al het animatie werk doet. Je geeft de tween verschillende objecten mee, een duratie en elke property die je maar wilt.

Simpele methoden om een tween te gebruiken is aan de hand van:
- gsap.to()
- gsap.from()
- gsap.fromTo()

### Timeline
Een timeline is simpelweg de container die de tweens bevat. Op deze manier kun je de tweens gemakkelijk besturen met bijvoorbeeld `pause()`, `play()` etc. etc.

````
                        PLAYHEAD
|--------------timeline-----|-----------|
|--tween1--|                |
           |-----tween2-----|-----------|
````

Om een timeline te maken kun je het volgende gebruiken:
- gsap.timeline()