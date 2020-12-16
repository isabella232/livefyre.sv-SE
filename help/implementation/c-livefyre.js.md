---
description: Huvudbiblioteket Livefyre använde för att driva Livefyre på er webbplats.
seo-description: Huvudbiblioteket Livefyre använde för att driva Livefyre på er webbplats.
seo-title: Livefyre.js
solution: Experience Manager
title: Livefyre.js
uuid: 7b3eca57-d5e8-416d-badf-a9c51d10dadd
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---


# Livefyre.js {#livefyre-js}

Huvudbiblioteket Livefyre använde för att driva Livefyre på er webbplats.

`Livefyre.js` är huvudbiblioteket som du kan installera på alla Livefyre-aktiverade webbsidor. Det definierar det globala `window.Livefyre`-objektet och en offentlig metod, `Livefyre.require`, som kan användas för att läsa in andra LiveFyre JavaScript-bibliotek som kan användas med [Bädda in Livefyre-appar](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md), [Integrera din autentiseringsleverantör med Livefyre](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) med mera.

## Lägg till på din webbplats {#section_cst_twg_xz}

Lägg till följande `<script>`-tagg på webbsidan eller webbplatsmallen. Om det är möjligt lägger du till det i `<head>`-avsnittet i HTML-dokumentet så att det läses in snabbt.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

>[!NOTE]
>
>Skriptet bäddar in en mycket liten (1 kB) fil som kallas Livefyre.js-scout som sedan läser in den senaste versionen av Livefyre.js över det protokoll som webbsidan har öppnats med (HTTP eller HTTPS).

## Livefyre.require {#section_ipq_hwg_xz}

`Livefyre.require` är en anpassad JavaScript-modulinläsare som  [curl.](https://github.com/cujojs/curl) jsor  [RequireJS](https://requirejs.org/). Den kan användas för att läsa in de flesta paket som publicerats av Livefyre och utgör en bekväm och intuitiv integrationsväg.

Paket som är tillgängliga via `Livefyre.require` versionshanteras med [semantisk version](https://semver.org/). Paket kan behövas i en viss version eller i en rad olika versioner så att webbsidan automatiskt kan dra nytta av nya felkorrigeringsfunktioner. Detta ger flexibilitet när du ska integrera Livefyre på din webbplats. Det finns tre nivåer av versionskoppling som du kan använda med `Livefyre.require`.

* **package-name#1:** Fäst vid huvudversion v1. Du får alla nya uppdateringar som har ett bakåtkompatibelt API. Fäst i en större version för att få buggfixar och smärre funktionsförbättringar för den versionen.
* **package-name#1.1:** Fäst mot delversion v1.1. Du får alla felkorrigeringar till den här mindre versionen. Livefyre Engineering kommer alltid att ge ojämnheter till en mindre version av ett paket om dess standardbeteende eller funktionella omfång ändras på ett sätt som kan orsaka nytt, oväntat beteende på din webbsida. Fäst en delversion om du vill få automatiska felkorrigeringar, men inga ytterligare funktioner eller ändringar av standardbeteendet.
* **package-name#1.1.1:** Fäst mot patch version 1.1.1. Beteendet för den här inbäddningen ändras aldrig, även om det finns felkorrigeringar. Fäst en patch-version om du har omfattande CSS-anpassningar för platsen som är beroende av ett pakets kodstruktur som kan ändras, eller om du har andra skäl att föredra att den Livefyre-version som du kör inte ändras på något sätt.

Ett exempel på integrering med `Livefyre.require` kan se ut så här:

```
<!-- First add Livefyre.js to the page --> 
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
  
<!-- Then load up all the desired Livefyre packages and Do Stuff in the callback --> 
<script> 
Livefyre.require([ 
    'lfawesome#1', 
    'lfsuperawesome#2.1.2' 
], function (LFAwesome, LFSuperAwesome) { 
    var greatness = new LFAwesome(); 
    // etc.. 
}); 
</script>
```

## Tillgängliga paket {#section_ygd_dwg_xz}

Undrar du vilka Livefyre JavaScript-paket som är tillgängliga via `Livefyre.require`? Du hittar alltid en uppdaterad lista över paket som stöds och deras senaste versioner här: [packages.html](https://cdn.livefyre.com/packages.html).

## Testar förhandsversioner av paket {#section_pgm_dpg_xz}

Ibland kanske du vill testa en kommande version av ett Livefyre-paket för att se till att det fungerar på din webbplats eller för att godkänna en funktion som utvecklas på din begäran. Utöver att inkludera ett semantiskt versionsområde kan du även ange en UAT-miljö för prerelease.

Följande kräver till exempel UAT-versionen av `fyre.conv`, programmen Comments, Live Blog och Chat.

```
Livefyre.require(['fyre.conv#uat'], callback); 
```
