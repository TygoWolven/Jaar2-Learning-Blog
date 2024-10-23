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
</script>

## Testresultaten
Om te kijken of mijn Learning Blog voldoet aan verschillende eisen, heb ik een hele boel tests uitgevoerd. De resultaten en documentatie hiervan zijn hier onder te vinden. 

### Performance Test
<img alt="Performance Score 100%" src={Performance100} />

De performance test is uitgevoerd met behulp van de Lighthouse Tool. Als resultaat kwam hier 100% uit, wat betekent dat mijn website hele goede performance heeft. Echter was er nog wel een klein verbeteringspunt gevonden, namelijk dat mijn afbeelding (logo) geen vaste width en height heeft meegekregen. Dit kan ervoor zorgen dat er Layout Shifts plaatsvinden in de pagina. De error die ik kreeg was als volgt: *'Image elements do not have explicit `width` and `height`'*.

### Accessibility Test
<div class="flex">
  <img alt="Accessibility Score 95%" src={Accessibility95} />
  <img alt="Accessibility Score 100%" src={Accessibility100} />
</div>

De accessibility test is uitgevoerd met behulp van de Lighthouse Tool. Als resultaat kwam hier 95% uit, wat betekent dat mijn website goed toegankelijk is voor alle gebruikers, maar nog niet perfect. Dit had te maken met dat het contrast op één van mijn knoppen niet goed genoeg was, waardoor deze voor slechtzienden moeilijk te onderscheiden is met de achtergrond van de pagina. De error die ik kreeg was: *'Background and foreground colors do not have a sufficient contrast ratio.'*.

Dit heb ik opgelost door de kleuren op de knop te veranderen, waardoor er een groter contrast is ontstaan met de achtergrond. Nu komt er uit het testresultaat 100% voor toegankelijkheid.

### Keyboard Tab Test
Bij deze test heb ik gekeken of ik kan navigeren door de website met alleen mijn `Tab` toets. Als conclusie kan ik hieruit trekken dat dit prima mogelijk is, op de homepagina volgt de focus netjes alle links, waardoor je gemakkelijk kunt navigeren naar bijvoorbeeld alle blog artikelen. Op de pagina van een artikel zelf krijg je ook eerst alle links te zien, waaronder de terug knop die heel belangerijk is.

### Kleurcontrast Test

### WCAG Test

### HTML Validator Test

### Browser Test

<style> 
  .flex {
    display: flex;
    gap: 1em;
  }
</style>