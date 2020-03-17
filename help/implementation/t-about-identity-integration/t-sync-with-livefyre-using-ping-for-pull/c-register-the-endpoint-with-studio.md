---
description: Registrera URL-slutpunkten så att Livefyre kan använda URL:en för att hämta uppdaterad profilinformation.
seo-description: Registrera URL-slutpunkten så att Livefyre kan använda URL:en för att hämta uppdaterad profilinformation.
seo-title: Registrera slutpunkten med Studio
solution: Experience Manager
title: Registrera slutpunkten med Studio
uuid: 4eb816ee-d743-43bf-bfee-d9b9fd98b482
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Registrera slutpunkten med Studio{#register-the-endpoint-with-studio}

Registrera URL-slutpunkten så att Livefyre kan använda URL:en för att hämta uppdaterad profilinformation.

Registrera Ping for Pull URL endast en gång per nätverk. När värdet har angetts ska det inte ändras om inte slutpunkten för hämtning av användarprofildata från ditt användarhanteringssystem ändras.

1. Använd Studio för att registrera den här URL-slutpunkten hos Livefyre.
1. Registrera den URL som Livefyre hämtar uppdaterad användarprofilinformation från, gå till **[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]** och ange den i **[!UICONTROL Ping for Pull URL]** fältet.

   URL-adressen kan till exempel se ut så här: `https://example.yoursite.com/some_path/?id={id}`

