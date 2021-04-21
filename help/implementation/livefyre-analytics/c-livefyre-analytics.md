---
title: Använd Livefyre med andra analysverktyg
description: Använd Livefyre med andra analysverktyg
exl-id: da29e281-5095-4e99-a248-19390f2059a2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# Använd Livefyre med andra analysverktyg{#use-livefyre-with-other-analytics-tool}

Ni kan använda analysverktyg för att samla in data om användarinteraktioner med Livefyre-appar. Du kan använda Adobe Analytics eller något annat verktyg.

Om du vill använda Livefyre med ett valfritt verktyg (inte Adobe Analytics) följer du anvisningarna på den här sidan.

## Steg 1: Konfigurera händelsehanterare {#section_ngm_gzl_pdb}

Konfigurera en händelsehanterare på sidor där du använder Livefyre-appar. På så sätt kan ni samla in data från apparna på den sidan som ni kan använda för analyser.

Lägg till Livefyre.js på en sida för att konfigurera händelsehanteraren. Livefyre.js läses in asynkront. För att minska filstorleken och förbättra inläsningsprestanda är analysen inte tillgänglig direkt. Du måste avfråga analysobjektet tills data är tillgängliga. Placera skriptet var som helst på sidan eller paketera det i dina egna kompilerade skript.

```
/** 
 * Handler for Livefyre analytics batch events. 
 * @param {Array.<string>} events Array of events that have been fired since 
 * the last batch send. 
 */ 
function analyticsHandler(events) { 
  // Send to analytics 
  console.log(events); 
} 
 
var attempts = 0; 
 
function pollForAnalytics() { 
  if (Livefyre && Livefyre.analytics) { 
    Livefyre.analytics.addHandler(analyticsHandler); 
    return; 
  } 
  if (attempts === 10) { 
    return; 
  } 
  attempts++; 
  setTimeout(pollForAnalytics, 500); 
} 
 
pollForAnalytics(); 
```

## Steg 2: Implementeringshanterarfunktion

När Livefyre.analytics-funktionen är tillgänglig på sidan implementerar du funktionen analyticsHandler för att skicka de mottagna händelserna till den analysöppnare som du väljer.

1. Analyshanteraren tar emot en array med händelser som måste itereras igenom och skickas individuellt eller som en grupp, om din leverantör stöder det.
1. Mappa händelsedata som tas emot av hanteraren till ett format som analysleverantören kräver.
1. Skicka data till analysleverantören.
