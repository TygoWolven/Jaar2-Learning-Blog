---
title: Don't Repeat Yourself
description: Hier documenteer ik wat ik heb geleerd in sprint 16.
date: '2024-11-11'
categories:
  - Semester 3
  - Sprint 16
published: true
status: false
value: 1
---

## Component Libraries
In deze sprint heb ik geleerd over component libraries. Dit zijn simpel gezegd mapjes met daarin componenten van je project. Hierin kun je verschillende structuren toepassen die makkelijk hergebruikt kunnen worden.

Een aantal voordelen van component libraries:
- eenvouding hergebruiken
- product krijgt consistente uitstraling
- efficientie en schaalbaarheid van het product
- snel nieuwe functies toevoegen, terwijl de algehele kwaliteit behouden blijft

Op npmjs kun je je eigen library uploaden, zodat anderen deze kunnen gebruiken. 

## Conventies binnen libraries
Naamgeving van componenten.
Naamgeving van variateies van componenten.
Naamgeving van properties binnen componenten.
Metanaamgeving: componenten, patronen etc. 
Indeling van de `$lib` folder.

**Metanaamgeving:**
Een hiërarchische benadering om het over bepaalde soorten componenten te hebben. 

Pages:
Volledige pagina's of schermen met een specifieke context bestaand uit sections. Bijvoorbeeld de homepage.

Sections:
Secties van een pagina bestaand uit componenten. Bijvoorbeeld een her-banner, een content-secie, een footer.

Components:
Herbruikbare componenten binnen de sections. Bijvoorbeeld knoppen, formulieren, kaarten.

Functional Layering

Inputs:
Gebruikersinvoer, knoppen, formulieren.
Display:
Weergeven van content, tabellen en grafieken.
Navigation:
Soorten van navigatie, menu's, breadcrumbs, skip-to-content.
Structural:
Layout-elementen die structuur bieden, grids, containers.

LEGO Structuur

Bricks:
Kleine niet herbruikbare stukjes, zoals een icoon of tekstblok.
Blocks: 
Herbruikbare basis componenten, een knop of een afbeelding.
Assemblages:
Gecombineerde componenten met een specifieke functie, formulier of een kaart.
Constructions:
Complexe pagina-secties of templates, dashboard.

Atomic Design:

Atoms:
Basis bouwblokken van je pagina, HTML Elementen.
Molecules:
Groep atomen bij elkaar.
Organism:
Groep moleculen bij elkaar.
Templates:
Groep organismes bij elkaar.
Pages:
Ingevuld template met inhoud.

Presenter Container:

Presentational components:
Een component die alleen de presentatie regelt. Bijvoorbeeld een afbeelding.
Container components:
Een component die de inhoud presenteert en de structuur regelt. 
Compositions:
Een groep presentational en container componentss die pagina-secties vormen.

## Deeltaak: The component building block

## Opdracht: Identificeer jouw componente

## RAPPE Websites
Responsive
Accesible
Performance
Progressive Enhanced

## Morphological Charts
Methode om onverwachte alternatieven te bedenken voor complexe designs. Dit doe je door een diagram te maken van alle mogelijke componenten die je nodig hebt.

Je hebt verschillende vragen waar je 3 oplossingen voor moet hebben, denk bijvoorbeeld aan problemen voor in een verhaal: COVID, Verliefdheid of een Botbreuk. Hierbij kun je alle vragen combineren waardoor je onverwachte alternatieven krijgt voor een verhaal.

AFBEELDING NAAR MORPHOLIOGISCAL CHART

## The New Responsive

Fluid grids, flexible images, and media queries are three technical ingredients for responsive web design, but it also requires a different way of thinking.
- Ethan Marcote

AFBEELDING VAN THE NEW RESPONSIVE

## Media query features
<strong tabindex="0">Level 3:<span>New Features since 21 May 2024</span></strong>

- width
- height
- grid
- scan
- device-height
- device-width
- resolution
- monochrome
- orientation
- aspect-ratio
- device-aspect-ratio
- color
- color-index

<strong tabindex="0">Level 4<span>New Features since 25 December 2021</span></strong>

- update
- overflow-block
- overflow-inline
- color-gamut
- pointer 
- hover
- any-pointer
- any-hover

<strong tabindex="0">Level 5<span>New Features since 18 December 2021</span></strong>

- environment-blending
- dynamic-range
- inverted-colors
- nav-controls
- scripting
- prefers-color-sheme
- forced-colors
- prefers-contrast
- prefers-reduced-transparency
- prefers-reduced-motion
- prefers-reduced-data

## Gestalt Principes
Gestalt principes zijn een set van regels die helpen bij het ontwerpen van een samenhangend design.

**De wet van nabijheid:** <br>
We groeperen figuren die dicht bij elkaar staan. Onze hersenen vinden dat deze bij elkaar horen.

**De wet van continuïteit:** <br>
We zien losse figuren die naast elkaar in een lijn of bocht lopen als geheel.

**De wet van gelijkheid:** <br>
Onze hersenen vinden dat figuren die er hetzelfde uitzien bij elkaar horen.

**De wet van geslotenheid:** <br>
Onze hersenen maken figuren af waarbij een stukje ontbreekt.

**De wet van overeenkomst:** <br>
Figuren die in dezelfde richting bewegen geven onze hersenen het gevoel dat ze bij elkaar horen. 

**De wet van voor- en achtergrond:** <br>
Onze hersenen onderscheiden vormen die op een achtergrond staan als losstaand figuur.

**De wet van symmetrie:** <br>
Symmetrische figuren geven onze hersenen het idee dat dingen geordend zijn. Het geeft rust.

### Wat is de Law of Proximity?
Objecten die dicht bij elkaar staan hebben de neiging om gegroepeerd te worden door ons brein. Wat zijn hier de voordelen van?
- Het helpt de gebruiker om informatie sneller en efficienter te gebruiken
- Het helpt een relatie te creeëren met objecten in de buurt
- De objecten hebben vaak dezelfde eigenschappen of functionaliteiten

## State Management
Toestand van je applicatie of component.

Shared persistent state:
Je wilt voorkomen dat aanpassingen in je website, voor iedereen aangepast worden.

Non shared persistent state:

Non shared non persistent state:

Non shared semi persistent state:

persistent is of de waarde wordt behouden of niet

Svelte persistent stores

Shared state:
alle gebruikers delen dezelfde states.






