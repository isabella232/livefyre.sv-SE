---
description: Svar på vanliga frågor (FAQs) om sekretessförfrågningar som är klara för GDPR.
seo-description: Svar på vanliga frågor (FAQs) om sekretessförfrågningar som är klara för GDPR.
seo-title: Frågor och svar om sekretess
solution: Experience Manager
title: Frågor och svar om sekretess
uuid: 0cd6f0d2-504d-46e9-ac46-070536cda086
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---


# Frågor och svar om sekretessförfrågningar{#privacy-request-faqs}

Svar på vanliga frågor (FAQs) om sekretessförfrågningar som är klara för GDPR.

* **Hur kan besökare på webbplatsen avanmäla sig från att spåras på en webbplats som använder Livefyre-appar?** När en besökare väljer ut en webbplats måste kundimplementeringen ange för Livefyre att användaren har avanmält sig innan en app instansieras. Livefyre har skapat ett sätt att göra detta med alternativet JavaScript, `userPrivacyOptOut`. Mer information om hur du använder `userPrivacyOptOut` finns i [userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

   När flaggan `userPrivacyOptOut` är true kommer appar på sidan inte att överföra data till Livefyre-servrar med hjälp av cookies eller någon annan metod. Livefyre kommer då inte att uppdatera den lokala lagringen med data som kan användas för att spåra besökare. Om en källa inte stöder en proxy visar Livefyre en mask i innehållet såvida inte en användare klickar på videon och godkänner den potentiella spårningen från den källan.

   Om du använder Livefyre-identitet kan användarna välja att ta bort sin profil eller skapa en rapport över data som spåras för sina användarkonton.

* **Hur förhindrar jag att framtida innehåll samlas in från en besökare som har valt att inte göra det?** Använd  `userPrivacyOptOut` med  `livefyre.js` på en webbsida där Livefyre-appar används. Mer information om `userPrivacyOptOut` finns i [userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md).

* **Hur skapar jag en rapport och tar bort data för appanvändare eller ägare av sociala konton?** [Sekretessbegäranden ](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) för att skapa en rapport och ta bort användardata från appar.

* **Hur tar jag bort allt innehåll för en besökare?** Livefyre bevarar inte beständig information om webbplatsbesökare, förutom i form av cookies som unikt identifierar dem för Livecount-funktioner. Livecount är ett övergående antal besökare i realtid på webbplatsen. Ingen historik bevaras efter att besökaren lämnar eller rensar cookies.

   Skapa en [sekretessbegäran](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) för att ta bort kontot. Livefyre tar bort eller gör användarprofilen och tillhörande poster anonyma.

* **Hur tar jag bort innehåll för en registrerad användare?** Skapa en  [sekretessbegäran ](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) om du vill ta bort kontot. Användarprofilen och alla associerade poster kommer att tas bort helt.

   >[!NOTE]
   >
   >Det går inte att ångra den här åtgärden.

* **Hur skapar jag en rapport över data som spårats av en aktuell eller tidigare anställd?** [Visa en sekretessrapport ](../../c-settings-other/c-gdpr-compliance/c-view-a-privacy-report.md#c_view_a_privacy_report) om du vill generera en rapport över data som spårats för ett användarkonto.

* **Klarar Livefyre sociala strömmar?** När en användare tar bort ett inlägg eller en tweet från sitt sociala nätverk, raderas även innehållet inom 24 timmar från alla källor i Livefyre. Detta gäller Twitter och Facebook.

