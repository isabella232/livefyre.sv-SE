---
description: Sidenotes-konfigurationsobjektet är ett JSON-objekt som används för att ange det innehåll som Livefyre-appen återger på sidan.
title: Konfigurationsalternativ för sidenotes
exl-id: efebf9e5-6623-4953-a8f6-c58495304ac1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Konfigurationsalternativ för sidenotes{#sidenotes-configuration-options}

Sidenotes-konfigurationsobjektet är ett JSON-objekt som används för att ange det innehåll som Livefyre-appen återger på sidan.

Objektet innehåller följande parametrar:

| Parameter | Typ | Beskrivning |
|--- |--- |--- |
| authDelegate | ** requiredObject | Nytt eller gammalt initierat autentiseringsombud. |
| collectionMeta | ** requiredObject | Mer information finns i collectionMeta-token. |
| customIcon | ** valfri sträng | Ställer in URL:en för en anpassad startikon. Standardvärdet är Livefyre bubble. |
| customStyles | ** alternativt objekt | Lägger till egna format för att ändra utseendet på sidomärken. Mer information finns i Anpassade format. |
| disableStream | ** optionalBoolean | Om true inaktiveras direktuppspelning i realtid i den här Sidenotes-instansen (inte i andra kommentarströmmar). Standardvärdet är false. |
| miljö | ** valfri sträng | Anger Livefyre UAT-miljön. Det enda möjliga värdet är `t402.livefyre.com`. För produktion måste den här parametern tas bort. |
| iconVisibility | *alternativt* objekt eller sträng | Definierar om ikonen Sidenotes ska vara synlig vid hovring eller statisk. Om det här är en sträng används den för båda versionerna av blockikonen (tom och har Sidenotes). Om det är ett objekt måste du ange varje typ: {empty: &quot;hover&quot;, antal: &quot;static&quot;}. Standardvärdet är statiskt. |
| inlineThreads | ** valfri boolesk | Om true infogas Sidenote-trådar direkt efter det block som de är kopplade till. Standardvärdet är false. |
| numSidenotesEl | *alternativt* objekt, sträng eller array | Anger vilket element widgeten för sidenotes-räkning ska dekorera. (Den här widgeten visar antalet sidobjekt på sidan och information om Sidenotes.) Om strängväljaren matchar mer än ett element väljs det första. (Använder specifikationen för CSS3 DOM-väljare.) |
| position | ** valfri sträng | Anger popup-fönstrets position när någon klickar på ett element som har Sidenotes aktiverat. Möjliga värden är&quot;smart&quot;,&quot;vänster&quot;,&quot;höger&quot; och&quot;nederst&quot;. Standard är&quot;smart&quot;, som justerar popup-fönstret till höger om sidan, såvida det inte finns tillräckligt med utrymme (i så fall flyttas det till under innehållet). |
| väljare | *requiredObject,* string, or array | Anger de element som startikonerna ska visas på. (Använder specifikationen för CSS3 DOM-väljare.) Om det är ett objekt, innehåller ett inkluderingsavsnitt och ett&quot;utelämnar&quot;-avsnitt som kommer att tillämpa CSS-väljaren för alla matchande inkluderingar, samt ta bort alla element som matchar uteslutningarna. Om du anger en sträng kommer alla matchande element på sidan att tas med. Om det är en array, listas de element som ska inkluderas. |
| strängar | ** alternativt objekt | Lägger till anpassade textsträngar för att ändra språk och text i hela programmet. Mer information finns i Anpassade strängar. |
| threadContainerEl | *alternativt* objekt, sträng eller array | Anger ett element där tråden för sidobjekt visas. Med den här parametern kan du flytta tråden. Om strängväljaren matchar mer än ett element väljs det första. (Använder specifikationen för CSS3 DOM-väljare.) |
