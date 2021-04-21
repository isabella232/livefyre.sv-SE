---
description: När du implementerar Livefyre-appar beror implementeringsformatet på ditt användningssätt. På den här sidan förklaras funktionerna för de tre sätt som du kan skapa en app på.
title: CMS-appintegrering
exl-id: 7590e247-87cc-470e-bab6-e61a19221dbd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# CMS-appintegreringar{#cms-app-integrations}

När du implementerar Livefyre-appar beror implementeringsformatet på ditt användningssätt. På den här sidan förklaras funktionerna för de tre sätt som du kan skapa en app på.

Livefyre-integrering är agnostiskt för alla CMS- och användarprofiler och Auth-plattformar. Implementera Livefyre på ett eller flera sätt, beroende på ditt användningsfall och dina krav.

Du kan använda traditionell integrering för att skapa anpassade AEM.

## CMS App Integration Type - översikt

| Typ | Utvecklingskrav | Funktioner | Proffs | Begränsningar |
|--- |--- |--- |--- |--- |
| App Designer | Mycket låg | Skapa JS-inbäddningar i Studio för att lägga till i sidor utan utvecklare <br>Begränsad formatering och konfigurationer </br>Användningsexempel: Sidor för engångsbruk (händelsetäckning, kampanjer, hubbar) | Kan få igång en app på kort tid. <br>Konfigurationer kan göras av icke-tekniska medlemmar. <br>Smidiga ändringar av konfigurationer | Måste skapa en app med Livefyre Studio först <br>Inte automatiserad |
| Livefyre.js | Medel | Integrera appar i JavaScript på sidorna <br>Använd skiftläge: Återanvändbara mallar (redaktionellt innehåll, produktrecensioner) | Använd hela sviten med appanpassningar och konfigurationer <br>Automatiserar processen för att dynamiskt instansiera appar inifrån ditt CMS-system till dina sidor | Behöver en utvecklare i framkanten. |
| SDK API:er | Avancerat | Hämta ditt innehåll från Livefyre och använd det för anpassade program <br>Anpassa gränssnittet utöver det som stöds i <br>Användningsexempel: Data-/analysintegrationer och anpassade front end-appar | Full kraft över appens utseende och känsla | Kräver utveckling direkt. <br>Högre utvecklingsinsatser att implementera. |
