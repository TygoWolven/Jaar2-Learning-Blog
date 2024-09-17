---
title: Sprint 13 - Your Tribe for Life
description: Hier heb ik gedocumenteerd wat ik heb geleerd in Sprint 13.
date: '2024-9-02'
categories:
  - Semester 3
  - Sprint 13
published: true
---

<script>
    import ProximalChart from "$lib/assets/image.png"
</script>

## Getting started with Directus and Sveltekit
In de eerste week van sprint 13 ben ik gaan experimenteren met het opstarten van een svelte project. Hierbij heb ik 
in de Terminal van Visual Studio Code een aantal commands ingevoerd waarmee ik het skelet van het project kon opzetten. 
<br>

````ts
npm create svelte@latest project-naam
// Kies voor een Skeleton Project
// Zet de Typescript functie uit
// Kies vervolgens features uit naar keuze (Optioneel)
cd project-naam
npm install
npm run dev
````
Om verder een beetje kennis te maken met Directus en Sveltekit ben ik een aantal tutorials gaan volgen.
Zo heb ik een tutorial gevolgd genaamd: "Getting started with Directus and Sveltekit". En een tutorial 
via de website genaamd: "learn.svelte.dev". Dit is een vrij uitgebreide tutorial waar je wel eventjes 
zoet mee bent. Het bestaat uit 4 delen, ieder opgedeeld in kleine onderwerpen. De eerste 2 delen gaan 
over Svelte, en de laatste 2 delen gaan over Sveltekit.

## The Zone of Proximal Development
Ik heb tijdens een les van Justus een nieuwe term geleerd, namelijk "The Zone of Proximal Development". Dit wil zeggen
dat er bepaalde leergebieden zijn met allemaal een eigen moeilijkheidsgraad. Over het algemeen bestaat dit begrip uit 3 zones.
Deze zones zal ik toelichten aan de hand van deze afbeelding:
<br>
<img alt="The Zone of Proximal Development" src={ProximalChart} />
<figcaption><i>The Zone of Proximal Development</i></figcaption>

Zo kun je ervoor kiezen om dingen te leren die binnen handbereik liggen, maar die zijn niet erg uitdagend. Je kunt er ook voor kiezen
om heel veel uitdaging op te zoeken, maar dat valt meestal buiten je comfort en gaat je dan ook niet lukken zonder hulp. Dan heb je nog
de zone waar je juist wel in wilt zitten, "The Zone of Proximal Development". Dit is de zone waarbij je wel wat uitdaging hebt om nieuwe 
dingen te leren, maar dat je er zelf wel uit kan komen.

## Figma 
Bij de Figma Workshop hebben we kennis gemaakt met verschillende shortcuts en de Auto-Layout functie om werken met Figma makkelijker te maken.
Ik zal hier een aantal shortcuts laten zien die ik heb geleerd:
- ``Ctrl + [ of ]`` om objecten naar een laag omhoog of omlaag te plaatsen. Als je hierbij ook nog ``Shift`` gebruikt verplaats je hem direct naar het einde.
- ``Ctrl + G`` om objecten te groeperen, of ``Ctrl + Shift + G`` om ze niet meer te groeperen.
- ``Alt`` om gelijkmatig objecten uit te rekken. In zowel hoogte als breedte.

Met de Auto-Layout functie kun je components maken die je makkelijk kunt hergebruiken in ieder bestand. Denk hierbij aan kaartjes, buttons etc. 

Als je gebruik gaat maken van Artboards kun je het beste vaste maten gebruiken voor zowel Desktop als voor mobile. Zo wordt aangeraden voor Desktop
een afmeting van ``1440 x 1028px`` te gebruiken, en voor mobile een afmeting van ``375 x 812px``.

## Creative Coding met CSS en JS
Binnen CSS en JS kun je leuke functies maken waarmee je je website speelser maakt. Zo heb je Snap Scrolling in CSS, waarmee je ervoor kan zorgen 
dat bijvoorbeeld lijsten altijd centraal uitlijnen. Echter moet dit een Progressive Enhancement zijn, en geen Breaking Enhancement. Voeg dit dus 
alleen toe als je @supports kan gebruiken. Zo herkent de browser of deze feature wordt ondersteund of niet.

Sveltekit probeert het makkelijker te maken om gebruik te maken van verschillende animation-timelines. Zo heb je een timeline genaamd: "Happy Scroller"
waarmee je dus vloeiende animaties kunt maken met Sveltekit. Deze is dan ook gebruikt in de live-demo van Justus. Om zo een timeline aan de praat te 
krijgen is er vaak Javascript nodig, zo heb je bijvoorbeeld zulke code nodig om bepaalde properties mee te geven met de animatie:

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