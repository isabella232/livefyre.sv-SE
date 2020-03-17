---
description: Lägg till Livefyre i era mobilappar.
seo-description: Lägg till Livefyre i era mobilappar.
seo-title: SDK för mobiler
solution: Experience Manager
title: SDK för mobiler
uuid: 84c7ca1c-3401-492a-bfa5-62b996947a44
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# SDK för mobiler{#mobile-sdks}

Lägg till Livefyre i era mobilappar.

Det finns flera alternativ för mobilimplementeringar, beroende på hur omfattande anpassning du planerar att göra:

* Webbappar för mobiler
* Livefyre Android eller iOS SDKs
* HTTP-API:er

## Webbappar för mobiler {#section_t2k_vpb_11b}

Kunder som öppnar en webbsida på en mobil enhet får automatiskt en Livefyre-innehållsström som är optimerad för mobilen, inklusive en formatering som passar den reducerade skärmstorleken och modifieringar som hanterar pekhändelser.

>[!NOTE]
>
>När du använder en Livefyre-app i en Android WebView måste parametern Android [WebSettings.setDomStorageEnabled](https://developer.android.com/reference/android/webkit/WebSettings.html) anges till true. Om localStorage inte är aktiverat kan Livefyre inte logga in användare i Livefyre-appen.

För att optimera för mobilen begränsar Livefyre funktionerna Comments, Live Blog och Chat App till att omfatta:

* Bokför
* Redigera
* Flagga
* Gilla
* Svara
* Avlyssnarantal
* Antal kommentarer
* Inline väntar moderering
* Hovercards
* Vanliga kommentarer
* Aktiva trådar
* Kökommentarer

Om du klickar på en författares namn i Mobile Web Apps öppnas hovercard-information på en ny sida.

## Livefyre Android SDK eller iOS SDK {#section_zdz_spb_11b}

Livefyre har även två SDK för mobiler: en iOS SDK och en Android SDK. Dessa SDK:er är omslutningar runt våra HTTP-slutpunkter, som är byggda för att ge ett enklare sätt att skicka och ta emot data. Det finns inget gränssnitt för dessa SDK:er, vilket ger större flexibilitet vad gäller hur innehållet visas och används i mobilappen.

Android- och iOS-SDK:er har stöd för följande funktioner för kommentarer, Live-bloggar och chatt:

| iOS-funktioner: | Android-funktioner: |
|--- |--- |
| <ul><li> Bokför </li><li>Redigera </li><li>Flagga </li><li>Gilla </li><li>Svara </li><li>Aktiva trådar</li></ul> | <ul><li>Bokför </li><li>Redigera </li><li>Gilla </li><li>Svara </li><li>Aktiva trådar</li></ul> |

## HTTP-API:er {#section_yqb_qpb_11b}

HTTP-API:erna är den grupp slutpunkter som du kan använda för att skapa konversationer och innehåll på Livefyre-plattformen. Den gör också att Livefyre kan lämna boxströmmarna. Lösningen kräver mer utvecklingstid från teknikteamet, men den ger större flexibilitet när man använder produktsviten Livefyre och möjliggör inbyggd mobilintegrering.

>[!IMPORTANT]
>
>**Skapa inte** autentiseringstoken för användare i den mobila klienten eftersom du då måste visa den hemliga nätverksnyckeln för Livefyre i en oskyddad app. En mer robust och säker lösning finns i avsnittet för token för användarautentisering.

