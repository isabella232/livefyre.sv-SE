---
description: Du kan skapa strömregler som hämtar innehåll från Twitter.
seo-description: Du kan skapa strömregler som hämtar innehåll från Twitter.
seo-title: Twitter-regler
solution: Experience Manager
title: Twitter-regler
uuid: a7fd2398-fd6b-4c24-92b2-7471176d7648
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Twitter-regler{#twitter-rules}

Du kan skapa strömregler som hämtar innehåll från Twitter.

Skapa Twitter-regler baserade på hashtaggar, nyckelord, @mentions eller författare.

Om du lägger till **[!UICONTROL Words]** och ett **[!UICONTROL Username]** för regeln returneras innehåll som innehåller båda posterna.

>[!NOTE]
>
>Livefyre följer riktlinjerna för Twitters webbannonsering, och kunderna ansvarar också för att följa dessa riktlinjer. Mer information finns i Twitters dokumentation om [skärmkraven](https://dev.twitter.com/terms/display-requirements).

Om du vill skapa Twitter-regler för att hämta innehåll från Twitter-flöden till din app eller mapp kan du filtrera efter:

* **[!UICONTROL Keywords]**
   * Ange **[!UICONTROL Keywords]** som ska inkluderas i eller exkluderas från Twitter-strömmen. Om du anger värden för både **[!UICONTROL Contains any of these words]** - och **[!UICONTROL Does not contain any of these words]** -fält returneras tweets som innehåller det första och inte innehåller det andra. Flera värden kan anges för ett enskilt fält och returnerar resultat som innehåller något av värdena. Om du vill använda den booleska operatorn AND för att söka efter interpoleringar med två eller flera ord använder du två et-tecken (*&amp;*) för att avgränsa de två orden.
   * Om du till exempel anger **[!UICONTROL Contains any of these words]** nyckelorden Giants, Posey och **[!UICONTROL Does not contain any of these words]** nyckelordet Dodger returneras alla Tweets som innehåller ordet *Giants* eller *Posey* och inte ordet *Dodger*.
Om du vill söka efter tweets som innehåller både *Giants* och *Posey* anger du&quot;Giants &amp;&amp; Posey&quot;. Den här funktionen stöds bara för **[!UICONTROL Contains any of these words]** - och **[!UICONTROL Does not contain any of these words]** -fälten i Twitter-regler.

* **[!UICONTROL Hashtags]**.
   * Ange **[!UICONTROL Hashtags]** som ska inkluderas i eller exkluderas från Twitter-strömmen. Om du anger värden för både **[!UICONTROL Contains any of these words]** och **[!UICONTROL Does not contain any of these words]** fält returneras tweets som innehåller hashtaggar i det första fältet, och de innehåller inga hashtaggar i det andra fältet. Du kan ange flera värden för ett enskilt fält. Strömmen returnerar resultat som innehåller något av värdena.

* **[!UICONTROL Usernames]**
   * Ange **[!UICONTROL @mentions]** eller **[!UICONTROL authors]** dra in i strömmen, eller exkludera från strömmen. Använd kryssrutorna för att ange om **[!UICONTROL Retweets]** eller **[!UICONTROL replies]** från valda författare också ska tas med.
   >[!NOTE]
   >
   >Du kan antingen inkludera eller utesluta författare; Du kan inte kombinera dessa två fält till en enda Twitter-regel.

* **[!UICONTROL Minimum number of followers.]** Välj det minsta antal följare som användaren måste ha för att hämta information från sina inlägg.
* **[!UICONTROL Location]**

   * Ange platsen (ort, postnummer, adress eller geokod i det vanliga latitud-/longitudformatet (+/- 90, +/- 180)). Börja skriva en plats för att visa en nedrullningsbar meny med förslag. Välj en plats i listrutan. Kartan visar ett häftstift på den platsen. Justera skjutreglaget för att välja en radie på 1 till 25 mil för varje plats. Om du inte väljer en radie väljer Livefyre automatiskt ett standardvärde på åtta engelska mil.
   >[!NOTE]
   >
   >För båda fälten beräknas avståndet från mitten av indataplatsen.

   * Du kan lägga till mer än en plats och radie. Du kan ta bort en plats genom att klicka på X bredvid namnet på en plats i rutan.
   * Kombinera fälten **[!UICONTROL Is near this location]** och **[!UICONTROL Is not near this location]** för att hämta innehåll inom platser i **[!UICONTROL Is near this location]** fältet, men inte nära platserna i **[!UICONTROL Is not near this location]** fältet.


* **[!UICONTROL Additional Filters]**
   * Använd ytterligare filter för att förfina Twitter-regeln ytterligare. Ange om du vill:
      * Inkludera **[!UICONTROL Replies]** i målinterpoleringarna (om strömmen blir hög kommer den här funktionen automatiskt att inaktiveras.)
      * Inkludera tweets från **[!UICONTROL Verified Twitter accounts only.]**
      * Inkludera **[!UICONTROL All Content]**, eller **[!UICONTROL Vines Only]**, eller **[!UICONTROL Images Only.]**
      * Inkludera endast interpoleringar som kommer från konton med det valda objektet **[!UICONTROL Minimum number of followers]** (any, 100, 500, 1000, 10,000 eller 100,000).

Ytterligare alternativ för strömningsregler för alla strömregler finns i Alternativ för [strömningsregel för alla strömregler](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
