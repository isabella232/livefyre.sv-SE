---
description: Du kan skapa direktuppspelningsregler som hämtar innehåll från RSS-flöden.
title: RSS-regler
exl-id: bfb3bbad-ab26-451e-b540-d6c41f54dc31
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# RSS-regler{#rss-rules}

Du kan skapa direktuppspelningsregler som hämtar innehåll från RSS-flöden.

RSS-strömmar uppdateras var femte minut och söker efter innehåll som inte redan finns i Livefyre från de första 50 objekten i flödet. Livefyre ignorerar allt som ligger utanför de första 50 objekten i feeden.

Om du vill skapa RSS-regler för att hämta innehåll från RSS-flöden till din app eller mapp kan du filtrera efter:

* **[!UICONTROL URL]** RSS-flöde.
* **[!UICONTROL Include recent items.]** Om detta är inställt på:

   * **[!UICONTROL Enabled]** lägger Livefyre till de första 50 innehållsobjekten i din feed i strömmen, oavsett publiceringsdatum.
   * **[!UICONTROL Disabled]** lägger Livefyre till de första 50 innehållsobjekten i din feed i strömmen med ett publiceringsdatum som är samma som datumet då ströminstansen skapades eller senare.

* **[!UICONTROL Extract post information from item link (when disabled, post information is extracted from XML).]** Hämta information från objektlänken eller från XML-filen.

**RSS-regler**

Livefyre tolkar RSS-flöden baserat på följande RSS-specifikationer:

* [RSS 2.0](https://en.wikipedia.org/wiki/RSS)
* [Media RSS](https://en.wikipedia.org/wiki/Media_RSS)
* [Atom feed](https://validator.w3.org/feed/docs/atom.html)

Livefyre läser inte feeds som inte följer dessa specifikationer, och deras innehåll hämtas inte till strömmen. Använd tjänsten WC3 Feed Validation för att kontrollera syntaxen för din RSS-feed och kontrollera att den är giltig.

Ytterligare alternativ för strömningsregler för alla strömregler finns i [Alternativ för strömningsregel för alla strömregler](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
