---
description: Du kan skapa strömregler som hämtar innehåll från e-post.
seo-description: Du kan skapa strömregler som hämtar innehåll från e-post.
seo-title: E-postregler
solution: Experience Manager
title: E-postregler
uuid: 3cd27d28-b7c0-4cbc-bae3-e2ef7beacba9
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# E-postregler{#email-rules}

Du kan skapa strömregler som hämtar innehåll från e-post.

Genom att skapa e-postbaserade strömmar kan du publicera innehåll direkt i en app eller mapp via e-post.

Använd den här funktionen om du vill att dina medarbetare ska kunna publicera direkt till dina appar eller resursbibliotek från datorn eller den mobila enheten.

När regeln har skapats kommer alla e-postmeddelanden som innehåller en bild- eller videofil som har skickats till den angivna e-postadressen att skickas direkt till ditt program eller resursbibliotek, enligt vad som anges. E-postmeddelanden som skickas med flera bilagor postar alla filer på lämplig plats. E-postmeddelanden som skickas till den angivna adressen som bara innehåller text gör ingenting.

När e-postmeddelandet har skickats används fälten för att fylla i följande objekt för innehållet:

* **[!UICONTROL From:]** Används som innehållets författare, om användarkontot finns. Om det inte finns något konto för avsändaren listas författaren som anonym.
* **[!UICONTROL Subject:]** Används för innehållets titel.
* **[!UICONTROL Body:]** Används för att fylla i innehållsinformation i Studio.
* **[!UICONTROL Attachments:]** Mediefiler måste bifogas, annars ignoreras e-postmeddelandet. Filtyper som stöds är 3GP, ASF, AVI, DV, GIF, JPG, MOV, MP4, MPEG, MPG, PNG, QT och WMV. Totalt för alla bilagor måste vara mindre än 25 MB.

Ytterligare alternativ för strömningsregler för alla strömregler finns i Alternativ för [strömningsregel för alla strömregler](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
