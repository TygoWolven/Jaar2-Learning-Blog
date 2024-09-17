---
title: Sprint 13 - Your Tribe for Life
description: Hier heb ik gedocumenteerd wat ik heb geleerd in Sprint 13.
date: '2024-9-02'
categories:
  - Semester 3
  - Sprint 13
published: true
---

## Getting started with Directus and Sveltekit

````ts
npm create svelte@latest project-naam
// Kies voor een Skeleton Project
// Zet de Typescript functie uit
// Kies vervolgens features uit naar keuze (Optioneel)
cd project-naam
npm install
npm run dev
````

Ons eerste huiswerk ging om het kennismaken met Directus en Sveltekit . Hierbij moesten we een tutorial 
volgen genaamd: "Getting started with Directus and Sveltekit". Tijdens het volgen van de stappen kwam ik 
vast te lopen op het deel waarop mijn data getoond zou moeten worden. Ik kreeg dat maar niet voor elkaar, 
mogelijk had dat te maken met dat de Directus omgeving niet goed is ingesteld.

Omdat ik hier vast liep, ben ik begonnen met een andere Tutorial over Sveltekit. Namelijk 'learn.svelte.dev', 
dit is een vrij uitgebreide tutorial waar je wel eventjes zoet mee bent. Het bestaat uit 4 delen, ieder opgedeeld 
in kleine onderwerpen. De eerste 2 delen gaan over Svelte, en de laatste 2 delen gaan over Sveltekit.

In de eerste week van sprint 13 ben ik gaan experimenteren met het opstarten van een svelte project. Hierbij heb ik 
in de Terminal van Visual Studio Code een aantal commands ingevoerd waarmee ik het skelet van het project kon opzetten. 
Zo installeer je sveltekit en de benodigde NPM-Packages. Als je dit succesvol hebt gedaan kun je je website bekijken door 
npm run dev uit te voeren.

Ook heb ik een nieuwe term geleerd, "The Zone of Proximal Development". Dit houd in dat je bepaalde leergebieden hebt met 
verschillende moeilijkheidsgraden. Zo kun je dingen leren die binnen handbereik liggen, maar niet erg uitdagend zijn. De 
volgende stap is dingen leren waar je zelf moeite voor moet doen, maar wat nog wel betaalbaar is. Dat is de Zone of Proximal 
Development waar je altijd in wil zitten. Daarna heb je nog het gebied die helemaal buiten je comfort valt wat ook veel te 
moeilijk is op dat moment om te leren, daar wil je nooit zitten.

Bij de Figma Workshop hebben we kennis gemaakt met verschillende shortcuts en Auto-Layout.
Ctrl + [ of ] om objecten naar een andere laag te plaatsen.
Ctrl + G om objecten te groeperen, of Ctrl + Shift + G om ze niet meer te groeperen.
Alt om gelijkmatig objecten uit te rekken.

Met Auto-Layout kun je components maken die je makkelijk kunt hergebruiken.

Desktop Artboard: 1440 x 1028
Mobile Artboard: 375 x 812

Creative Coding met CSS

Snap Scrolling in CSS moet een Progressive Enhancement zijn, geen Breaking Enhacement. Dit kun je doen door gebruik te maken van @supports. Zo herkent de browser of deze feature wordt ondersteund of niet.

De animation-timeline heet Happy Scroller. Deze is gebruikt in de demo van Justus. 

Welkom in de Learning Journal van Tygo Wolven.

Ons eerste huiswerk ging om het kennismaken met Directus en Sveltekit . Hierbij moesten we een tutorial 
volgen genaamd: "Getting started with Directus and Sveltekit". Tijdens het volgen van de stappen kwam ik 
vast te lopen op het deel waarop mijn data getoond zou moeten worden. Ik kreeg dat maar niet voor elkaar, 
mogelijk had dat te maken met dat de Directus omgeving niet goed is ingesteld.

Omdat ik hier vast liep, ben ik begonnen met een andere Tutorial over Sveltekit. Namelijk 'learn.svelte.dev', 
dit is een vrij uitgebreide tutorial waar je wel eventjes zoet mee bent. Het bestaat uit 4 delen, ieder opgedeeld 
in kleine onderwerpen. De eerste 2 delen gaan over Svelte, en de laatste 2 delen gaan over Sveltekit.

