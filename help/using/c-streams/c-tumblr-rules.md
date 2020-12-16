---
description: Du kan skapa strömregler som hämtar innehåll från Tumblr.
seo-description: Du kan skapa strömregler som hämtar innehåll från Tumblr.
seo-title: Tumblr-regler
solution: Experience Manager
title: Tumblr-regler
uuid: fe9601ab-aa5e-48c6-a5bf-5543c179cb90
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---


# Tumblr-regler{#tumblr-rules}

Du kan skapa strömregler som hämtar innehåll från Tumblr.

Skapa Tumblr-regler baserat på en Tumblr-blogg och filtreras efter tagg. Tumblr-strömmar uppdateras var femte minut och söker efter innehåll som inte redan finns i Livefyre från de första 20 objekten i feeden. Livefyre ignorerar allt som ligger utanför de första 20 objekten i feeden.

Om du vill skapa Tumblr Rules för att hämta innehåll från Tumblr till din app eller mapp kan du filtrera efter:

* **[!UICONTROL Blog]**

   * Ange **[!UICONTROL Blog Name]** för Tumblr-bloggen. Ange URL:en (*personal.tumblr.com*) eller namnet på bloggen (*personal*).

   * Inkludera upp till en **[!UICONTROL Tag]** för att filtrera resultat efter inlägg med en viss tagg.

* **[!UICONTROL Include recent items.]** Om detta är inställt på:

   * **[!UICONTROL Enabled]** lägger Livefyre till de första 20 innehållsobjekten i din feed i strömmen, oavsett publiceringsdatum.
   * **[!UICONTROL Disabled]** lägger Livefyre till de första 20 innehållsobjekten i din feed i strömmen med ett publiceringsdatum som är samma som datumet då ströminstansen skapades eller senare.

Ytterligare alternativ för strömningsregler för alla strömregler finns i [Alternativ för strömningsregel för alla strömregler](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
