---
description: Lägg till flaggan userPrivacyOptOut på sidan så att en besökare kan avanmäla sig från spårningen.
seo-description: Lägg till flaggan userPrivacyOptOut på sidan så att en besökare kan avanmäla sig från spårningen.
seo-title: userPrivacyOptOut
title: userPrivacyOptOut
uuid: a043c50e-0a02-4c83-bbce-54b9b51316a5
translation-type: tm+mt
source-git-commit: 9e01dd4515c01154e3566a39b367b8efa4ec082a
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---


# userPrivacyOptOut{#userprivacyoptout}

Lägg till flaggan `userPrivacyOptOut` på sidan så att en besökare kan avanmäla sig från spårningen.

Livefyre tillhandahåller JavaScript-händelser för att spåra användaraktivitet i Livefyre-appar.

Om du bäddar in Livefyre-appar och en besökare inte godkänner spårning, kan du konfigurera Livefyre dynamiskt för att inaktivera funktioner för att säkerställa besökarens integritet.

När konfigurationen är konfigurerad kommer Livefyre att:

* Inaktivera autentiseringsstöd i appar.
* Inaktivera Livecount och händelsegenerering
* Ta bort befintliga cookies som skapats av appar som finns på sidan
* Proxy media with images from third party domains to prevent third party from creating cookies
* Aktivera klickning på videomasker för tredjepartsvideor som kräver ytterligare ett klick för att visas

## Konfigurera en sida för avanmälan

Integrering med inbäddning av Livefyre-appar kan konfigurera Livefyre när en besökare inte har gett sitt samtycke med en enda JavaScript-variabel.

Instruktioner:

1. Lägg till flaggan `userPrivacyOptOut` på sidan före JavaScript-koden `Livefyre.js`:

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. Lägg till `Livefyre.js` på sidan var som helst efter `userPrivacyOptOut`.

   Livefyre-appar instansieras med de förhöjda sekretessinställningarna.

   >[!NOTE]
   >
   >Ändra inte värdet på `userPrivacyOptOut` när Livefyre-apparna har lästs in.

Kontrollera att ditt arbetsflöde för samtycke anger `userPrivacyOptOut` som true om en besökare väljer att avanmäla sig.
