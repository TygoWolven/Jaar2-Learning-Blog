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

## Clean Code & Refactoring

### Clean Code
Robert C. Martin heeft een boek geschreven genaamd: _"Clean Code"_. Het schrijven van clean code doe je om jezelf 
een proffesional te kunnen noemen. Er zijn geen smoesjes om minder dan je best te doen. Code is clean als het gemakkelijk 
te begrijpen is voor iedereen in het team. Begrijpelijk betekent in dit geval: leesbaar, aanpasbaar, uitbreidbaar en onderhoudbaar.

#### The Scout Rule
Try and leave this world a little better than you found it...

- Gebruik betekenisvolle namen voor variabelen, functies en bestanden.
- Vermijd cryptische afkortingen zoals, a, x, data of temp.

#### Schrijf kleine functies
Functies moeten klein zijn en slechts één verantwoordelijkheid hebben. Lange functies zijn moeilijk te begrijpen en onderhouden.

#### Gebruik goed commentaar
Less is more. Goede code heeft weinig commentaar nodig omdat het zichzelf uitlegt. Gebruik commentaar alleen als de code zonder context niet duidelijk is.

#### Maak je code leesbaar (voor mensen)
Code wordt vaker gelezen dan geschreven. Maak het daarom intuItief en helder, alsof je schrijft voor een collega. Inspringen, witruimte en consistsentie zijn cruciaal.

### Refactoring
Refactoring is het proces van het verbeteren van code zonder de functionaliteit te veranderen.

- Hernoem functie declaraties: Het doel is om de functie beter aan te laten sluiten bij de behoeften van de codebase zonder gedrag te veranderen.
- Splits conditionals op: Complexe en onoverzichtelijke statements worden opgesplitst in kleinere stukjes.
- Vervang loops door pipelines
- Verwijder dode code: Overbodige of niet gebruikte code wordt opgespoord en verwijdert uit de codebase, denk hierbij aan functies die nooit worden aangeroepen.
- Verschuif statements: Herpositioneren van code binnen een methode om de leesbaarheid en logische volgorde te verbeteren. _(Gebruik de Alt toets om makkelijk te verschuiven.)_

### Sveltekit Best-practices
/src/lib voor componenten en helpers
/ars/routes voor layouts en pagina's
/static voor statische assets

#### Performance
Code-splitting
Asset preloading
File hashing
Request coalescing
Parallel loading
Pre-rendering
Link preloading

## WebGL / Shaders / Three.js
Three.js is een JavaScript bibliotheek voor het maken van 3D werelden, animaties en visualisaties op het web. Het bestaat uit 3 kernonderdelen: 
- Scene - is je werkomgeving waar de 3D objecten zich bevinden
- Camera - waarmee je naar de 3D objecten gaat kijken (het oogpunt)
- Renderer - het systeem dat alles gaat tekenen

### Cameras
Perspective camera - Hiermee kun je perspectief zien (3D)
Orthographic camera - Hiermee zie je geen perspectief (2D)

### Meshes
Geometry en een material is wat een mesh vormt. Een mesh kan bijvoorbeeld een bankje zijn die in de scene staat. 

### Shaders
Vertex shader
Fragment shader is de belangrijkste shader, want deze gaat een kleur toekennen aan wat je getekent hebt.

### Tutorial
Bruno Simons heeft een gratis tutorial voor mensen die willen beginnen met 3D op het web:

https://threejs-journey.com/#summary
https://tympanus.net/codrops/

## WebGL
Een handige extensie om te beginnen met WebGL is Spector.js.
