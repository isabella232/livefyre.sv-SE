---
description: Dessa alternativ gäller för alla flödesregler från alla sociala nätverk eller bokföringsmetoder.
title: Direktuppspelningsregelalternativ för alla flödesregler
exl-id: eff1a3cb-395f-4eb1-be93-f0f09bba95e2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Direktuppspelningsregelalternativ för alla direktuppspelningsregler{#stream-rule-options-for-all-stream-rules}

Dessa alternativ gäller för alla flödesregler från alla sociala nätverk eller bokföringsmetoder.

Sökfunktioner för text och nyckelordsfält:

* När du anger nyckelord används den booleska operatorn **OR** automatiskt i Livefyre för enskilda ord. Om du till exempel vill söka efter inlägg med antingen ordet *tårta* eller *recept* anger du *tårta* och sedan *recept* i fältet **[!UICONTROL keyword]**.

* Du kan söka efter exakta fraser genom att omge den exakta frastexten inom citattecken. Om du till exempel vill söka efter den exakta frasen *recept* anger du *&quot;recept på tårta&quot;* i fältet **[!UICONTROL keyword]**.

* Du kan kombinera sökningar med boolesk och exakt fras i en strömregel. Du kan till exempel söka efter *tårta*, *recept* och *&quot;tårtrecept&quot;* genom att ange varje fras i taget.

**[!UICONTROL Additional Filters]**:

* **[!UICONTROL Media]**. Välj något av följande:

   * **[!UICONTROL All Content.]** Tillåt allt innehåll.
   * **[!UICONTROL Media Required.]** Tillåt endast innehåll med bilder och videoklipp. (För Instagram- och Facebook-innehåll kan du endast ange **[!UICONTROL Photos]** eller **[!UICONTROL Videos]**).

* **[!UICONTROL Language]**. Välj vilket språk du vill söka i. Engelska är standardspråket.
* **[!UICONTROL Smart Tags]**. Välj de taggar som ska användas för att identifiera innehåll. Livefyre använder dataveteknik för att identifiera foton och videoklipp med specifika smarta taggar för att göra sökningen mer exakt. Använd modifieraren **[!UICONTROL ANY]** för att filtrera innehåll i strömmen med valfri tagg eller modifieraren **[!UICONTROL ALL]** för att filtrera innehåll i strömmen som använder alla taggar. Använd fältet **[!UICONTROL Image contains none of these smart tags]** för att ange taggar för foton som innehåller innehåll som du inte vill ha i strömmen. Det här alternativet fungerar inte för textinnehåll.

* **[!UICONTROL Products]**. Lägg till produkttaggar för att matcha strömningsregeln med produkter från din produktkatalog.
* **[!UICONTROL Premoderate]**. Välj något av följande:

   * **[!UICONTROL On]**. Förmåtta allt inkommande regelinnehåll. Du kan visa förmodererat innehåll från avsnittet Streams i ModQ. **[!UICONTROL On]** åsidosätter inställningarna i Appinställningar.
   * **[!UICONTROL Off]**. Förmåtta inte innehåll för inkommande regler. **[!UICONTROL Off]** åsidosätter inställningarna i Appinställningar.
   * **[!UICONTROL Inherited (Off)]**. Använd de förmåttliga inställningarna från platsen (under **[!UICONTROL Site Settings]**).

* **[!UICONTROL SAFE Rules]**. Välj något av följande:
   * **[!UICONTROL Apply SAFE Rules]**. Använd alla SAFE-regler för den här strömmen.
   * **[!UICONTROL Apply SAFE Rules for:]** Välj ett eller flera alternativ för att tillämpa SAFE-regler för den här strömregeln.
   * **[!UICONTROL Disable SAFE Rules]**. Använd inte några SAFE-regler för den här strömmen.

Information om alternativ för strömningsregler som är specifika för ett socialt nätverk eller en innehållstyp finns i följande dokumentation för respektive typ av socialt nätverk eller innehåll:

* [Facebook Pages](../c-streams/c-facebook-page-rules.md#c_facebook_page_rules)
* [E-post](../c-streams/c-email-rules.md#c_email_rules)
* [Instagram](../c-streams/c-instagram-rules.md#c_instagram_rules)
* [Tumblr](../c-streams/c-tumblr-rules.md#c_tumblr_rules)
* [Twitter](../c-streams/c-twitter-rules.md#c_twitter_rules)
* [YouTube](../c-streams/c-youtube-rules/c-youtube-rules.md#c_youtube_rules)
* [RSS](../c-streams/c-rss-rules-streams.md#c_rss_rules_streams)
