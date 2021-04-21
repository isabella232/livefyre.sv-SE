---
description: Du kan skapa strömregler som hämtar innehåll från YouTube regler.
title: YouTube Rules
exl-id: 720a6fc6-d5de-4c78-a14e-51bced6e8dda
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---

# YouTube Rules {#youtube-rules}

Du kan skapa strömregler som hämtar innehåll från YouTube regler.

Skapa YouTube-regler baserat på Användare, Kanal eller Spellista.

Om du vill skapa YouTube Rules för att hämta innehåll från YouTube till din app eller mapp kan du filtrera efter:

* **[!UICONTROL User]**
   * Ange huvudsträngen för en **[!UICONTROL User]** för att inkludera videor från användaren i strömmen.
   * Om URL:en för den användarfeed du vill ange är `https://www.youtube.com/user/livefyresupport` anger du bara `livefyresupport`.

* **[!UICONTROL Channel]**
   * Ange huvudsträngen för en **[!UICONTROL Channel]** om du vill inkludera videoklipp från en kanal i strömmen.
   * Om URL:en för den kanalfeed du vill mata in är `https://www.youtube.com/channel/UCeNZlh03MyUkjRlLFpVQxsg` anger du bara `UCeNZlh03MyUkjRlLFpVQxsg`.

* **[!UICONTROL Playlist]**
   * Ange huvudsträngen för en **[!UICONTROL Playlist]** för att inkludera videor från en spellista i strömmen.
   * Om URL:en för den spellistfeed du vill mata in är `https://www.youtube.com/playlist?list=PLFE5670C92BDAC201` anger du bara `PLFE5670C92BDAC201`

* **[!UICONTROL Include recent items.]** Om detta är inställt på:
   * **[!UICONTROL Enabled]** lägger Livefyre till de första 15 innehållsobjekten i din feed i strömmen, oavsett publiceringsdatum.
   * **[!UICONTROL Disabled]** lägger Livefyre till de första 15 innehållsobjekten i din feed i strömmen med ett publiceringsdatum som är samma som datumet då strömregeln skapades eller senare.

Ytterligare alternativ för strömningsregler för alla strömregler finns i [Alternativ för strömningsregel för alla strömregler](../../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
