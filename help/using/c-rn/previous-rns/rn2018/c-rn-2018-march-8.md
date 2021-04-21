---
description: Versionsinformation för utgåva 8 mars 2018.
title: 8 mars 2018
exl-id: 46d4a425-17e0-48a2-a596-5cc7163f9edd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---

# 8 mars 2018{#march}

Versionsinformation för utgåva 8 mars 2018.

## Nya funktioner {#section_syx_mdt_wcb}

Följande funktioner är nya i produktionsversionen av den här versionen:

* **Tar bort program. **Möjligheten att ta bort appar i Studio har lagts till så att användarna bättre kan hantera applistan. Om du tar bort en app tas den bort från tabellen, men appen tas inte bort från webbplatsen. Appen fortsätter att ta emot innehåll från en ström om den är konfigurerad att göra det.

## Problem {#section_ehw_ndt_wcb}

Problemen i följande tabeller löstes i den här versionen.

## Produktionsrelease

| **Ärendetyp** | **Komponent** | **Versionsinformation** |
|---|---|---|
| Fel | Omröstningar | Ändrade omröstningar så att enbart HTTPS används. Tidigare tilläts omröstningar fortfarande användas med HTTP. |
| Fel | Studio | Korrigerade ett problem som gjorde att det modala fönstret som visar meddelanden när du loggar in i Studio skulle visas för stort på skärmar med låg upplösning. |

## UAT-release

| Ärendetyp | Komponent | Versionsinformation |
|--- |--- |--- |
| Förbättring | Bildband | Följande tillgänglighetsfunktioner för bildbandet har uppdaterats: <br><ul><li>Vänster-/högerpilar korrigerade från &lt;div> till &lt;button> </li><li>Elementet för förhandsgranskning har ändrats från den mindre beskrivande ARIA-etiketten &quot;Öppna bifogat foto&quot; till en etikett som läser namnet på plattformen och posttexten.</li></ul> |
| Fel | Media Wall | Korrigerade ett problem i Media Wall där taggar inte kunde klickas när ett Instagram-inlägg lades till från en strömregel. |
| Förbättring | Media Wall | Förbättrad tillgänglighet för medievägg på följande sätt: <br><ul><li>När du öppnar och stänger modulerna via tangentbordskommandon flyttas fokus inte längre tillbaka till sidans övre del. Fokusera istället på det element som senast fokuserades före modala popup-fönster.</li><li>Knappen Läs in mer kan tabbas till och aktiveras med tangenten Enter.</li></ul> |
| Fel | Rights Management | Ett fel har korrigerats där du inte kunde se en spärrad behörighetsbegäran efter att rättigheter för en Instagram-resurs beviljats. |
