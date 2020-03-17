---
description: När du implementerar Livefyre-appar beror implementeringsformatet på ditt användningssätt. På den här sidan förklaras funktionerna för de tre sätt som du kan skapa en app på.
seo-description: När du implementerar Livefyre-appar beror implementeringsformatet på ditt användningssätt. På den här sidan förklaras funktionerna för de tre sätt som du kan skapa en app på.
seo-title: CMS-appintegrering
solution: Experience Manager
title: CMS-appintegrering
uuid: 14fd7e36-0e50-4ae3-97f0-2de731c184f5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# CMS-appintegrering{#cms-app-integrations}

När du implementerar Livefyre-appar beror implementeringsformatet på ditt användningssätt. På den här sidan förklaras funktionerna för de tre sätt som du kan skapa en app på.

Livefyre-integrering är agnostiskt för alla CMS- och användarprofiler och Auth-plattformar. Implementera Livefyre på ett eller flera sätt, beroende på ditt användningsfall och dina krav.

Du kan använda traditionell integrering för att skapa anpassade AEM-komponenter.

## CMS App Integration Type - översikt

| Typ | Utvecklingskrav | Funktioner | Proffs | Begränsningar |
|--- |--- |--- |--- |--- |
| App Designer | Mycket låg | Skapa JS-inbäddningar i Studio för att lägga till på sidor utan att utvecklaren behöver ha tillgång till <br>begränsad formatering och konfigurationer </br>Använd skiftläge: Sidor för engångsbruk (händelsetäckning, kampanjer, hubbar) | Kan få igång en app på kort tid. <br>Konfigurationer kan göras av icke-tekniska medlemmar. <br>Smidiga ändringar av konfigurationer | Måste skapa en app med Livefyre Studio först <br>Inte automatiserad |
| Livefyre.js | Medel | Integrera appar i JavaScript på sidorna <br>Använd skiftläge: Återanvändbara mallar (redaktionellt innehåll, produktrecensioner) | Använd hela sviten med appanpassningar och konfigurationer <br>Automatiserar processen för att dynamiskt instansiera appar inifrån ditt CMS-system till dina sidor | Behöver en utvecklare i framkanten. |
| SDK API:er | Avancerat | Hämta ditt innehåll från Livefyre och använd det för anpassade program <br>Anpassa gränssnittet utöver det som stöds, <br>Använd exempel: Data-/analysintegrationer och anpassade front end-appar | Full kraft över appens utseende och känsla | Kräver utveckling direkt. <br>Högre utvecklingsinsatser att implementera. |
