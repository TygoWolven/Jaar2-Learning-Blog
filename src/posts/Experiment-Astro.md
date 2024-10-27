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

<script>
  import Astro from "$lib/assets/astro.png"
</script>

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
<br>
<img alt="Welcome to Astro" src={Astro} />

Nu kun je aan de slag gaan met Astro! De basis van je project is geinstalleerd dus nu word alles experimenteren. Om het werken met Astro fijner te maken voor mezelf heb ik een aantal `Extensions` geinstalleerd in Visual Studio Code. Eentje genaamd `Astro`, die zorgt ervoor dat Visual Studio Code je project herkent als Astro-project. Ook heb ik een extension genaamd `Astro Snippets` die je helpt om componenten sneller en gemakkelijker op te bouwen.

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

## Astro Beginner Tutorial

https://www.youtube.com/watch?v=acgIGT0J99U&t=786s

Omdat ik nieuw ben met Astro besloot ik een beginners tutorial te kijken waarin de basis functies van Astro worden uitgelegd. Zo zijn er een aantal dingen aan bod gekomen:
- De flexibiliteit van Astro
- Geen Javascript runtime voor verbeterde performance
- Het gebruik van `.md` bestanden binnen Astro
- Componenten met scoped CSS
- Astro Props

In vergelijking met sveltekit is het eerste wat me opviel dat er geen gebruik gemaakt word van `<script>` tags, maar van de 3 typescript `---` streepjes. De functie hiervan is hetzelfde maar je moet het wel even weten. Ook zijn in beide frameworks de `layout` file aanwezig, echter werken deze wel iets anders. In sveltekit bevat deze een slot die automatisch word gevuld door de juiste pagina, maar in Astro moet je hiervoor eerst de code nesten in een `<Layout>` tag. Alleen de content die binnen deze tag staat word gezien als het slot. Je zou dus kunnen zeggen dat Astro in dit geval meer werk kost.


## Astro Props
Astro ondersteunt props. Dit zijn variabelen die je in een component kunt gebruiken. Zo kun je bijvoorbeeld een enkel component aanmaken, maar hiervan wel op elke pagina de content aanpassen. Dit heeft dan weer te maken met de variabelen binnenin het component.
<br>

````ts
---
interface Props {
	title: string;
	body: string;
}

const {title, body } = Astro.props;
---

<li>
	<h2>
		{title}
	</h2>
	<p>
		{body}
	</p>
</li>

````
Nu je de Astro Props hebt opgezet binnen je component kun je in je werkbestand het component aanspreken en de variabelen aanpassen.
<br>

````
	<Card
		title="Sprint 13:"
		body="Your Tribe for Life"
	/>
````