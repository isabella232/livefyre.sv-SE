---
description: Du kan skapa strömregler som hämtar innehåll från Facebook Pages.
title: Facebook sidlinjaler
exl-id: 1dc728c6-81fa-4c6c-acba-d9a4aea71ed2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# Facebook Page Rules{#facebook-page-rules}

Du kan skapa strömregler som hämtar innehåll från Facebook Pages.

Du kan använda Facebook sidregler för att direktuppspela offentligt publicerat innehåll från Facebook Pages. Innehållet hämtas till appen eller mappen med samma frekvens som SocialSync, som ändras baserat på Facebook Page och posttrafikmönster. Länkar på Facebook Pages stöds också och kommer att visas i strömmen.

Om du vill skapa Facebook Page Rules för att hämta innehåll från Facebook sidor till din app eller mapp kan du filtrera efter:

* **[!UICONTROL Facebook Page]**

   * Ange **[!UICONTROL Name]** för sidan. Ange bara den avslutande texten för URL:en. **Till exempel:** Om du vill lägga till innehåll från  `https://facebook.com/KellysSuperFunFanPage` skriver du  ** KellysSuperFunFanPage i  **[!UICONTROL Name]** fältet.

   * Aktivera **[!UICONTROL Include Facebook Comments for each post]** om du vill inkludera användarkommentarer till sidinlägg.
   * Aktivera **[!UICONTROL Only Show Author Posts]** om du vill utesluta inlägg från andra användare.

Ytterligare alternativ för strömningsregler för alla strömregler finns i [Alternativ för strömningsregel för alla strömregler](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

>[!NOTE]
>
>Livefyre är begränsat till innehåll som tas emot från Facebook och kan därför inte garantera att alla inlägg på en Facebook Page kommer att tas med i strömmen.

>[!NOTE]
>
>Om både Facebook SocialSync och en Facebook-sidregel är aktiverade för en viss Facebook-sida, och användarkommentarer är aktiverade för Facebook sidregel, åsidosätts SocialSync av flödesregeln. Innehållet direktuppspelas i appen endast baserat på Facebook-regeln för sidurval, och inte med SocialSync.

De typer av innehåll som stöds av Facebook Page Curate är:

* Sidägare eller administratör

   * Status
   * Foton
   * Videofilmer som länkar

* Facebook Standard

   * Status
   * Foton
   * Videofilmer som länkar

* Tredje part

   * Status
