---
description: Du kan skapa direktuppspelningsregler som hämtar innehåll från Facebook-sidor.
seo-description: Du kan skapa direktuppspelningsregler som hämtar innehåll från Facebook-sidor.
seo-title: Regler för Facebook-sidor
solution: Experience Manager
title: Regler för Facebook-sidor
uuid: 2be63476-1a92-409d-a22f-e1ec66b6dcc8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Regler för Facebook-sidor{#facebook-page-rules}

Du kan skapa direktuppspelningsregler som hämtar innehåll från Facebook-sidor.

Du kan använda regler för Facebook-sidor för att direktuppspela offentligt publicerat innehåll från Facebook-sidor. Innehållet hämtas till appen eller mappen med samma frekvens som SocialSync, som ändras baserat på Facebook-sidan och posttrafikmönster. Länkar på Facebook-sidor stöds också och visas i strömmen.

Om du vill skapa sidregler för Facebook för att hämta innehåll från Facebook-sidor till din app eller mapp kan du filtrera efter:

* **[!UICONTROL Facebook Page]**

   * Ange sidans **[!UICONTROL Name]** namn. Ange bara den avslutande texten för URL:en. **Till exempel:** Om du vill lägga till innehåll från `https://facebook.com/KellysSuperFunFanPage`skriver du *KellysSuperFunFanPage* i **[!UICONTROL Name]** fältet.

   * Aktivera det här alternativet **[!UICONTROL Include Facebook Comments for each post]** om du vill inkludera användarkommentarer till inlägg på sidan.
   * Aktivera **[!UICONTROL Only Show Author Posts]** om du vill utesluta inlägg från andra användare.

Ytterligare alternativ för strömningsregler för alla strömregler finns i Alternativ för [strömningsregel för alla strömregler](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

>[!NOTE]
>
>Livefyre är begränsat till innehåll som tas emot från Facebook och kan därför inte garantera att alla inlägg på en Facebook-sida inkluderas i strömmen.

>[!NOTE]
>
>Om både Facebook SocialSync och en Facebook-sidregel är aktiverade för en viss Facebook-sida, och användarkommentarer är aktiverade för Facebook-sidregeln, åsidosätts SocialSync av strömningsregeln. Innehållet kommer att direktuppspelas i appen enbart baserat på Facebooks regel för sidurval, och inte med SocialSync.

De typer av innehåll som stöds av Facebook-sidurval är bland annat:

* Sidägare eller administratör

   * Status
   * Foton
   * Videofilmer som länkar

* Standard Facebook-användare

   * Status
   * Foton
   * Videofilmer som länkar

* Tredje part

   * Status

