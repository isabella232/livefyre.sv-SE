---
description: Registrera URL-slutpunkten så att Livefyre kan använda URL:en för att hämta uppdaterad profilinformation.
title: Registrera slutpunkten med Studio
exl-id: 2910a13a-ae88-41d7-ba7c-88d7a1dbe445
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Registrera slutpunkten med Studio{#register-the-endpoint-with-studio}

Registrera URL-slutpunkten så att Livefyre kan använda URL:en för att hämta uppdaterad profilinformation.

Registrera Ping for Pull URL endast en gång per nätverk. När värdet har angetts ska det inte ändras om inte slutpunkten för hämtning av användarprofildata från ditt användarhanteringssystem ändras.

1. Använd Studio för att registrera den här URL-slutpunkten hos Livefyre.
1. Registrera den URL som Livefyre hämtar uppdaterad användarprofilinformation från, gå till **[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]** och ange den i fältet **[!UICONTROL Ping for Pull URL]**.

   URL-adressen kan till exempel se ut så här: `https://example.yoursite.com/some_path/?id={id}`
