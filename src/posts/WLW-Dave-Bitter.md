---
title: Dave Bitter
description: Hier documenteer ik wat ik heb geleerd in de We Love Web van Dave Bitter.
date: '2025-01-17'
categories:
  - Semester 3
  - Sprint 18
  - We Love Web
published: true
status: true
value: 2
---

## The Rise of AI-powered Voice Interfaces
Dave is al 7 jaar aan het wachten op een opdracht waarbij hij Voice UI kan gebruiken op het web. Met de Speach Recognition API heeft hij een website gemaakt die een transcript maakt van wat jij verteld. 

Vanaf 1950 werden de eerste pogingen gedaan om voice recognition werkend te krijgen. Over de jaren heen kwamen er steeds meer vorderingen, van het eerste programma die dit werkend kreeg, tot smart voice assistants op de dag van vandaag zoals Google Home of Alexa.

## Chatting with AI is cool, but we can make it awesome!
Dave is van mening dat we AI moeten gebruiken om de menselijke interactie te verbeteren, om een natuurlijker gesprek te voeren.

- SpeechRecognition Web API
- SpeechSynthesis Web API _(Dave maakt gebruik van ElevenLabs)_

Het nadeel aan ElevenLabs is dat hij eerst een fetch moet doen om een leuke stem te krijgen, dus de reactietijd werd langer. Dit heeft er voor gezorgd dat het gesprek minder natuurlijk voelde, omdat de browser tijd nodig had om het antwoord klaar te zetten. 

Om dit op te lossen heeft hij de fetch verandert. Eerst werd het hele antwoord in 1 request verstuurd, maar nu per zinnetje. Dit heeft er voor gezorgd dat de AI veel sneller een antwoord kon geven, en zo doorlopend nieuwe zinnen binnen kreeg om te vertellen.