In de eerste week van sprint 13 ben ik gaan experimenteren met het opstarten van een svelte project. Hierbij heb ik 
in de Terminal van Visual Studio Code een aantal commands ingevoerd waarmee ik het skelet van het project kon opzetten. 
Zo installeer je sveltekit en de benodigde NPM-Packages. Als je dit succesvol hebt gedaan kun je je website bekijken door 
npm run dev uit te voeren.

Ook heb ik een nieuwe term geleerd, "The Zone of Proximal Development". Dit houd in dat je bepaalde leergebieden hebt met 
verschillende moeilijkheidsgraden. Zo kun je dingen leren die binnen handbereik liggen, maar niet erg uitdagend zijn. De 
volgende stap is dingen leren waar je zelf moeite voor moet doen, maar wat nog wel betaalbaar is. Dat is de Zone of Proximal 
Development waar je altijd in wil zitten. Daarna heb je nog het gebied die helemaal buiten je comfort valt wat ook veel te 
moeilijk is op dat moment om te leren, daar wil je nooit zitten.

Bij de Figma Workshop hebben we kennis gemaakt met verschillende shortcuts en Auto-Layout.
Ctrl + [ of ] om objecten naar een andere laag te plaatsen.
Ctrl + G om objecten te groeperen, of Ctrl + Shift + G om ze niet meer te groeperen.
Alt om gelijkmatig objecten uit te rekken.

Met Auto-Layout kun je components maken die je makkelijk kunt hergebruiken.

Desktop Artboard: 1440 x 1028
Mobile Artboard: 375 x 812

Creative Coding met CSS

Snap Scrolling in CSS moet een Progressive Enhancement zijn, geen Breaking Enhacement. Dit kun je doen door gebruik te maken van @supports. Zo herkent de browser of deze feature wordt ondersteund of niet.

De animation-timeline heet Happy Scroller. Deze is gebruikt in de demo van Justus. 

Creative Coding met Javascript

``<svelte:window on:mousemove={followPointer} />``

``import { fade } from 'svelte/transition'``

``transition:fade={{ duration: 250 }}``

## Epics, Stories & Userstories
Een epic is een handige manier om werk te organiseren en een hiërarchie te creeren. Het idee is om werk op te splitsen in 
opleverbare stukken, zodat grote projecten kunnen worden afgerond en klanten op regelmatige basis waarde krijgen voor hun geld.

Een paar voorbeelden van goede epics zijn:
- Een nieuwe E-commerce website lanceren voor de kruidvat.
- De website van het Ministerie van Volksgezondheid verbeteren.
- De nieuwe website lanceren voor de Hogeschool van Amsterdam.
- Argumented Reality toevoegen aan de website van de Intertoys.

Uit deze epics, oftewel hele grote taken, komen stories. Hierin wordt de epic opgedeeld in kleinere taken:
- Een winkelmandje toevoegen.
- Betalingsmogelijkheden toevoegen.
- Een klantenserviceportal toevoegen.

De stories zijn al kleinere taken dan een epic, maar nogsteeds moeilijk in te schatten qua tijd. Daarom splitsen
we deze stories nogmaals op in userstories zodat we een betere inschatting kunnen maken:

Bij het toevoegen van een winkelmandje:
- Als bezoeker, wil ik producten in mijn winkelmandje kunnen doen om overzicht te houden wat ik aanschaf.
- Als bezoeker, wil ik producten kunnen verwijderen uit mijn winkelmandje als ik iets gevonden heb wat beter past bij wat ik nodig heb.
- Als bezoeker, wil ik overzicht houden op het uit te geven bedrag zodat ik het gevoel heb in controle te zijn.

Kortom, een epic is een groots idee, deze verklein je in stories, en deze maak je inschatbaar in userstories.

## MoSCoW Methode
Must haves: Zijn taken die af moeten voor de deadline.

Should haves: Zijn taken die eigenlijk wel af moeten, maar niet noodzakelijk zijn.

Could haves: Zijn taken die af kunnen, mits we tijd over hebben.

Want to have but will not have this sprint: Zijn taken die leuk zijn voor een andere keer.