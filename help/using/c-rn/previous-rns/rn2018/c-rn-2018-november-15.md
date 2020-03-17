---
description: Versionsinformation för 15 november 2018.
seo-description: Versionsinformation för 15 november 2018.
seo-title: Versionsinformation
solution: Experience Manager
title: Versionsinformation
uuid: 34e64943-dea6-46ac-9fcc-8febeab6aa42
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104

---


# Versionsinformation{#release-notes}

Versionsinformation för 15 november 2018.

## Nya funktioner {#section_syx_mdt_wcb}

Följande nya funktioner släpptes i produktionsversionen av den här versionen:

* **Uppdateringar av Instagram-sökning och -strömning.** Du kan använda ett *Instagram-företagskonto* för att:

   * Utför en social sökning i Instagram per användare (användaren måste också vara ett Instagram-affärskonto).

   * Skapa Instagram-strömmar från ett specifikt Instagram-användarkonto (kontot måste också vara ett företagskonto), inklusive ditt eget.

   * Begär rättigheter för resurser från Instagram via ett delvis automatiserat arbetsflöde.

   * Information om vilken typ av Instagram-konton du behöver för att ställa in och begära rättigheter från Instagram finns i [Om Instagram-konton](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md).

* **Automatisk övervakning av användningsrättigheter begär svar för företagskontobaserade sökningar.** Endast för företagskontonsbaserade sökningar - möjlighet att automatiskt övervaka svar på förfrågningar om rättigheter och uppdatera aktivitetshistoriken i Livefyre är tillgängligt.

Mer information om hur du begär rättigheter för Instagram-konton finns i [Skicka Instagram Rights Request manuellt](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md) och [Skicka en delvis automatiserad Instagram Rights Request](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md).

* **Integrering med Adobe Target.** Tack vare den förbättrade integrationen med Adobe Target kan du dela Livefyre-appar direkt i Adobe Target Offers Library. Mer information om hur du använder Livefyre med Adobe Target finns i [Target-dokumentationen](https://marketing.adobe.com/resources/help/en_US/livefyre/livefyre-target.html).

## Problem {#section_ehw_ndt_wcb}

Problemen i följande tabeller löstes i den här versionen.

### Produktionsrelease

| Ärendetyp | Komponent | Versionsinformation |
|--- |--- |--- |
| Problem | AppService: Livefyre-identitet | Ett problem har korrigerats där användaren klickade på [! UICONTROL Återställ till standard] återställde inte logotypen under Login Modal i Studio > Integration Settings > Livefyre Identity till standardbilden. |
| Problem | Bibliotek | Ett problem där en video som överfördes till biblioteket och sedan visades i resursinformationen inte visades korrekt har åtgärdats. |
| Problem | Strömmar | Korrigerade ett problem som förhindrade att produkter visades i en strömregel. |
| Problem | Strömmar | Ett problem har korrigerats där produkttaggar inte var tillgängliga för en strömregel. |
| Förbättring | Studio | Ett problem har korrigerats där produkt-ID inte visades i Livefyre Studio. |
| Problem | Studio: ModQ | Korrigerade ett problem där borttaget innehåll fortfarande visas i ModQ efter att det tagits bort. |

### UAT-release

| **Ärendetyp** | **Komponent** | **Versionsinformation** |
|---|---|---|
| Problem | Social komponent: Carousel | Korrigerade ett problem där länken Dela inte svarade och kopierade URL:en som förväntat i IE11 och Mozilla Firefox. |