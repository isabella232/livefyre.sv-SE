---
description: Sidenotes-konfigurationsobjektet är ett JSON-objekt som används för att ange det innehåll som Livefyre-appen återger på sidan.
seo-description: Sidenotes-konfigurationsobjektet är ett JSON-objekt som används för att ange det innehåll som Livefyre-appen återger på sidan.
seo-title: Konfigurationsalternativ för sidenotes
solution: Experience Manager
title: Konfigurationsalternativ för sidenotes
uuid: 067e51e6-9720-4226-a805-c7a07c8cdaa0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Konfigurationsalternativ för sidenotes{#sidenotes-configuration-options}

Sidenotes-konfigurationsobjektet är ett JSON-objekt som används för att ange det innehåll som Livefyre-appen återger på sidan.

Objektet innehåller följande parametrar:

| Parameter | Typ | Beskrivning |
|--- |--- |--- |
| authDelegate | *obligatoriskt* objekt | Nytt eller gammalt initierat autentiseringsombud. |
| collectionMeta | *obligatoriskt* objekt | Mer information finns i collectionMeta-token. |
| customIcon | *valfri* sträng | Ställer in URL:en för en anpassad startikon. Standardvärdet är Livefyre bubble. |
| customStyles | *valfritt* objekt | Lägger till egna format för att ändra utseendet på sidomärken. Mer information finns i Anpassade format. |
| disableStream | *valfri* Boolean | Om true inaktiveras direktuppspelning i realtid i den här Sidenotes-instansen (inte i andra kommentarströmmar). Standardvärdet är false. |
| miljö | *valfri* sträng | Anger Livefyre UAT-miljön. Det enda möjliga värdet är `t402.livefyre.com`. För produktion måste den här parametern tas bort. |
| iconVisibility | *valfritt* objekt eller sträng | Definierar om ikonen Sidenotes ska vara synlig vid hovring eller statisk. Om det här är en sträng används den för båda versionerna av blockikonen (tom och har Sidenotes). Om det är ett objekt måste du ange varje typ: {empty: &quot;hover&quot;, antal: &quot;static&quot;}. Standardvärdet är statiskt. |
| inlineThreads | *valfri* boolesk | Om true infogas Sidenote-trådar direkt efter det block som de är kopplade till. Standardvärdet är false. |
| numSidenotesEl | *valfritt* objekt, sträng eller array | Anger vilket element widgeten för sidenotes-räkning ska dekorera. (Den här widgeten visar antalet sidobjekt på sidan och information om Sidenotes.) Om strängväljaren matchar mer än ett element väljs det första. (Använder specifikationen för CSS3 DOM-väljare.) |
| position | *valfri* sträng | Anger popup-fönstrets position när någon klickar på ett element som har Sidenotes aktiverat. Möjliga värden är&quot;smart&quot;,&quot;vänster&quot;,&quot;höger&quot; och&quot;nederst&quot;. Standard är&quot;smart&quot;, som justerar popup-fönstret till höger om sidan, såvida det inte finns tillräckligt med utrymme (i så fall flyttas det till under innehållet). |
| väljare | *obligatoriskt* objekt, sträng eller array | Anger de element som startikonerna ska visas på. (Använder specifikationen för CSS3 DOM-väljare.) Om det är ett objekt, innehåller ett inkluderingsavsnitt och ett&quot;utelämnar&quot;-avsnitt som kommer att tillämpa CSS-väljaren för alla matchande inkluderingar, samt ta bort alla element som matchar uteslutningarna. Om du anger en sträng kommer alla matchande element på sidan att tas med. Om det är en array, listas de element som ska inkluderas. |
| strängar | *valfritt* objekt | Lägger till anpassade textsträngar för att ändra språk och text i hela programmet. Mer information finns i Anpassade strängar. |
| threadContainerEl | *valfritt* objekt, sträng eller array | Anger ett element där tråden för sidobjekt visas. Med den här parametern kan du flytta tråden. Om strängväljaren matchar mer än ett element väljs det första. (Använder specifikationen för CSS3 DOM-väljare.) |

