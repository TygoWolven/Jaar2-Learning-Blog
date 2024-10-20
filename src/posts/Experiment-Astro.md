---
title: Tech Stack Astro
description: Hier documenteer ik wat ik heb geleerd over het framework Astro.
date: '2024-10-14'
categories:
  - Semester 3
  - Sprint 15
  - Experiment
published: true
status: false
value: 3
---

## Installatie van Astro
De installatie lijkt heel erg op dat van Sveltekit, dit komt mede doordat het allebei frameworks zijn. Om te laten zien hoe deze installatie gaat zal ik hem hier even nabootsen.
<br>

````ts
`Je begint met het aanmaken van je project.`
npm create astro@latest 
// Where should we create your new project?
`Geef hier de juiste route aan voor je project.`
// How would you like to start your new project?
// - Include sample files (recommended)
// - Use blog template
// - Empty
`Hier kan je zelf een keuze maken, maar omdat ik 
nieuw ben met Astro kies ik voor de sample files.`
// Do you plan to write Typescript?
// Yes / No 
`In mijn geval 'Nee', maar dit is ook eigen keuze.`
// Install dependencies?
// Yes / No
`Als je nu geen dependencies installeert, zul je 
later nog 'npm install' moeten uitvoeren.`
// Initialize new git repository? (optional)
// Yes / No
`Nu je alles hebt gedaan kun je 
je 'dev server' opstarten.`
npm run dev
````

Nu kun je aan de slag gaan met Astro! De basis van je project is geinstalleerd dus nu word alles experimenteren. Om het werken met Astro fijner te maken voor mezelf heb ik 2 `Extensions` geinstalleerd in Visual Studio Code. Allebei genaamd `Astro`.

## Basis Astro Layout
Zodra je Astro hebt geinstalleerd krijg je een aantal mappen en bestanden in je project. Om nieuwe pagina's aan te maken kun je `.astro` of `.md` bestanden toevoegen in de `/pages` map. Dit zorgt er dan voor dat ieder bestand een route is op basis van de bestandsnaam.
<br>

```text
/
├── public/
│   └── favicon.svg
├── src/
│   ├── components/
│   │   └── Card.astro
│   ├── layouts/
│   │   └── Layout.astro
│   └── pages/
│       └── index.astro
└── package.json
```

Astro is een heel flexibel framework. Dit is te zien aan het gebruik van compontents, je kunt namelijk components van andere frameworks gebruiken. Denk hierbij aan React, Vue, Svelte en Preact. Verder kun je alle statische elementen zoals afbeedlingen in de `/public` map stoppen.

## Astro Tutorial

https://www.youtube.com/watch?v=e-hTm5VmofI