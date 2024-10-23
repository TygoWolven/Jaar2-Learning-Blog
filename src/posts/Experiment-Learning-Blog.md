---
title: Learning Blog
description: Hier documenteer ik hoe ik deze blog tot dit resultaat heb weten te krijgen.
date: '2024-9-02'
categories:
  - Semester 3
  - Sprint 15
  - Experiment
published: true
status: false
value: 3
---

<script>
  import Performance100 from "$lib/assets/performance-100.png"
  import Accessibility95 from "$lib/assets/accessibility-95.png"
  import Accessibility100 from "$lib/assets/accessibility-100.png"
  import CCA1 from "$lib/assets/CCA-tekst-achtergrond.png"
  import CCA2 from "$lib/assets/CCA-grote-tekst-achtergrond.png"
  import Browsers from "$lib/assets/browsers.png"
  import W3C from "$lib/assets/w3c.png"
</script>

## Testresultaten
Om te kijken of mijn Learning Blog voldoet aan verschillende eisen, heb ik een hele boel tests uitgevoerd. De resultaten en documentatie hiervan zijn hier onder te vinden. 

### Performance Test
<img alt="Performance Score 100%" src={Performance100} />

De performance test is uitgevoerd met behulp van de Lighthouse Tool. Als resultaat kwam hier 100% uit, wat betekent dat mijn website hele goede performance heeft en dus zorgt voor een fijne *User Experience*. Echter was er nog wel een klein verbeteringspunt gevonden, namelijk dat mijn afbeelding (logo) geen vaste width en height heeft meegekregen. Dit kan ervoor zorgen dat er Layout Shifts plaatsvinden in de pagina. De error die ik kreeg was als volgt: *'Image elements do not have explicit `width` and `height`'*.

### Accessibility Test
<div class="flex">
  <img alt="Accessibility Score 95%" src={Accessibility95} />
  <img alt="Accessibility Score 100%" src={Accessibility100} />
</div>

De accessibility test is uitgevoerd met behulp van de Lighthouse Tool. Als resultaat kwam hier 95% uit, wat betekent dat mijn website goed *toegankelijk* is voor alle gebruikers, maar nog niet perfect. Dit had te maken met dat het contrast op één van mijn knoppen niet goed genoeg was, waardoor deze voor slechtzienden moeilijk te onderscheiden is met de achtergrond van de pagina. De error die ik kreeg was: *'Background and foreground colors do not have a sufficient contrast ratio.'*.

Dit heb ik opgelost door de kleuren op de knop te veranderen, waardoor er een groter contrast is ontstaan met de achtergrond. Nu komt er uit het testresultaat 100% voor toegankelijkheid.

### Keyboard Tab Test
Bij deze test heb ik gekeken of ik kan navigeren door de website met alleen mijn `Tab` toets. Als conclusie kan ik hieruit trekken dat dit prima mogelijk is, op de homepagina volgt de focus netjes alle links, waardoor je gemakkelijk kunt navigeren naar bijvoorbeeld alle blog artikelen. Op de detailpagina van een artikel krijg je ook eerst alle links te zien, waaronder de terug knop die heel belangerijk is.

### Kleurcontrast Test
Voor deze test ben ik gaan kijken naar het contrast op mijn website. Hierbij specifiek naar het contrast bij de teksten op mijn website, aangezien dat de belangerijke content is voor alle gebruikers. Ik heb gekeken naar mijn witte tekst die ik gebruik voor de informatie, en naar de groene tekst die ik gebruik voor mijn titels.

<br>
<div class="flex cca">
  <img alt="Colour Contrast Analyser Testresult" src={CCA1} />
  <img alt="Colour Contrast Analyser Testresult" src={CCA2} />
</div>

Als resultaat is hier gekomen dat mijn witte tekst (AAA) scoort. Dit betekent dat het perfect toegankelijk is om te gebruiken. Echter hebben mijn groene titels minder goed gescoord, zo zijn deze niet geslaagd als normale tekst, en bij (AAA) zelfs niet als grote tekst. Nu is dit probleem niet heel groot omdat deze titels alleen maar in het groot worden gebruikt, dus dan zouden ze alsnog (AA) scoren, oftewel alsnog goed toegankelijk.

### HTML Validator Test
Aan de hand van een W3C validatie, https://validator.w3.org/, heb ik mijn website getest op semantische code. Hieruit kwamen geen ernstige errors, wat betekent dat mijn website prima op orde is qua code.

<br>
<img alt="HTML Validation Test" src={W3C} />

### Browser Test
Ik heb mijn live-website op meerdere browsers getest. Denk hierbij aan Google Chrome, Microsoft Edge, Firefox, Opera en Brave.

<br>
<img alt="Browser Logo's" src={Browsers} />

Bij ieder van deze browsers leek mijn website correct te functioneren, zonder problemen. Er was af een toe wel een verschil in reactietijd, zo was Chrome bijvoorbeeld sneller met het laden van een artikel dan Microsoft Edge of Firefox.

<style> 
  .flex {
    display: flex;
    gap: 1em;
  }

  .cca > img {
    width: 50%;
  }
</style>