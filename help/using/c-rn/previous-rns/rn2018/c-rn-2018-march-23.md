---
description: Versionsinformation för utgåvan den 23 mars 2018.
seo-description: Versionsinformation för utgåvan den 23 mars 2018.
seo-title: 23 mars 2018
solution: Experience Manager
title: 23 mars 2018
uuid: b69b8715-ace4-48e0-8f54-ce4e12170ef3
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---


# 23 mars 2018{#march}

Versionsinformation för utgåvan den 23 mars 2018.

## Nya funktioner {#section_syx_mdt_wcb}

Följande funktioner är nya i produktionsversionen av den här versionen:

* **Nytt i produktion:** Facebook skapade en säkerhetsuppdatering för Facebook-inloggning som gör att kundens Facebook-inloggning inte fungerar som den ska. För att åtgärda problemet måste du:

   1. Lägg till följande URL i fältet **[!UICONTROL Valid OAuth redirect URIs]** i OAuth-inställningar för klient. Ersätt `<networkname>` med rätt nätverksnamn:
      `https://identity.livefyre.com/<networkname>/api/v1.0/public/profile/social/complete/facebook_fyre`

   1. Växla **[!UICONTROL Use Strict Mode for Redirect URI]** till **[!UICONTROL Yes]**.

* **Nytt i UAT:** Du kan nu välja ett konfidensintervall för smarta taggar i strömmar. Genom att ställa in precisionspoängen (0-100) för taggar kan du styra exaktheten för de resurser som vi hämtar.

## Problem {#section_ehw_ndt_wcb}

Problemen i följande tabeller löstes i den här versionen.

## Produktionsrelease

| **Ärendetyp** | **Komponent** | **Versionsinformation** |
|---|---|---|
| Fel | Media Wall | Korrigerade ett problem i Medievägg där taggar inte kunde klickas när ett Instagram-inlägg lades till från en direktuppspelningsregel. |
| Fel | ModQ | Ett problem med ModQ som inte lästes in korrekt har åtgärdats. |
| Fel | ModQ | Korrigerade ett problem där inbäddning av ljud fick ModQ att sluta fungera. |

## UAT-release

| **Ärendetyp** | **Komponent** | **Versionsinformation** |
|---|---|---|
| Förbättring | Bildband | Korrigerade några problem som gjorde bildbandet mer tillgängligt. |
| Förbättring | Studio | Nu kan du logga in på Livefyre med en IMS-inloggning. |

