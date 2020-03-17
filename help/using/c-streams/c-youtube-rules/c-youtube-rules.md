---
description: Du kan skapa strömregler som hämtar innehåll från YouTube-regler.
seo-description: Du kan skapa strömregler som hämtar innehåll från YouTube-regler.
seo-title: YouTube-regler
solution: Experience Manager
title: YouTube-regler
uuid: ec6a3780-7119-45c3-8ab2-fb0f9803d161
translation-type: tm+mt
source-git-commit: 30aa5cce5e7567208362cc35caeb7b7260c42f3b

---


# YouTube-regler {#youtube-rules}

Du kan skapa strömregler som hämtar innehåll från YouTube-regler.

Skapa YouTube-regler baserat på Användare, Kanal eller Spellista.

Om du vill skapa YouTube-regler för att hämta innehåll från YouTube till din app eller mapp kan du filtrera efter:

* **[!UICONTROL User]**
   * Ange vanlighetssträngen för en **[!UICONTROL User]** som ska inkludera videor från användaren i strömmen.
   * Om URL:en till den användarfeed du vill mata in är `https://www.youtube.com/user/livefyresupport`anger du bara `livefyresupport`.

* **[!UICONTROL Channel]**
   * Ange vanlighetssträngen för en video **[!UICONTROL Channel]** som ska inkluderas från en kanal i strömmen.
   * Om URL:en för den kanalfeed du vill mata in till exempel är `https://www.youtube.com/channel/UCeNZlh03MyUkjRlLFpVQxsg`anger du bara `UCeNZlh03MyUkjRlLFpVQxsg`.

* **[!UICONTROL Playlist]**
   * Ange vanlighetssträngen för en video **[!UICONTROL Playlist]** som ska inkluderas från en spellista i strömmen.
   * Om URL:en för den spellistfeed du vill mata in är `https://www.youtube.com/playlist?list=PLFE5670C92BDAC201`anger du bara `PLFE5670C92BDAC201`

* **[!UICONTROL Include recent items.]** Om detta är inställt på:
   * **[!UICONTROL Enabled]** lägger Livefyre till de första 15 innehållsobjekten i din feed i strömmen, oavsett publiceringsdatum.
   * **[!UICONTROL Disabled]** lägger Livefyre till de första 15 innehållsobjekten i din feed i strömmen med ett publiceringsdatum som är samma som datumet då strömregeln skapades eller senare.

Ytterligare alternativ för strömningsregler för alla strömregler finns i Alternativ för [strömningsregel för alla strömregler](../../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
